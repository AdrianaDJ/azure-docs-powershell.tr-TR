---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 15ee05260a4714831808b68b1bc8b1784d9ffdd2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107374"
---
# <span data-ttu-id="ddca3-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ddca3-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="ddca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddca3-102">SYNOPSIS</span></span>
<span data-ttu-id="ddca3-103">Bir Kullanıcı, uygulama veya güvenlik grubuna anahtar kasası ile işlemler gerçekleştirmesi için var olan izinleri verir veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="ddca3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddca3-104">SYNTAX</span></span>

### <span data-ttu-id="ddca3-105">ByUserPrincipalName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ddca3-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddca3-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="ddca3-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddca3-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ddca3-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddca3-108">Her bir</span><span class="sxs-lookup"><span data-stu-id="ddca3-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddca3-109">Forkasa</span><span class="sxs-lookup"><span data-stu-id="ddca3-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddca3-110">Inputobjectbyobjectid</span><span class="sxs-lookup"><span data-stu-id="ddca3-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddca3-111">Inputobjectbyserviceprincipalname</span><span class="sxs-lookup"><span data-stu-id="ddca3-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddca3-112">Inputobjectbyuserprincipalname</span><span class="sxs-lookup"><span data-stu-id="ddca3-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddca3-113">Faizno</span><span class="sxs-lookup"><span data-stu-id="ddca3-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddca3-114">Inputobjectforkasa</span><span class="sxs-lookup"><span data-stu-id="ddca3-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddca3-115">Resourceıdbyobjectid</span><span class="sxs-lookup"><span data-stu-id="ddca3-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddca3-116">Resourceıdbyserviceprincipalname</span><span class="sxs-lookup"><span data-stu-id="ddca3-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddca3-117">Resourceıdbyuserprincipalname</span><span class="sxs-lookup"><span data-stu-id="ddca3-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddca3-118">Resourceıdbmapostaadresi</span><span class="sxs-lookup"><span data-stu-id="ddca3-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddca3-119">KaynakKimliği</span><span class="sxs-lookup"><span data-stu-id="ddca3-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddca3-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddca3-120">DESCRIPTION</span></span>
<span data-ttu-id="ddca3-121">**Set-Azanahtarvaultaccesspolicy** cmdlet 'i, bir Kullanıcı, uygulama veya güvenlik grubuna anahtar kasası ile belirtilen işlemleri gerçekleştirecek varolan izinleri verir veya bunları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="ddca3-122">Diğer kullanıcıların, uygulamaların veya güvenlik gruplarının Anahtar Kasası 'ndaki izinleri değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="ddca3-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="ddca3-123">Güvenlik grubunun izinlerini ayarlıyorsanız, bu işlem yalnızca bu güvenlik grubundaki kullanıcıları etkiler.</span><span class="sxs-lookup"><span data-stu-id="ddca3-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="ddca3-124">Aşağıdaki dizinlerin tümü aynı Azure dizini olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="ddca3-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="ddca3-125">Anahtar Kasası 'nın bulunduğu Azure aboneliğinin varsayılan dizini.</span><span class="sxs-lookup"><span data-stu-id="ddca3-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="ddca3-126">İzinleri verdiğiniz Kullanıcı veya uygulama grubunu içeren Azure dizini.</span><span class="sxs-lookup"><span data-stu-id="ddca3-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="ddca3-127">Bu koşullar karşılanmazsa senaryoların örnekleri ve bu cmdlet çalışmaz:</span><span class="sxs-lookup"><span data-stu-id="ddca3-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="ddca3-128">Anahtar kasayı yönetmek için kullanıcıya farklı bir kuruluştan yetki verme.</span><span class="sxs-lookup"><span data-stu-id="ddca3-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="ddca3-129">Her kuruluşun kendi dizini vardır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="ddca3-130">Azure hesabınızda birden çok dizin vardır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="ddca3-131">Bir uygulamayı varsayılan dizin dışında bir dizine kaydedersiniz, bu uygulamayı anahtar kasayı kullanacak şekilde yetkilenmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ddca3-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="ddca3-132">Uygulama varsayılan dizinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-132">The application must be in the default directory.</span></span>
<span data-ttu-id="ddca3-133">Kaynak grubu, bu cmdlet için isteğe bağlı olarak belirtilmesi durumunda daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="ddca3-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="ddca3-134">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddca3-134">EXAMPLES</span></span>

