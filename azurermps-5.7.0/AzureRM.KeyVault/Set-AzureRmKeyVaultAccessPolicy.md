---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 20a36e35c509ecca889d4059bd7e74ccafa22dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588897"
---
# <span data-ttu-id="2a175-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a175-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="2a175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a175-102">SYNOPSIS</span></span>
<span data-ttu-id="2a175-103">Bir Kullanıcı, uygulama veya güvenlik grubuna anahtar kasası ile işlemler gerçekleştirmesi için var olan izinleri verir veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2a175-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a175-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a175-104">SYNTAX</span></span>

### <span data-ttu-id="2a175-105">ByUserPrincipalName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2a175-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a175-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="2a175-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a175-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2a175-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a175-108">Her bir</span><span class="sxs-lookup"><span data-stu-id="2a175-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a175-109">Forkasa</span><span class="sxs-lookup"><span data-stu-id="2a175-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a175-110">Inputobjectbyobjectid</span><span class="sxs-lookup"><span data-stu-id="2a175-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a175-111">Inputobjectbyserviceprincipalname</span><span class="sxs-lookup"><span data-stu-id="2a175-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a175-112">Inputobjectbyuserprincipalname</span><span class="sxs-lookup"><span data-stu-id="2a175-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a175-113">Faizno</span><span class="sxs-lookup"><span data-stu-id="2a175-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2a175-114">Inputobjectforkasa</span><span class="sxs-lookup"><span data-stu-id="2a175-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a175-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a175-115">DESCRIPTION</span></span>
<span data-ttu-id="2a175-116">**Set-AzureRmKeyVaultAccessPolicy** cmdlet 'i, belirli işlemleri Anahtar Kasası ile gerçekleştirmek için bir Kullanıcı, uygulama veya güvenlik grubuna mevcut izinleri verir veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2a175-116">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="2a175-117">Diğer kullanıcıların, uygulamaların veya güvenlik gruplarının Anahtar Kasası 'ndaki izinleri değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="2a175-117">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="2a175-118">Güvenlik grubunun izinlerini ayarlıyorsanız, bu işlem yalnızca bu güvenlik grubundaki kullanıcıları etkiler.</span><span class="sxs-lookup"><span data-stu-id="2a175-118">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="2a175-119">Aşağıdaki dizinlerin tümü aynı Azure dizini olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="2a175-119">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="2a175-120">Anahtar Kasası 'nın bulunduğu Azure aboneliğinin varsayılan dizini.</span><span class="sxs-lookup"><span data-stu-id="2a175-120">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="2a175-121">İzinleri verdiğiniz Kullanıcı veya uygulama grubunu içeren Azure dizini.</span><span class="sxs-lookup"><span data-stu-id="2a175-121">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="2a175-122">Bu koşullar karşılanmazsa senaryoların örnekleri ve bu cmdlet çalışmaz:</span><span class="sxs-lookup"><span data-stu-id="2a175-122">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="2a175-123">Anahtar kasayı yönetmek için kullanıcıya farklı bir kuruluştan yetki verme.</span><span class="sxs-lookup"><span data-stu-id="2a175-123">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="2a175-124">Her kuruluşun kendi dizini vardır.</span><span class="sxs-lookup"><span data-stu-id="2a175-124">Each organization has its own directory.</span></span> 
- <span data-ttu-id="2a175-125">Azure hesabınızda birden çok dizin vardır.</span><span class="sxs-lookup"><span data-stu-id="2a175-125">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="2a175-126">Bir uygulamayı varsayılan dizin dışında bir dizine kaydedersiniz, bu uygulamayı anahtar kasayı kullanacak şekilde yetkilenmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="2a175-126">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="2a175-127">Uygulama varsayılan dizinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a175-127">The application must be in the default directory.</span></span>

<span data-ttu-id="2a175-128">Kaynak grubu, bu cmdlet için isteğe bağlı olarak belirtilmesi durumunda daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="2a175-128">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="2a175-129">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a175-129">EXAMPLES</span></span>

