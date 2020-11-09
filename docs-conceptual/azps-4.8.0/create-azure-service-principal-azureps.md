---
title: Azure PowerShell ile Azure hizmet sorumlularını kullanma
description: Azure PowerShell ile hizmet sorumluları oluşturmayı ve kullanmayı öğrenin.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 20a58253e3f9435a9d33c700435f77fbb42df7ea
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/05/2020
ms.locfileid: "93365118"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma

Azure hizmetlerini kullanan otomatikleştirilmiş araçlar her zaman kısıtlı erişime sahip olmalıdır. Azure, uygulamaların tam ayrıcalığa sahip kullanıcılar olarak oturum açmasına izin vermek yerine hizmet sorumlularını sunuyor.

Azure hizmet sorumlusu, Azure kaynaklarına erişen uygulamalar, barındırılan hizmetler ve otomatikleştirilmiş araçlar ile kullanılmak için oluşturulan bir kimliktir. Bu erişim, hizmet sorumlusuna atanan roller tarafından kısıtlanır ve hangi kaynaklara hangi düzeyde erişilebileceğini kontrol edebilirsiniz. Güvenlik nedeniyle, otomatikleştirilmiş araçların kullanıcı kimliği ile oturum açmalarına izin vermek yerine her zaman hizmet sorumlularını kullanmanız önerilir.

Bu makale, Azure PowerShell ile hizmet sorumlusu oluşturma, sıfırlama ve hakkında bilgi alma adımlarını gösterir.

