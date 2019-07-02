---
title: Azure PowerShell ile Azure hizmet sorumlularını kullanma
description: Azure PowerShell ile hizmet sorumluları oluşturmayı ve kullanmayı öğrenin.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: abb85d3d3f6a20697510447cda2c02b2703ef921
ms.sourcegitcommit: 5bdedc77b27b66998387486761ec67ed9326f169
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2019
ms.locfileid: "67345371"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma

Azure hizmetlerini kullanan otomatikleştirilmiş araçlar her zaman kısıtlı erişime sahip olmalıdır. Azure, uygulamaların tam ayrıcalığa sahip kullanıcılar olarak oturum açmasına izin vermek yerine hizmet sorumlularını sunuyor.

Azure hizmet sorumlusu, Azure kaynaklarına erişen uygulamalar, barındırılan hizmetler ve otomatikleştirilmiş araçlar ile kullanılmak için oluşturulan bir kimliktir. Bu erişim, hizmet sorumlusuna atanan roller tarafından kısıtlanır ve hangi kaynaklara hangi düzeyde erişilebileceğini kontrol edebilirsiniz. Güvenlik nedeniyle, otomatikleştirilmiş araçların kullanıcı kimliği ile oturum açmalarına izin vermek yerine her zaman hizmet sorumlularını kullanmanız önerilir.

Bu makale, Azure PowerShell ile hizmet sorumlusu oluşturma, sıfırlama ve hakkında bilgi alma adımlarını gösterir.

## <a name="create-a-service-principal"></a>Hizmet sorumlusu oluşturma