### <span data-ttu-id="ddca3-135">Örnek 1: bir Anahtar Kasası için kullanıcıya izinler verme ve izinleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="ddca3-135">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="ddca3-136">İlk komut, Azure Active Directory 'nizde bir kullanıcıya izinler PattiFuller@contoso.com vererek, Contoso03Vault adlı bir anahtar kasası ile anahtar ve gizli işlemler gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-136">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="ddca3-137">*Passby* parametresi, cmdlet tarafından döndürülen güncelleştirilmiş nesneye yol.</span><span class="sxs-lookup"><span data-stu-id="ddca3-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="ddca3-138">İkinci komut, ilk komutta verilen izinleri değiştirir PattiFuller@contoso.com , şimdi de bunları ayarlama ve silmenin yanı sıra gizli erişime izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="ddca3-138">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="ddca3-139">Bu komuttan sonra anahtar işlemlerinin izinleri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-139">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="ddca3-140">Son komut, PattiFuller@contoso.com anahtar işlemler için tüm izinleri kaldırmak üzere var olan izinleri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-140">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="ddca3-141">Gizli operasyonların izinleri bu komuttan sonra değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-141">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="ddca3-142">Örnek 2: gizlilikleri okumak ve yazmak için uygulama hizmeti sorumlusunun izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="ddca3-142">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="ddca3-143">Bu komut, Contoso03Vault adlı bir Anahtar Kasası için uygulama izinleri verir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-143">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="ddca3-144">*ServicePrincipalName* parametresi uygulamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-144">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="ddca3-145">Uygulama, Azure Active Directory 'inizde kaydettirilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-145">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="ddca3-146">*ServicePrincipalName* parametresinin değeri uygulamanın hizmet asıl adı veya uygulama kimliği GUID 'si olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-146">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="ddca3-147">Bu örnekte, hizmet asıl adı belirtilir `http://payroll.contoso.com` ve komut uygulama izinlerini okuma ve yazma</span><span class="sxs-lookup"><span data-stu-id="ddca3-147">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="ddca3-148">Örnek 3: nesne KIMLIĞINI kullanarak bir uygulamanın izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="ddca3-148">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="ddca3-149">Bu komut, uygulama izinlerinin gizli bilgileri okuyup yazabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ddca3-149">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="ddca3-150">Bu örnekte, uygulamanın hizmet sorumlusunun nesne KIMLIĞINI kullanan uygulama belirtilir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-150">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="ddca3-151">Örnek 4: Kullanıcı asıl adı için izinler verme</span><span class="sxs-lookup"><span data-stu-id="ddca3-151">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="ddca3-152">Bu komut, gizli erişim için belirtilen kullanıcı asıl adı için Get, LIST ve Permissions izinleri verir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-152">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="ddca3-153">Örnek 5: Microsoft. COMPUTE kaynak sağlayıcısı tarafından bir anahtar kasasından alınabilmesini sağlama</span><span class="sxs-lookup"><span data-stu-id="ddca3-153">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="ddca3-154">Bu komut, Microsoft. COMPUTE kaynak sağlayıcısı tarafından Contoso03Vault Key kasasından alınan gizliliklerin izinlerini verir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-154">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="ddca3-155">Örnek 6: güvenlik grubuna izinler verme</span><span class="sxs-lookup"><span data-stu-id="ddca3-155">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="ddca3-156">İlk komut, tüm Active Directory gruplarını almak için Get-AzADGroup cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-156">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="ddca3-157">Çıkışta, Group2 adlı **Group1** , **group2** ve **Group3** adlı 3 Grup görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="ddca3-157">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="ddca3-158">Birden çok grup aynı ada sahip olabilir ancak her zaman benzersiz bir ObjectID olabilir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-158">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="ddca3-159">Aynı ada sahip birden fazla grup döndürülürse, kullanmak istediğiniz birini belirlemek için çıkışta ObjectID 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ddca3-159">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="ddca3-160">Bu komutun çıkışını Set-AzKeyVaultAccessPolicy ile Anahtar Kasası için izin vermek üzere, **myownkasa** Group2.</span><span class="sxs-lookup"><span data-stu-id="ddca3-160">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="ddca3-161">Bu örnek, aynı komut satırında ' Group2 ' adlı grupları satır içinde numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-161">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="ddca3-162">Döndürülen listede ' Group2 ' adlı birden çok grup olabilir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-162">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="ddca3-163">Bu örnek, ilk olarak döndürülen listedeki dizin 0 ile gösterilen ilkini seçer \[ \] .</span><span class="sxs-lookup"><span data-stu-id="ddca3-163">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="ddca3-164">Örnek 7: müşteri yönetimli kiracı anahtarına Azure Information Protection erişimi verme (BYOK)</span><span class="sxs-lookup"><span data-stu-id="ddca3-164">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="ddca3-165">Bu komut, Azure bilgi koruması 'nı bir müşteri tarafından yönetilen anahtar (kendi anahtarınızı veya "BYOK" senaryosunu) Azure Information Protection kiracı anahtarı olarak kullanacak şekilde yetkilendirir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-165">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="ddca3-166">Bu komutu çalıştırdığınızda, kendi tuş kasa adınızı belirtin, ancak *servicePrincipalName* parametresini GUID **00000012-0000-0000-C000-000000000000** ile belirtmeniz ve örnekteki izinleri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-166">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="ddca3-167">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddca3-167">PARAMETERS</span></span>