> [!WARNING]
> [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) komutunu kullanarak hizmet sorumlusu oluşturduğunuzda, çıkışta korumanız gereken kimlik bilgileri yer alır. Bu kimlik bilgilerini kodunuza eklemediğinizden emin olun veya kaynak denetiminizdeki kimlik bilgilerini denetleyin. Alternatif olarak, kimlik bilgilerini kullanma gereksinimini ortadan kaldırmak için [yönetilen kimlikleri](/azure/active-directory/managed-identities-azure-resources/overview) kullanabilirsiniz.
>
> [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) varsayılan olarak [Katkıda bulunan](/azure/role-based-access-control/built-in-roles#contributor) rolünü abonelik kapsamında hizmet sorumlusuna atar. Güvenliği ihlal edilmiş hizmet sorumlusu riskinizi azaltmak için daha belirli bir rol atayın ve kapsamı kaynağa ya da kaynak grubuna daraltın. Daha fazla bilgi için bkz. [Rol ataması ekleme adımları](/azure/role-based-access-control/role-assignments-steps).

## <a name="create-a-service-principal"></a>Hizmet sorumlusu oluşturma

[New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet’i ile hizmet sorumlusu oluşturun. Hizmet sorumlusu oluştururken, kullanacağınız oturum açma kimlik doğrulaması türünü seçebilirsiniz.

> [!NOTE]
> Hesabınız hizmet sorumlusu oluşturma iznine sahip değilse `New-AzADServicePrincipal`, “İşlemi tamamlamak için yeterli ayrıcalık yok” iletisini içeren bir hata döndürür.
> Hizmet sorumlusu oluşturmak için Azure Active Directory yöneticinizle iletişime geçin.

Hizmet sorumluları için iki tür kimlik doğrulaması kullanılabilir: Parola tabanlı kimlik doğrulaması ve sertifika tabanlı kimlik doğrulaması.

### <a name="password-based-authentication"></a>Parola tabanlı kimlik doğrulaması

> [!IMPORTANT]
> Parola tabanlı kimlik doğrulaması hizmet sorumlusu için varsayılan rol **Katkıda Bulunan** ’dır. Bu rol, bir Azure hesabında okuma ve yazma için tam izne sahiptir. Rol atamalarını yönetme hakkında bilgi için bkz. [Hizmet sorumlusu rollerini yönetme](#manage-service-principal-roles).

Diğer kimlik doğrulaması parametreleri olmadan parola tabanlı kimlik doğrulaması kullanılır ve sizin için rastgele bir parola oluşturulur. Parola tabanlı kimlik doğrulaması istiyorsanız bu yöntem önerilir.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Döndürülen nesne, oluşturulan parolayı içeren bir `SecureString` olan `Secret` üyesini içerir. Hizmet sorumlusuyla kimlik doğrulaması yapabilmek için bu değeri güvenli bir yerde depoladığınızdan emin olun. Değeri, konsol çıkışında _görüntülenmez_. Parolayı kaybederseniz [hizmet sorumlusu kimlik bilgilerini sıfırlayın](#reset-credentials).

Aşağıdaki kod, gizli diziyi dışarı aktarmanıza olanak tanır:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

Kullanıcı tarafından sağlanan parolalar için `-PasswordCredential` bağımsız değişkeni `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` nesnelerini alır. Bu nesneler, geçerli `StartDate` ve `EndDate` değerleri içermeli ve düz metin `Password` kabul etmelidir. Parola oluştururken [Azure Active Directory parola kurallarına ve kısıtlamalarına](/azure/active-directory/active-directory-passwords-policy) uyduğunuzdan emin olun.
Zayıf bir parola kullanmayın ve parolaları tekrar kullanmayın.

```azurepowershell-interactive
Import-Module -Name Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz.

> [!IMPORTANT]
> Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir. Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan _hemen sonra_ şu komutu çalıştırın:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

### <a name="certificate-based-authentication"></a>Sertifika tabanlı kimlik doğrulaması

> [!IMPORTANT]
> Sertifika tabanlı kimlik doğrulaması hizmet sorumlusu oluşturulurken atanan varsayılan bir rol yoktur. Rol atamalarını yönetme hakkında bilgi için bkz. [Hizmet sorumlusu rollerini yönetme](#manage-service-principal-roles).

Sertifika tabanlı kimlik doğrulaması kullanan hizmet sorumluları `-CertValue` parametresiyle oluşturulur. Bu parametre, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesini alır. Bu, PEM dosyası ya da metin biçiminde kodlanmış CRT veya CER olarak temsil edilir. Ortak sertifikanın ikili kodlamaları desteklenmez. Bu yönergeler, mevcut bir sertifikanızın olduğunu varsayar.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

`PSADKeyCredential` nesnelerini alan `-KeyCredential` parametresini de kullanabilirsiniz. Bu nesneler geçerli `StartDate` ile `EndDate` değerleri içermelidir ve `CertValue` üyesi, ortak sertifikanın base64 biçiminde kodlanmış ASCII dizesine ayarlı olmalıdır.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

`New-AzADServicePrincipal` cmdlet’inden döndürülen nesne `Id` ve `DisplayName` üyelerini içerir. Hizmet sorumlusuyla oturum açmak için bunların herhangi birini kullanabilirsiniz. Hizmet sorumlusuyla oturum açan kullanıcıların sertifikanın özel anahtarına da erişim sağlamaları gerekir.

> [!IMPORTANT]
> Hizmet sorumlusuyla oturum açmak için hizmet sorumlusunun altında oluşturulduğu kiracı kimliği gerekir. Hizmet sorumlusu oluşturulduğunda etkin olan kiracıyı almak için hizmet sorumlusu oluşturulduktan _hemen sonra_ şu komutu çalıştırın:

```azurepowershell-interactive
(Get-AzContext).Tenant.Id
```

## <a name="get-an-existing-service-principal"></a>Mevcut bir hizmet sorumlusunu alma

Etkin kiracı için hizmet sorumlularının listesini [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) ile alabilirsiniz. Bu komut, varsayılan olarak bir kiracıdaki _tüm_ hizmet sorumlularını döndürür. Büyük kuruluşlarda sonuçların döndürülmesi uzun sürebilir. Bunun yerine, isteğe bağlı sunucu tarafı filtreleme bağımsız değişkenlerinin birini kullanmanız önerilir:

- `-DisplayNameBeginsWith`, sağlanan değer ile eşleşen _ön eke_ sahip hizmet sorumlularını ister. Hizmet sorumlusunun görünen adı, oluşturma sırasında `-DisplayName` ile ayarlanan değerdir.
- `-DisplayName`, bir hizmet sorumlusu adının _tam eşleşmesini_ ister.

## <a name="manage-service-principal-roles"></a>Hizmet sorumlusu rollerini yönetme

Azure PowerShell, rol atamalarını yönetmek için aşağıdaki cmdlet’leri içerir:

- [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
- [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
- [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

Parola tabanlı kimlik doğrulaması hizmet sorumlusu için varsayılan rol **Katkıda Bulunan** ’dır. Bu rol, bir Azure hesabında okuma ve yazma için tam izne sahiptir. **Okuyucu** rolü daha kısıtlayıcıdır, yalnızca salt okunur erişime sahiptir. Rol Tabanlı Erişim Denetimi (RBAC) ve roller hakkında daha fazla bilgi için bkz. [RBAC: Yerleşik roller](/azure/active-directory/role-based-access-built-in-roles).

Bu örnek, **Okuyucu** rolünü ekler ve **Katkıda Bulunan** rolünü kaldırır:

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName 'Reader'
Remove-AzRoleAssignment -ObjectId <service principal object ID> -RoleDefinitionName 'Contributor'
```

> [!IMPORTANT]
> Rol atama cmdlet'leri, hizmet sorumlusu nesne kimliğini almaz. Oluşturma zamanında üretilen ilişkili uygulama kimliğini alırlar. Hizmet sorumlusuna uygulama kimliği almak için `Get-AzADServicePrincipal` kullanın.

> [!NOTE]
> Hesabınızın rol atama izni yoksa hesabınızın “'Microsoft.Authorization/roleAssignments/write' eylemini gerçekleştirme yetkisi olmadığını” belirten bir hata iletisiyle karşılaşırsınız. Rolleri yönetmek için Azure Active Directory yöneticinizle iletişime geçin.

Bir rol eklendiğinde, önceden atanmış izinler _kısıtlanmaz_. Bir hizmet sorumlusunun izinlerini kısıtlarken **Katkıda Bulunan** rolü kaldırılmalıdır.

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
Connect-AzAccount -ServicePrincipal -Tenant <TenantId> -CertificateThumbprint <Thumbprint> -ApplicationId <ApplicationId>
```

Bir sertifikayı, PowerShell tarafından erişilebilir olan bir kimlik bilgileri deposundan içeri aktarmak için bkz. [Azure PowerShell ile Oturum Açma](authenticate-azureps.md#sp-signin)

## <a name="reset-credentials"></a>Kimlik bilgilerini sıfırlama

Hizmet sorumlusunun kimlik bilgilerini unutursanız rastgele bir parola ile yeni kimlik bilgileri eklemek için [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential) kullanın. Bu cmdlet, parola sıfırlanırken kullanıcı tanımlı kimlik bilgilerini desteklemez.

> [!IMPORTANT]
> Yeni kimlik bilgileri atamadan önce, mevcut kimlik bilgileri kullanılarak oturum açılmasını önlemek için bunları silebilirsiniz. Bunu yapmak için, [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet’ini kullanın:

```azurepowershell-interactive
Remove-AzADSpCredential -DisplayName ServicePrincipalName
```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```

## <a name="troubleshooting"></a>Sorun giderme

Şu hatayı alırsanız: _“New-AzADServicePrincipal: identifierUris özelliğine yönelik aynı değere sahip başka bir nesne zaten var.”_ aynı ada sahip başka bir hizmet sorumlusunun zaten mevcut olup olmadığını doğrulayın.

```azurepowershell-interactive
Get-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Mevcut hizmet sorumlusu artık gerekmiyorsa bunu aşağıdaki örneği kullanarak kaldırabilirsiniz.

```azurepowershell-interactive
Remove-AzAdServicePrincipal -DisplayName ServicePrincipalName
```

Ayrıca, önceden Azure Active Directory uygulaması için bir hizmet sorumlusu oluşturduysanız bu hatayla karşılaşabilirsiniz. Hizmet sorumlusunu kaldırsanız da uygulama kullanılabilir. Bu uygulama, aynı ada sahip başka bir hizmet sorumlusu oluşturmanızı engeller.

Aynı ada sahip başka bir Azure Active Directory uygulaması olup olmadığını doğrulamak için aşağıdaki örneği kullanabilirsiniz:

```azurepowershell-interactive
Get-AzADApplication -DisplayName ServicePrincipalName
```

Aynı ada sahip başka bir uygulama varsa ve artık bu uygulamaya ihtiyaç duymuyorsanız aşağıdaki örneği kullanarak bunu kaldırabilirsiniz.

```azurepowershell-interactive
Remove-AzADApplication -DisplayName ServicePrincipalName
```

Bu uygulamaya ihtiyaç duyuyorsanız oluşturmayı denediğiniz yeni hizmet sorumlusu için alternatif bir ad seçin.