### <span data-ttu-id="2a175-130">Örnek 1: bir Anahtar Kasası için kullanıcıya izinler verme ve izinleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="2a175-130">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="2a175-131">İlk komut, Azure Active Directory 'nizde bir kullanıcıya izinler PattiFuller@contoso.com vererek, Contoso03Vault adlı bir anahtar kasası ile anahtar ve gizli işlemler gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="2a175-131">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="2a175-132">İkinci komut, ilk komutta verilen izinleri değiştirir PattiFuller@contoso.com , şimdi de bunları ayarlama ve silmenin yanı sıra gizli erişime izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="2a175-132">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="2a175-133">Bu komuttan sonra anahtar işlemlerinin izinleri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="2a175-133">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="2a175-134">*Passby* parametresi, cmdlet tarafından döndürülen güncelleştirilmiş nesneye yol.</span><span class="sxs-lookup"><span data-stu-id="2a175-134">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="2a175-135">Son komut, PattiFuller@contoso.com anahtar işlemler için tüm izinleri kaldırmak üzere var olan izinleri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2a175-135">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="2a175-136">Gizli operasyonların izinleri bu komuttan sonra değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="2a175-136">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="2a175-137">*Passby* parametresi, cmdlet tarafından döndürülen güncelleştirilmiş nesneye yol.</span><span class="sxs-lookup"><span data-stu-id="2a175-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="2a175-138">Örnek 2: gizlilikleri okumak ve yazmak için uygulama hizmeti sorumlusunun izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="2a175-138">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="2a175-139">Bu komut, Contoso03Vault adlı bir Anahtar Kasası için uygulama izinleri verir.</span><span class="sxs-lookup"><span data-stu-id="2a175-139">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="2a175-140">*ServicePrincipalName* parametresi uygulamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-140">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="2a175-141">Uygulama, Azure Active Directory 'inizde kaydettirilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a175-141">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="2a175-142">*ServicePrincipalName* parametresinin değeri uygulamanın hizmet asıl adı veya uygulama kimliği GUID 'si olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a175-142">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="2a175-143">Bu örnekte, hizmet asıl adı belirtilir http://payroll.contoso.com ve komut uygulama izinlerini okuma ve yazma</span><span class="sxs-lookup"><span data-stu-id="2a175-143">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="2a175-144">Örnek 3: nesne KIMLIĞINI kullanarak bir uygulamanın izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="2a175-144">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="2a175-145">Bu komut, uygulama izinlerinin gizli bilgileri okuyup yazabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2a175-145">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="2a175-146">Bu örnekte, uygulamanın hizmet sorumlusunun nesne KIMLIĞINI kullanan uygulama belirtilir.</span><span class="sxs-lookup"><span data-stu-id="2a175-146">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="2a175-147">Örnek 4: Kullanıcı asıl adı için izinler verme</span><span class="sxs-lookup"><span data-stu-id="2a175-147">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="2a175-148">Bu komut, gizli erişim için belirtilen kullanıcı asıl adı için Get, LIST ve Permissions izinleri verir.</span><span class="sxs-lookup"><span data-stu-id="2a175-148">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="2a175-149">Örnek 5: Microsoft. COMPUTE kaynak sağlayıcısı tarafından bir anahtar kasasından alınabilmesini sağlama</span><span class="sxs-lookup"><span data-stu-id="2a175-149">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="2a175-150">Bu komut, Microsoft. COMPUTE kaynak sağlayıcısı tarafından Contoso03Vault Key kasasından alınan gizliliklerin izinlerini verir.</span><span class="sxs-lookup"><span data-stu-id="2a175-150">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="2a175-151">Örnek 6: güvenlik grubuna izinler verme</span><span class="sxs-lookup"><span data-stu-id="2a175-151">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="2a175-152">İlk komut, tüm Active Directory gruplarını almak için Get-AzureRmADGroup cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2a175-152">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="2a175-153">Çıkışta, Group2 adlı **Group1** , **group2** ve **Group3** adlı 3 Grup görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="2a175-153">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="2a175-154">Birden çok grup aynı ada sahip olabilir ancak her zaman benzersiz bir ObjectID olabilir.</span><span class="sxs-lookup"><span data-stu-id="2a175-154">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="2a175-155">Aynı ada sahip birden fazla grup döndürülürse, kullanmak istediğiniz birini belirlemek için çıkışta ObjectID 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a175-155">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="2a175-156">Bu komutun çıkışını Set-AzureRmKeyVaultAccessPolicy ile Anahtar Kasası için izin vermek üzere, **myownkasa** Group2.</span><span class="sxs-lookup"><span data-stu-id="2a175-156">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="2a175-157">Bu örnek, aynı komut satırında ' Group2 ' adlı grupları satır içinde numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="2a175-157">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="2a175-158">Döndürülen listede ' Group2 ' adlı birden çok grup olabilir.</span><span class="sxs-lookup"><span data-stu-id="2a175-158">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="2a175-159">Bu örnek, ilk olarak döndürülen listedeki dizin 0 ile gösterilen ilkini seçer \[ \] .</span><span class="sxs-lookup"><span data-stu-id="2a175-159">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="2a175-160">Örnek 7: müşteri yönetimli kiracı anahtarına Azure Information Protection erişimi verme (BYOK)</span><span class="sxs-lookup"><span data-stu-id="2a175-160">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="2a175-161">Bu komut, Azure bilgi koruması 'nı bir müşteri tarafından yönetilen anahtar (kendi anahtarınızı veya "BYOK" senaryosunu) Azure Information Protection kiracı anahtarı olarak kullanacak şekilde yetkilendirir.</span><span class="sxs-lookup"><span data-stu-id="2a175-161">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="2a175-162">Bu komutu çalıştırdığınızda, kendi tuş kasa adınızı belirtin, ancak *servicePrincipalName* parametresini GUID **00000012-0000-0000-C000-000000000000** ile belirtmeniz ve örnekteki izinleri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2a175-162">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="2a175-163">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a175-163">PARAMETERS</span></span>

