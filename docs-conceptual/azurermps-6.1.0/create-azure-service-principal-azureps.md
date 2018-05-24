---
title: Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma
description: Azure PowerShell ile uygulamanız veya hizmetiniz için nasıl hizmet sorumlusu oluşturabileceğinizi öğrenin.
keywords: Azure PowerShell, Azure Active Directory, Azure Active directory, AD, RBAC
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 92acd8e66a1244e050e035ef9929333ac09f3181
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2018
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Azure PowerShell ile bir Azure hizmet sorumlusu oluşturma

Uygulamanızı veya hizmetinizi Azure PowerShell ile yönetmeyi planlıyorsanız, uygulamanızı kendi kimlik bilgileriniz altında değil bir Azure Active Directory (AAD) hizmet sorumlusu altında çalıştırın. Bu konu başlığında, Azure PowerShell ile bir güvenlik sorumlusu oluşturma işlemi adım adım gösterilir.

> [!NOTE]
> Azure portalı aracılığıyla da hizmet sorumlusu oluşturabilirsiniz. Daha ayrıntılı bilgi edinmek için [Kaynaklara erişebilen bir Active Directory uygulaması ve hizmet sorumlusu oluşturmak için portalı kullanma](/azure/azure-resource-manager/resource-group-create-service-principal-portal) konusunu okuyun.

## <a name="what-is-a-service-principal"></a>'Hizmet sorumlusu' nedir?

Azure hizmet sorumlusu, kullanıcı tarafından oluşturulan uygulamalar, hizmetler ve otomasyon araçlarının belirli Azure kaynaklarına erişmek için kullandığı bir güvenlik kimliğidir. Bunu belirli bir rolü olan ve izinleri sıkı bir şekilde denetlenen bir "kullanıcı kimliği" (kullanıcı adı ve parola veya sertifika) olarak düşünebilirsiniz. Genel kullanıcı kimliğinin aksine, bu kimliğin yalnızca belirli şeyleri yapabilmesi gerekir. Hizmet sorumlusuna yönetim görevlerini gerçekleştirmesi için gereken en düşük izin düzeyini atamanız, güvenliği geliştirir.

## <a name="verify-your-own-permission-level"></a>Kendi izin düzeyinizi doğrulama

Öncelikle hem Azure Active Directory’nizde hem de Azure aboneliğinizde yeterli izinlere sahip olmanız gerekir. Özellikle de Active Directory’de bir uygulama oluşturabilmeniz ve hizmet sorumlusuna bir rol atayabilmeniz gerekir.

Hesabınızın yeterli izinlere sahip olup olmadığını denetlemenin en kolay yolu portalı kullanmaktır. Bkz. [Portalda gerekli izinleri denetleme](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Uygulamanız için hizmet sorumlusu oluşturma

Azure hesabınızda oturum açtığınızda hizmet sorumlusunu oluşturabilirsiniz. Dağıtılan uygulamanızı tanımlamak için aşağıdaki yollardan birine sahip olmanız gerekir:

* Dağıtılan uygulamanızın benzersiz adı (aşağıdaki örneklerde yer alan "MyDemoWebApp" gibi) veya
* Uygulama Kimliği, yani dağıtılan uygulama, hizmet veya nesnenizle ilişkili benzersiz GUID

### <a name="get-information-about-your-application"></a>Uygulamanız ile ilgili bilgi edinme

Uygulamanızla ilgili bilgileri keşfetmek için `Get-AzureRmADApplication` cmdlet’i kullanılabilir.

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a>Uygulamanız için hizmet sorumlusu oluşturma

Hizmet sorumlusunu oluşturmak için `New-AzureRmADServicePrincipal` cmdlet’i kullanılır.

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>Hizmet sorumlusuyla ilgili bilgi edinme

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>Hizmet sorumlusunu kullanarak oturum açma

Artık sağladığınız *appId* ve *parola* ile uygulamanızın yeni hizmet sorumlusu olarak oturum açabilirsiniz. Hesabınızın Kiracı Kimliğini sağlamanız gerekir. Kiracı Kimliğiniz, Azure’da kişisel kimlik bilgilerinizle oturum açtığınızda görüntülenir.

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Bu komutu yeni bir PowerShell oturumundan çalıştırın. Başarıyla oturum açtıktan sonra şuna benzeyen bir çıktı görürsünüz:

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Tebrikler! Uygulamanızı çalıştırmak için bu kimlik bilgilerini kullanabilirsiniz. Ardından, hizmet sorumlusunun izinlerini ayarlamanız gerekir.

## <a name="managing-roles"></a>Rolleri yönetme

> [!NOTE]
> Azure Rol Tabanlı Erişim Denetimi (RBAC), kullanıcı ve hizmet sorumlularının rollerini tanımlama ve yönetmeye yönelik bir modeldir. Rollerin kendileriyle ilişkili izin kümeleri vardır ve bir sorumlunun okuyabileceği, erişebileceği, yazabileceği ya da yönetebileceği kaynakları bunlar belirler. RBAC ve roller hakkında daha fazla bilgi edinmek için bkz. [RBAC: Yerleşik roller](/azure/active-directory/role-based-access-built-in-roles).

Azure PowerShell, rol atamalarını yönetmek için aşağıdaki cmdlet’leri sunar:

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

Bir hizmet sorumlusunun varsayılan rolü **Katkıda Bulunan**’dır. Geniş izinleri göz önünde bulundurulduğunda, uygulamanızın Azure hizmetleriyle gerçekleştirdiği etkileşimlerin kapsamına bağlı olarak, doğru bir seçim olmayabilir.
**Okuyucu** rolü daha kısıtlayıcıdır ve salt okunur uygulamalar için iyi bir seçim olabilir. Azure portalı aracılığıyla role özel izinlerin ayrıntılarını görüntüleyebilir veya özel roller oluşturabilirsiniz.

Bu örnekte, bir önceki örneğimize **Okuyucu** rolünü ekleyip **Katkıda Bulunan** rolünü siliyoruz:

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Şu anda atanmış olan rolleri görüntülemek için:

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

Rol yönetimi için diğer Azure PowerShell cmdlet’leri:

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Güvenlik sorumlusunun kimlik bilgilerini değiştirme

Düzenli aralıklarla izinleri gözden geçirmek ve parolayı güncelleştirmek, güvenlik açısından iyi bir uygulamadır. Uygulamanız değiştikçe güvenlik kimlik bilgilerini yönetmek ve değiştirmek de isteyebilirsiniz. Örneğin, yeni bir parola oluşturup eskisini kaldırarak hizmet sorumlusunun parolasını değiştirebiliriz.

### <a name="add-a-new-password-for-the-service-principal"></a>Hizmet sorumlusu için yeni parola ekleme

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Hizmet sorumlusunun kimlik bilgilerinin listesini alma

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Hizmet sorumlusundan eski parolayı kaldırma

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Hizmet sorumlusunun kimlik bilgileri listesini doğrulama

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