### <span data-ttu-id="ddca3-168">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ddca3-168">-ApplicationId</span></span>
<span data-ttu-id="ddca3-169">.</span><span class="sxs-lookup"><span data-stu-id="ddca3-169">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-170">-Bypassobjectivseçvalidation</span><span class="sxs-lookup"><span data-stu-id="ddca3-170">-BypassObjectIdValidation</span></span>
<span data-ttu-id="ddca3-171">Nesnenin Azure Active Directory 'de bulunduğunu doğrulamadan bir nesne KIMLIĞI belirtmenize imkan verir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-171">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="ddca3-172">Bu parametreyi yalnızca, başka bir Azure kiracısından temsilci seçilen güvenlik grubuna başvuran bir nesne KIMLIĞINE anahtar kasaya erişim vermek istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="ddca3-172">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddca3-173">-DefaultProfile</span></span>
<span data-ttu-id="ddca3-174">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ddca3-174">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-175">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="ddca3-175">-EmailAddress</span></span>
<span data-ttu-id="ddca3-176">İzin verilecek kullanıcının kullanıcı e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-176">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="ddca3-177">Bu e-posta adresinin geçerli abonelikle ilişkilendirilmiş dizinde varolması ve benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-177">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-178">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="ddca3-178">-EnabledForDeployment</span></span>
<span data-ttu-id="ddca3-179">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ddca3-179">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-180">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ddca3-180">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="ddca3-181">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="ddca3-181">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-182">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="ddca3-182">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="ddca3-183">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="ddca3-183">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-184">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddca3-184">-InputObject</span></span>
<span data-ttu-id="ddca3-185">Anahtar Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="ddca3-185">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-186">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="ddca3-186">-ObjectId</span></span>
<span data-ttu-id="ddca3-187">İzin verilecek Azure Active Directory 'deki Kullanıcı veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-187">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-188">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ddca3-188">-PassThru</span></span>
<span data-ttu-id="ddca3-189">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ddca3-189">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ddca3-190">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ddca3-190">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-191">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="ddca3-191">-PermissionsToCertificates</span></span>
<span data-ttu-id="ddca3-192">Kullanıcıya veya hizmet sorumlusuna verilecek sertifika izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-192">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="ddca3-193">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="ddca3-193">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="ddca3-194">Al</span><span class="sxs-lookup"><span data-stu-id="ddca3-194">Get</span></span>
- <span data-ttu-id="ddca3-195">Listeniz</span><span class="sxs-lookup"><span data-stu-id="ddca3-195">List</span></span>
- <span data-ttu-id="ddca3-196">Silme</span><span class="sxs-lookup"><span data-stu-id="ddca3-196">Delete</span></span>
- <span data-ttu-id="ddca3-197">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="ddca3-197">Create</span></span>
- <span data-ttu-id="ddca3-198">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="ddca3-198">Import</span></span>
- <span data-ttu-id="ddca3-199">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="ddca3-199">Update</span></span>
- <span data-ttu-id="ddca3-200">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="ddca3-200">Managecontacts</span></span>
- <span data-ttu-id="ddca3-201">Jedokulu</span><span class="sxs-lookup"><span data-stu-id="ddca3-201">Getissuers</span></span>
- <span data-ttu-id="ddca3-202">Listissuers</span><span class="sxs-lookup"><span data-stu-id="ddca3-202">Listissuers</span></span>
- <span data-ttu-id="ddca3-203">Setiçilere</span><span class="sxs-lookup"><span data-stu-id="ddca3-203">Setissuers</span></span>
- <span data-ttu-id="ddca3-204">Deleteverenler</span><span class="sxs-lookup"><span data-stu-id="ddca3-204">Deleteissuers</span></span>
- <span data-ttu-id="ddca3-205">Manageverenler</span><span class="sxs-lookup"><span data-stu-id="ddca3-205">Manageissuers</span></span>
- <span data-ttu-id="ddca3-206">Bulaşan</span><span class="sxs-lookup"><span data-stu-id="ddca3-206">Recover</span></span>
- <span data-ttu-id="ddca3-207">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="ddca3-207">Backup</span></span>
- <span data-ttu-id="ddca3-208">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="ddca3-208">Restore</span></span>
- <span data-ttu-id="ddca3-209">Ilmaya</span><span class="sxs-lookup"><span data-stu-id="ddca3-209">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-210">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="ddca3-210">-PermissionsToKeys</span></span>
<span data-ttu-id="ddca3-211">Bir kullanıcı veya hizmet sorumlusuna atamak için anahtar işlem izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-211">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="ddca3-212">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="ddca3-212">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="ddca3-213">Çözmeye</span><span class="sxs-lookup"><span data-stu-id="ddca3-213">Decrypt</span></span>
- <span data-ttu-id="ddca3-214">Şifre</span><span class="sxs-lookup"><span data-stu-id="ddca3-214">Encrypt</span></span>
- <span data-ttu-id="ddca3-215">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="ddca3-215">UnwrapKey</span></span>
- <span data-ttu-id="ddca3-216">WrapKey</span><span class="sxs-lookup"><span data-stu-id="ddca3-216">WrapKey</span></span>
- <span data-ttu-id="ddca3-217">Ayarlandığını</span><span class="sxs-lookup"><span data-stu-id="ddca3-217">Verify</span></span>
- <span data-ttu-id="ddca3-218">ISS</span><span class="sxs-lookup"><span data-stu-id="ddca3-218">Sign</span></span>
- <span data-ttu-id="ddca3-219">Al</span><span class="sxs-lookup"><span data-stu-id="ddca3-219">Get</span></span>
- <span data-ttu-id="ddca3-220">Listeniz</span><span class="sxs-lookup"><span data-stu-id="ddca3-220">List</span></span>
- <span data-ttu-id="ddca3-221">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="ddca3-221">Update</span></span>
- <span data-ttu-id="ddca3-222">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="ddca3-222">Create</span></span>
- <span data-ttu-id="ddca3-223">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="ddca3-223">Import</span></span>
- <span data-ttu-id="ddca3-224">Silme</span><span class="sxs-lookup"><span data-stu-id="ddca3-224">Delete</span></span>
- <span data-ttu-id="ddca3-225">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="ddca3-225">Backup</span></span>
- <span data-ttu-id="ddca3-226">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="ddca3-226">Restore</span></span>
- <span data-ttu-id="ddca3-227">Bulaşan</span><span class="sxs-lookup"><span data-stu-id="ddca3-227">Recover</span></span>
- <span data-ttu-id="ddca3-228">Ilmaya</span><span class="sxs-lookup"><span data-stu-id="ddca3-228">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-229">-Permissionstogizlilikler</span><span class="sxs-lookup"><span data-stu-id="ddca3-229">-PermissionsToSecrets</span></span>
<span data-ttu-id="ddca3-230">Kullanıcıya veya hizmet sorumlusuna verilecek gizli işlem izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-230">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="ddca3-231">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="ddca3-231">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="ddca3-232">Al</span><span class="sxs-lookup"><span data-stu-id="ddca3-232">Get</span></span>
- <span data-ttu-id="ddca3-233">Listeniz</span><span class="sxs-lookup"><span data-stu-id="ddca3-233">List</span></span>
- <span data-ttu-id="ddca3-234">Ayarlanırsa</span><span class="sxs-lookup"><span data-stu-id="ddca3-234">Set</span></span>
- <span data-ttu-id="ddca3-235">Silme</span><span class="sxs-lookup"><span data-stu-id="ddca3-235">Delete</span></span>
- <span data-ttu-id="ddca3-236">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="ddca3-236">Backup</span></span>
- <span data-ttu-id="ddca3-237">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="ddca3-237">Restore</span></span>
- <span data-ttu-id="ddca3-238">Bulaşan</span><span class="sxs-lookup"><span data-stu-id="ddca3-238">Recover</span></span>
- <span data-ttu-id="ddca3-239">Ilmaya</span><span class="sxs-lookup"><span data-stu-id="ddca3-239">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-240">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="ddca3-240">-PermissionsToStorage</span></span>
<span data-ttu-id="ddca3-241">Kullanıcıya veya hizmet sorumlusuna vermek için yönetilen depolama hesabını ve SaS tanımlama işlem izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-241">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-242">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddca3-242">-ResourceGroupName</span></span>
<span data-ttu-id="ddca3-243">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-243">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-244">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ddca3-244">-ResourceId</span></span>
<span data-ttu-id="ddca3-245">Anahtar Kasası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ddca3-245">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-246">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ddca3-246">-ServicePrincipalName</span></span>
<span data-ttu-id="ddca3-247">İzin verilecek uygulamanın hizmet asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-247">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="ddca3-248">AzureActive dizininde uygulama için kaydettirilmiş olan istemci KIMLIĞI olarak da bilinen uygulama KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="ddca3-248">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="ddca3-249">Bu parametrenin belirttiği hizmet asıl adına sahip uygulama, geçerli aboneliğinizi içeren Azure dizininde kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-249">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-250">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ddca3-250">-UserPrincipalName</span></span>
<span data-ttu-id="ddca3-251">İzinlerin atanacağı kullanıcının Kullanıcı asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-251">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="ddca3-252">Bu Kullanıcı asıl adı, geçerli abonelikle ilişkilendirilmiş dizinde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ddca3-252">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-253">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ddca3-253">-VaultName</span></span>
<span data-ttu-id="ddca3-254">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-254">Specifies the name of a key vault.</span></span>
<span data-ttu-id="ddca3-255">Bu cmdlet, bu parametrenin belirttiği Anahtar Kasası için erişim ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-255">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-256">-Onay</span><span class="sxs-lookup"><span data-stu-id="ddca3-256">-Confirm</span></span>
<span data-ttu-id="ddca3-257">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ddca3-257">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddca3-258">-WhatIf</span></span>
<span data-ttu-id="ddca3-259">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddca3-259">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddca3-260">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ddca3-260">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddca3-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddca3-261">CommonParameters</span></span>
<span data-ttu-id="ddca3-262">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddca3-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddca3-263">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ddca3-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddca3-264">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddca3-264">INPUTS</span></span>

### <span data-ttu-id="ddca3-265">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultidentityıtem</span><span class="sxs-lookup"><span data-stu-id="ddca3-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="ddca3-266">System. String</span><span class="sxs-lookup"><span data-stu-id="ddca3-266">System.String</span></span>

## <span data-ttu-id="ddca3-267">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddca3-267">OUTPUTS</span></span>

### <span data-ttu-id="ddca3-268">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="ddca3-268">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ddca3-269">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddca3-269">NOTES</span></span>

## <span data-ttu-id="ddca3-270">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddca3-270">RELATED LINKS</span></span>

[<span data-ttu-id="ddca3-271">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="ddca3-271">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="ddca3-272">Remove-Azanahtar,</span><span class="sxs-lookup"><span data-stu-id="ddca3-272">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