[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet’i ile hizmet sorumlusu oluşturun. Hizmet sorumlusu oluştururken, kullanacağınız oturum açma kimlik doğrulaması türünü seçebilirsiniz.

> [!NOTE]
>
> Hesabınız hizmet sorumlusu oluşturma iznine sahip değilse `New-AzADServicePrincipal`, “İşlemi tamamlamak için yeterli ayrıcalık yok” iletisini içeren bir hata döndürür. Hizmet sorumlusu oluşturmak için Azure Active Directory yöneticinizle iletişime geçin.

Hizmet sorumluları için iki tür kimlik doğrulaması kullanılabilir: Parola tabanlı kimlik doğrulaması ve sertifika tabanlı kimlik doğrulaması.

### <a name="password-based-authentication"></a>Parola tabanlı kimlik doğrulaması

Diğer kimlik doğrulaması parametreleri olmadan parola tabanlı kimlik doğrulaması kullanılır ve sizin için rastgele bir parola oluşturulur. Parola tabanlı kimlik doğrulaması istiyorsanız bu yöntem önerilir.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Döndürülen nesne, oluşturulan parolayı içeren bir `SecureString` olan `Secret` üyesini içerir. Hizmet sorumlusuyla kimlik doğrulaması yapabilmek için bu değeri güvenli bir yerde depoladığınızdan emin olun. Değeri, konsol çıkışında __görüntülenmez__. Parolayı kaybederseniz [hizmet sorumlusu kimlik bilgilerini sıfırlayın](#reset-credentials). 

Kullanıcı tarafından sağlanan parolalar için `-PasswordCredential` bağımsız değişkeni `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` nesnelerini alır. Bu nesneler, geçerli `StartDate` ve `EndDate` değerleri içermeli ve düz metin `Password` kabul etmelidir. Parola oluştururken [Azure Active Directory parola kurallarına ve kısıtlamalarına](/azure/active-directory/active-directory-passwords-policy) uyduğunuzdan emin olun. Zayıf bir parola kullanmayın ve parolaları tekrar kullanmayın.

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.

> [!IMPORTANT]
>
> Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir. Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan __hemen sonra__ şu komutu çalıştırın:
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a>Sertifika tabanlı kimlik doğrulaması

Sertifika tabanlı kimlik doğrulaması kullanan hizmet sorumluları `-CertValue` parametresiyle oluşturulur. Bu parametre, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesini alır. Bu, PEM dosyası ya da metin biçiminde kodlanmış CRT veya CER olarak temsil edilir. Ortak sertifikanın ikili kodlamaları desteklenmez. Bu yönergeler, mevcut bir sertifikanızın olduğunu varsayar.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

`PSADKeyCredential` nesnelerini alan `-KeyCredential` parametresini de kullanabilirsiniz. Bu nesneler geçerli `StartDate` ile `EndDate` değerleri içermelidir ve `CertValue` üyesi, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesine ayarlı olmalıdır.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz. Hizmet sorumlusuyla oturum açan kullanıcıların sertifikanın özel anahtarına da erişim sağlamaları gerekir.

> [!IMPORTANT]
>
> Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir. Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan __hemen sonra__ şu komutu çalıştırın:
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a>Mevcut bir hizmet sorumlusunu alma

[Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) ile şu anda etkin kiracı için hizmet sorumlularının listesini alabilirsiniz. Varsayılan olarak bu komut, kiracıda yer alan __tüm__ hizmet sorumlularını döndürür. Bu yüzden, büyük kuruluşlar için sonuçların döndürülmesi uzun sürebilir. Bunun yerine, isteğe bağlı sunucu tarafı filtreleme bağımsız değişkenlerinin birini kullanmanız önerilir:

* `-DisplayNameBeginsWith`, sağlanan değer ile eşleşen _ön eke_ sahip hizmet sorumlularını ister. Hizmet sorumlusunun görünen adı, oluşturma sırasında `-DisplayName` ile ayarlanan değerdir.
* `-DisplayName`, bir hizmet sorumlusu adının _tam eşleşmesini_ ister.

## <a name="manage-service-principal-roles"></a>Hizmet sorumlusu rollerini yönetme

Azure PowerShell, rol atamalarını yönetmek için aşağıdaki cmdlet’leri içerir:

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Bir hizmet sorumlusunun varsayılan rolü **Katkıda Bulunan**’dır. Bu rol, bir Azure hesabında okuma ve yazma için tam izne sahiptir. **Okuyucu** rolü daha kısıtlayıcıdır, yalnızca salt okunur erişime sahiptir.  Rol Tabanlı Erişim Denetimi (RBAC) ve roller hakkında daha fazla bilgi için bkz. [RBAC: Yerleşik roller](/azure/active-directory/role-based-access-built-in-roles).

Bu örnek, **Okuyucu** rolünü ekler ve **Katkıda Bulunan** rolünü kaldırır:

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> Rol atama cmdlet'leri, hizmet sorumlusu nesne kimliğini almaz. Oluşturma zamanında üretilen ilişkili uygulama kimliğini alırlar. Hizmet sorumlusuna uygulama kimliği almak için `Get-AzADServicePrincipal` kullanın.

> [!NOTE]
> Hesabınızın rol atama izni yoksa, hesabınızın “'Microsoft.Authorization/roleAssignments/write' eylemini gerçekleştirme yetkisi olmadığını” belirten bir hata iletisiyle karşılaşırsınız. Rolleri yönetmek için Azure Active Directory yöneticinizle iletişime geçin.

Bir rol eklendiğinde, önceden atanmış izinler _kısıtlanmaz_. Bir hizmet sorumlusunun izinlerini kısıtlarken __Katkıda Bulunan__ rolü kaldırılmalıdır.

Atanan roller listelenerek değişiklikler doğrulanabilir:

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>Hizmet sorumlusu kullanarak oturum açma

Oturum açarak yeni hizmet sorumlusunun kimlik bilgilerini ve izinlerini test edin. Hizmet sorumlusu ile oturum açmak için, hizmet sorumlusuyla ilişkilendirilen `applicationId` değeri ve altında oluşturulduğu kiracı gereklidir.

Hizmet sorumlusunda parola kullanarak oturum açmak için:

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

Sertifika tabanlı kimlik doğrulaması, Azure PowerShell’in sertifika parmak izini temel alarak bir yerel sertifika deposundan bilgi alabilir olmasını gerektirir.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

Bir sertifikayı, PowerShell tarafından erişilebilir olan bir kimlik bilgileri deposundan içeri aktarmak için bkz. [Azure PowerShell ile Oturum Açma](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>Kimlik bilgilerini sıfırlama

Hizmet sorumlusunun kimlik bilgilerini unutursanız yeni kimlik bilgileri eklemek için [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) kullanın. Bu cmdlet, `New-AzADServicePrincipal` ile aynı kimlik bilgileri bağımsız değişkenlerini ve türlerini alır. Kimlik bilgileri bağımsız değişkenleri olmadan, rastgele parola ile yeni bir `PasswordCredential` oluşturulur.

> [!IMPORTANT]
> Yeni kimlik bilgileri atamadan önce, mevcut kimlik bilgileri kullanılarak oturum açılmasını önlemek için bunları silebilirsiniz. Bunu yapmak için, [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet’ini kullanın:
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```