### <span data-ttu-id="2a175-164">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2a175-164">-ApplicationId</span></span>
<span data-ttu-id="2a175-165">.</span><span class="sxs-lookup"><span data-stu-id="2a175-165">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-166">-Bypassobjectivseçvalidation</span><span class="sxs-lookup"><span data-stu-id="2a175-166">-BypassObjectIdValidation</span></span>
<span data-ttu-id="2a175-167">Nesnenin Azure Active Directory 'de bulunduğunu doğrulamadan bir nesne KIMLIĞI belirtmenize imkan verir.</span><span class="sxs-lookup"><span data-stu-id="2a175-167">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="2a175-168">Bu parametreyi yalnızca, başka bir Azure kiracısından temsilci seçilen güvenlik grubuna başvuran bir nesne KIMLIĞINE anahtar kasaya erişim vermek istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="2a175-168">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a175-169">-DefaultProfile</span></span>
<span data-ttu-id="2a175-170">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2a175-170">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-171">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="2a175-171">-EmailAddress</span></span>
<span data-ttu-id="2a175-172">İzin verilecek kullanıcının kullanıcı e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-172">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="2a175-173">Bu e-posta adresinin geçerli abonelikle ilişkilendirilmiş dizinde varolması ve benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2a175-173">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-174">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="2a175-174">-EnabledForDeployment</span></span>
<span data-ttu-id="2a175-175">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2a175-175">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-176">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2a175-176">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="2a175-177">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="2a175-177">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-178">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="2a175-178">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="2a175-179">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="2a175-179">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a175-180">-InputObject</span></span>
<span data-ttu-id="2a175-181">Anahtar Kasası nesnesi</span><span class="sxs-lookup"><span data-stu-id="2a175-181">Key Vault Object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-182">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="2a175-182">-ObjectId</span></span>
<span data-ttu-id="2a175-183">İzin verilecek Azure Active Directory 'deki Kullanıcı veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-183">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-184">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2a175-184">-PassThru</span></span>
<span data-ttu-id="2a175-185">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="2a175-185">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="2a175-186">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2a175-186">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-187">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="2a175-187">-PermissionsToCertificates</span></span>
<span data-ttu-id="2a175-188">Kullanıcıya veya hizmet sorumlusuna verilecek sertifika izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-188">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="2a175-189">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="2a175-189">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="2a175-190">Al</span><span class="sxs-lookup"><span data-stu-id="2a175-190">Get</span></span>
- <span data-ttu-id="2a175-191">Listeniz</span><span class="sxs-lookup"><span data-stu-id="2a175-191">List</span></span>
- <span data-ttu-id="2a175-192">Silme</span><span class="sxs-lookup"><span data-stu-id="2a175-192">Delete</span></span>
- <span data-ttu-id="2a175-193">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="2a175-193">Create</span></span>
- <span data-ttu-id="2a175-194">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="2a175-194">Import</span></span>
- <span data-ttu-id="2a175-195">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="2a175-195">Update</span></span>
- <span data-ttu-id="2a175-196">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="2a175-196">Managecontacts</span></span>
- <span data-ttu-id="2a175-197">Jedokulu</span><span class="sxs-lookup"><span data-stu-id="2a175-197">Getissuers</span></span>
- <span data-ttu-id="2a175-198">Listissuers</span><span class="sxs-lookup"><span data-stu-id="2a175-198">Listissuers</span></span>
- <span data-ttu-id="2a175-199">Setiçilere</span><span class="sxs-lookup"><span data-stu-id="2a175-199">Setissuers</span></span>
- <span data-ttu-id="2a175-200">Deleteverenler</span><span class="sxs-lookup"><span data-stu-id="2a175-200">Deleteissuers</span></span>
- <span data-ttu-id="2a175-201">Manageverenler</span><span class="sxs-lookup"><span data-stu-id="2a175-201">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-202">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="2a175-202">-PermissionsToKeys</span></span>
<span data-ttu-id="2a175-203">Bir kullanıcı veya hizmet sorumlusuna atamak için anahtar işlem izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-203">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="2a175-204">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="2a175-204">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="2a175-205">Çözmeye</span><span class="sxs-lookup"><span data-stu-id="2a175-205">Decrypt</span></span>
- <span data-ttu-id="2a175-206">Şifre</span><span class="sxs-lookup"><span data-stu-id="2a175-206">Encrypt</span></span>
- <span data-ttu-id="2a175-207">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="2a175-207">UnwrapKey</span></span>
- <span data-ttu-id="2a175-208">WrapKey</span><span class="sxs-lookup"><span data-stu-id="2a175-208">WrapKey</span></span>
- <span data-ttu-id="2a175-209">Ayarlandığını</span><span class="sxs-lookup"><span data-stu-id="2a175-209">Verify</span></span>
- <span data-ttu-id="2a175-210">ISS</span><span class="sxs-lookup"><span data-stu-id="2a175-210">Sign</span></span>
- <span data-ttu-id="2a175-211">Al</span><span class="sxs-lookup"><span data-stu-id="2a175-211">Get</span></span>
- <span data-ttu-id="2a175-212">Listeniz</span><span class="sxs-lookup"><span data-stu-id="2a175-212">List</span></span>
- <span data-ttu-id="2a175-213">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="2a175-213">Update</span></span>
- <span data-ttu-id="2a175-214">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="2a175-214">Create</span></span>
- <span data-ttu-id="2a175-215">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="2a175-215">Import</span></span>
- <span data-ttu-id="2a175-216">Silme</span><span class="sxs-lookup"><span data-stu-id="2a175-216">Delete</span></span>
- <span data-ttu-id="2a175-217">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="2a175-217">Backup</span></span>
- <span data-ttu-id="2a175-218">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="2a175-218">Restore</span></span>
- <span data-ttu-id="2a175-219">Bulaşan</span><span class="sxs-lookup"><span data-stu-id="2a175-219">Recover</span></span>
- <span data-ttu-id="2a175-220">Ilmaya</span><span class="sxs-lookup"><span data-stu-id="2a175-220">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-221">-Permissionstogizlilikler</span><span class="sxs-lookup"><span data-stu-id="2a175-221">-PermissionsToSecrets</span></span>
<span data-ttu-id="2a175-222">Kullanıcıya veya hizmet sorumlusuna verilecek gizli işlem izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-222">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="2a175-223">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="2a175-223">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="2a175-224">Al</span><span class="sxs-lookup"><span data-stu-id="2a175-224">Get</span></span>
- <span data-ttu-id="2a175-225">Listeniz</span><span class="sxs-lookup"><span data-stu-id="2a175-225">List</span></span>
- <span data-ttu-id="2a175-226">Ayarlanırsa</span><span class="sxs-lookup"><span data-stu-id="2a175-226">Set</span></span>
- <span data-ttu-id="2a175-227">Silme</span><span class="sxs-lookup"><span data-stu-id="2a175-227">Delete</span></span>
- <span data-ttu-id="2a175-228">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="2a175-228">Backup</span></span>
- <span data-ttu-id="2a175-229">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="2a175-229">Restore</span></span>
- <span data-ttu-id="2a175-230">Bulaşan</span><span class="sxs-lookup"><span data-stu-id="2a175-230">Recover</span></span>
- <span data-ttu-id="2a175-231">Ilmaya</span><span class="sxs-lookup"><span data-stu-id="2a175-231">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-232">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="2a175-232">-PermissionsToStorage</span></span>
<span data-ttu-id="2a175-233">Kullanıcıya veya hizmet sorumlusuna vermek için yönetilen depolama hesabını ve SaS tanımlama işlem izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-233">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-234">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a175-234">-ResourceGroupName</span></span>
<span data-ttu-id="2a175-235">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-235">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-236">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="2a175-236">-ServicePrincipalName</span></span>
<span data-ttu-id="2a175-237">İzin verilecek uygulamanın hizmet asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-237">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="2a175-238">AzureActive dizininde uygulama için kaydettirilmiş olan istemci KIMLIĞI olarak da bilinen uygulama KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="2a175-238">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="2a175-239">Bu parametrenin belirttiği hizmet asıl adına sahip uygulama, geçerli aboneliğinizi içeren Azure dizininde kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2a175-239">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-240">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2a175-240">-UserPrincipalName</span></span>
<span data-ttu-id="2a175-241">İzinlerin atanacağı kullanıcının Kullanıcı asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-241">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="2a175-242">Bu Kullanıcı asıl adı, geçerli abonelikle ilişkilendirilmiş dizinde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a175-242">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-243">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2a175-243">-VaultName</span></span>
<span data-ttu-id="2a175-244">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a175-244">Specifies the name of a key vault.</span></span>

<span data-ttu-id="2a175-245">Bu cmdlet, bu parametrenin belirttiği Anahtar Kasası için erişim ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2a175-245">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-246">-Onay</span><span class="sxs-lookup"><span data-stu-id="2a175-246">-Confirm</span></span>
<span data-ttu-id="2a175-247">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2a175-247">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-248">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a175-248">-WhatIf</span></span>
<span data-ttu-id="2a175-249">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a175-249">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a175-250">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2a175-250">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a175-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a175-251">CommonParameters</span></span>
<span data-ttu-id="2a175-252">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a175-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a175-253">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a175-253">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a175-254">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a175-254">INPUTS</span></span>

### <span data-ttu-id="2a175-255">Dize, Guid, String [], anahtar</span><span class="sxs-lookup"><span data-stu-id="2a175-255">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="2a175-256">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a175-256">OUTPUTS</span></span>

### <span data-ttu-id="2a175-257">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="2a175-257">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="2a175-258">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a175-258">NOTES</span></span>

## <span data-ttu-id="2a175-259">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a175-259">RELATED LINKS</span></span>

[<span data-ttu-id="2a175-260">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="2a175-260">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="2a175-261">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a175-261">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

