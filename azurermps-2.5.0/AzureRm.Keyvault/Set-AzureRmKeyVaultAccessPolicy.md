---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 413f0e22139abe26a2be34a607587042739df1d5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938810"
---
# <span data-ttu-id="fdbd8-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fdbd8-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="fdbd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="fdbd8-103">Bir Kullanıcı, uygulama veya güvenlik grubuna anahtar kasası ile işlemler gerçekleştirmesi için var olan izinleri verir veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdbd8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fdbd8-104">SYNTAX</span></span>

### <span data-ttu-id="fdbd8-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fdbd8-105">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdbd8-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fdbd8-106">ByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdbd8-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="fdbd8-107">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdbd8-108">Her bir</span><span class="sxs-lookup"><span data-stu-id="fdbd8-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdbd8-109">Forkasa</span><span class="sxs-lookup"><span data-stu-id="fdbd8-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdbd8-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="fdbd8-110">DESCRIPTION</span></span>
<span data-ttu-id="fdbd8-111">**Set-AzureRmKeyVaultAccessPolicy** cmdlet 'i, belirli işlemleri Anahtar Kasası ile gerçekleştirmek için bir Kullanıcı, uygulama veya güvenlik grubuna mevcut izinleri verir veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-111">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="fdbd8-112">Diğer kullanıcıların, uygulamaların veya güvenlik gruplarının Anahtar Kasası 'ndaki izinleri değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="fdbd8-113">Güvenlik grubunun izinlerini ayarlıyorsanız, bu işlem yalnızca bu güvenlik grubundaki kullanıcıları etkiler.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="fdbd8-114">Aşağıdaki dizinlerin tümü aynı Azure dizini olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="fdbd8-114">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="fdbd8-115">Anahtar Kasası 'nın bulunduğu Azure aboneliğinin varsayılan dizini.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="fdbd8-116">İzinleri verdiğiniz Kullanıcı veya uygulama grubunu içeren Azure dizini.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="fdbd8-117">Bu koşullar karşılanmazsa senaryoların örnekleri ve bu cmdlet çalışmaz:</span><span class="sxs-lookup"><span data-stu-id="fdbd8-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="fdbd8-118">Anahtar kasayı yönetmek için kullanıcıya farklı bir kuruluştan yetki verme.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="fdbd8-119">Her kuruluşun kendi dizini vardır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-119">Each organization has its own directory.</span></span> 
- <span data-ttu-id="fdbd8-120">Azure hesabınızda birden çok dizin vardır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="fdbd8-121">Bir uygulamayı varsayılan dizin dışında bir dizine kaydedersiniz, bu uygulamayı anahtar kasayı kullanacak şekilde yetkilenmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="fdbd8-122">Uygulama varsayılan dizinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-122">The application must be in the default directory.</span></span>

<span data-ttu-id="fdbd8-123">Kaynak grubu, bu cmdlet için isteğe bağlı olarak belirtilmesi durumunda daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="fdbd8-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fdbd8-124">EXAMPLES</span></span>

### <span data-ttu-id="fdbd8-125">Örnek 1: bir Anahtar Kasası için kullanıcıya izinler verme ve izinleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="fdbd8-125">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets 'set,delete'
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="fdbd8-126">İlk komut, Azure Active Directory 'nizde bir kullanıcıya izinler PattiFuller@contoso.com vererek, Contoso03Vault adlı bir anahtar kasası ile anahtar ve gizli işlemler gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="fdbd8-127">İkinci komut, ilk komutta verilen izinleri değiştirir PattiFuller@contoso.com , şimdi de bunları ayarlama ve silmenin yanı sıra gizli erişime izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="fdbd8-128">Bu komuttan sonra anahtar işlemlerinin izinleri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-128">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="fdbd8-129">*Passby* parametresi, cmdlet tarafından döndürülen güncelleştirilmiş nesneye yol.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="fdbd8-130">Son komut, PattiFuller@contoso.com anahtar işlemler için tüm izinleri kaldırmak üzere var olan izinleri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="fdbd8-131">Gizli operasyonların izinleri bu komuttan sonra değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-131">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="fdbd8-132">*Passby* parametresi, cmdlet tarafından döndürülen güncelleştirilmiş nesneye yol.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="fdbd8-133">Örnek 2: gizlilikleri okumak ve yazmak için uygulama hizmeti sorumlusunun izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="fdbd8-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="fdbd8-134">Bu komut, Contoso03Vault adlı bir Anahtar Kasası için uygulama izinleri verir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="fdbd8-135">*ServicePrincipalName* parametresi uygulamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-135">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="fdbd8-136">Uygulama, Azure Active Directory 'inizde kaydettirilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-136">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="fdbd8-137">*ServicePrincipalName* parametresinin değeri uygulamanın hizmet asıl adı veya uygulama kimliği GUID 'si olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="fdbd8-138">Bu örnekte, hizmet asıl adı belirtilir http://payroll.contoso.com ve komut uygulama izinlerini okuma ve yazma</span><span class="sxs-lookup"><span data-stu-id="fdbd8-138">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="fdbd8-139">Örnek 3: nesne KIMLIĞINI kullanarak bir uygulamanın izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="fdbd8-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="fdbd8-140">Bu komut, uygulama izinlerinin gizli bilgileri okuyup yazabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-140">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="fdbd8-141">Bu örnekte, uygulamanın hizmet sorumlusunun nesne KIMLIĞINI kullanan uygulama belirtilir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="fdbd8-142">Örnek 4: Kullanıcı asıl adı için izinler verme</span><span class="sxs-lookup"><span data-stu-id="fdbd8-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="fdbd8-143">Bu komut, gizli erişim için belirtilen kullanıcı asıl adı için Get, LIST ve Permissions izinleri verir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="fdbd8-144">Örnek 5: Microsoft. COMPUTE kaynak sağlayıcısı tarafından bir anahtar kasasından alınabilmesini sağlama</span><span class="sxs-lookup"><span data-stu-id="fdbd8-144">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="fdbd8-145">Bu komut, Microsoft. COMPUTE kaynak sağlayıcısı tarafından Contoso03Vault Key kasasından alınan gizliliklerin izinlerini verir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="fdbd8-146">Örnek 6: güvenlik grubuna izinler verme</span><span class="sxs-lookup"><span data-stu-id="fdbd8-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="fdbd8-147">İlk komut, tüm Active Directory gruplarını almak için Get-AzureRmADGroup cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-147">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="fdbd8-148">Çıkışta, Group2 adlı **Group1** , **group2** ve **Group3** adlı 3 Grup görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="fdbd8-149">Birden çok grup aynı ada sahip olabilir ancak her zaman benzersiz bir ObjectID olabilir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="fdbd8-150">Aynı ada sahip birden fazla grup döndürülürse, kullanmak istediğiniz birini belirlemek için çıkışta ObjectID 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="fdbd8-151">Bu komutun çıkışını Set-AzureRmKeyVaultAccessPolicy ile Anahtar Kasası için izin vermek üzere, **myownkasa** Group2.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-151">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="fdbd8-152">Bu örnek, aynı komut satırında ' Group2 ' adlı grupları satır içinde numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="fdbd8-153">Döndürülen listede ' Group2 ' adlı birden çok grup olabilir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="fdbd8-154">Bu örnek, ilk olarak döndürülen listedeki dizin 0 ile gösterilen ilkini seçer \[ \] .</span><span class="sxs-lookup"><span data-stu-id="fdbd8-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="fdbd8-155">Örnek 7: müşteri yönetimli kiracı anahtarına Azure Information Protection erişimi verme (BYOK)</span><span class="sxs-lookup"><span data-stu-id="fdbd8-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="fdbd8-156">Bu komut, Azure bilgi koruması 'nı bir müşteri tarafından yönetilen anahtar (kendi anahtarınızı veya "BYOK" senaryosunu) Azure Information Protection kiracı anahtarı olarak kullanacak şekilde yetkilendirir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="fdbd8-157">Bu komutu çalıştırdığınızda, kendi tuş kasa adınızı belirtin, ancak *servicePrincipalName* parametresini GUID **00000012-0000-0000-C000-000000000000** ile belirtmeniz ve örnekteki izinleri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-157">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="fdbd8-158">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fdbd8-158">PARAMETERS</span></span>

### <span data-ttu-id="fdbd8-159">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fdbd8-159">-ApplicationId</span></span>
<span data-ttu-id="fdbd8-160">.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-160">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-161">-Bypassobjectivseçvalidation</span><span class="sxs-lookup"><span data-stu-id="fdbd8-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="fdbd8-162">Nesnenin Azure Active Directory 'de bulunduğunu doğrulamadan bir nesne KIMLIĞI belirtmenize imkan verir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="fdbd8-163">Bu parametreyi yalnızca, başka bir Azure kiracısından temsilci seçilen güvenlik grubuna başvuran bir nesne KIMLIĞINE anahtar kasaya erişim vermek istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdbd8-164">-DefaultProfile</span></span>
<span data-ttu-id="fdbd8-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fdbd8-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdbd8-166">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="fdbd8-166">-EmailAddress</span></span>
<span data-ttu-id="fdbd8-167">İzin verilecek kullanıcının kullanıcı e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-167">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="fdbd8-168">Bu e-posta adresinin geçerli abonelikle ilişkilendirilmiş dizinde varolması ve benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-168">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-169">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="fdbd8-169">-EnabledForDeployment</span></span>
<span data-ttu-id="fdbd8-170">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-170">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-171">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fdbd8-171">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="fdbd8-172">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-172">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-173">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="fdbd8-173">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="fdbd8-174">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-174">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-175">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="fdbd8-175">-ObjectId</span></span>
<span data-ttu-id="fdbd8-176">İzin verilecek Azure Active Directory 'deki Kullanıcı veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-176">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-177">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fdbd8-177">-PassThru</span></span>
<span data-ttu-id="fdbd8-178">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-178">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="fdbd8-179">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-179">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fdbd8-180">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="fdbd8-180">-PermissionsToCertificates</span></span>
<span data-ttu-id="fdbd8-181">Kullanıcıya veya hizmet sorumlusuna verilecek sertifika izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-181">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="fdbd8-182">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="fdbd8-182">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="fdbd8-183">Al</span><span class="sxs-lookup"><span data-stu-id="fdbd8-183">Get</span></span>
- <span data-ttu-id="fdbd8-184">Listeniz</span><span class="sxs-lookup"><span data-stu-id="fdbd8-184">List</span></span>
- <span data-ttu-id="fdbd8-185">Silme</span><span class="sxs-lookup"><span data-stu-id="fdbd8-185">Delete</span></span>
- <span data-ttu-id="fdbd8-186">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="fdbd8-186">Create</span></span>
- <span data-ttu-id="fdbd8-187">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="fdbd8-187">Import</span></span>
- <span data-ttu-id="fdbd8-188">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="fdbd8-188">Update</span></span>
- <span data-ttu-id="fdbd8-189">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="fdbd8-189">Managecontacts</span></span>
- <span data-ttu-id="fdbd8-190">Jedokulu</span><span class="sxs-lookup"><span data-stu-id="fdbd8-190">Getissuers</span></span>
- <span data-ttu-id="fdbd8-191">Listissuers</span><span class="sxs-lookup"><span data-stu-id="fdbd8-191">Listissuers</span></span>
- <span data-ttu-id="fdbd8-192">Setiçilere</span><span class="sxs-lookup"><span data-stu-id="fdbd8-192">Setissuers</span></span>
- <span data-ttu-id="fdbd8-193">Deleteverenler</span><span class="sxs-lookup"><span data-stu-id="fdbd8-193">Deleteissuers</span></span>
- <span data-ttu-id="fdbd8-194">Manageverenler</span><span class="sxs-lookup"><span data-stu-id="fdbd8-194">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-195">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="fdbd8-195">-PermissionsToKeys</span></span>
<span data-ttu-id="fdbd8-196">Bir kullanıcı veya hizmet sorumlusuna atamak için anahtar işlem izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-196">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="fdbd8-197">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="fdbd8-197">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="fdbd8-198">Çözmeye</span><span class="sxs-lookup"><span data-stu-id="fdbd8-198">Decrypt</span></span>
- <span data-ttu-id="fdbd8-199">Şifre</span><span class="sxs-lookup"><span data-stu-id="fdbd8-199">Encrypt</span></span>
- <span data-ttu-id="fdbd8-200">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="fdbd8-200">UnwrapKey</span></span>
- <span data-ttu-id="fdbd8-201">WrapKey</span><span class="sxs-lookup"><span data-stu-id="fdbd8-201">WrapKey</span></span>
- <span data-ttu-id="fdbd8-202">Ayarlandığını</span><span class="sxs-lookup"><span data-stu-id="fdbd8-202">Verify</span></span>
- <span data-ttu-id="fdbd8-203">ISS</span><span class="sxs-lookup"><span data-stu-id="fdbd8-203">Sign</span></span>
- <span data-ttu-id="fdbd8-204">Al</span><span class="sxs-lookup"><span data-stu-id="fdbd8-204">Get</span></span>
- <span data-ttu-id="fdbd8-205">Listeniz</span><span class="sxs-lookup"><span data-stu-id="fdbd8-205">List</span></span>
- <span data-ttu-id="fdbd8-206">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="fdbd8-206">Update</span></span>
- <span data-ttu-id="fdbd8-207">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="fdbd8-207">Create</span></span>
- <span data-ttu-id="fdbd8-208">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="fdbd8-208">Import</span></span>
- <span data-ttu-id="fdbd8-209">Silme</span><span class="sxs-lookup"><span data-stu-id="fdbd8-209">Delete</span></span>
- <span data-ttu-id="fdbd8-210">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="fdbd8-210">Backup</span></span>
- <span data-ttu-id="fdbd8-211">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="fdbd8-211">Restore</span></span>
- <span data-ttu-id="fdbd8-212">Bulaşan</span><span class="sxs-lookup"><span data-stu-id="fdbd8-212">Recover</span></span>
- <span data-ttu-id="fdbd8-213">Ilmaya</span><span class="sxs-lookup"><span data-stu-id="fdbd8-213">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-214">-Permissionstogizlilikler</span><span class="sxs-lookup"><span data-stu-id="fdbd8-214">-PermissionsToSecrets</span></span>
<span data-ttu-id="fdbd8-215">Kullanıcıya veya hizmet sorumlusuna verilecek gizli işlem izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-215">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="fdbd8-216">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="fdbd8-216">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="fdbd8-217">Al</span><span class="sxs-lookup"><span data-stu-id="fdbd8-217">Get</span></span>
- <span data-ttu-id="fdbd8-218">Listeniz</span><span class="sxs-lookup"><span data-stu-id="fdbd8-218">List</span></span>
- <span data-ttu-id="fdbd8-219">Ayarlanırsa</span><span class="sxs-lookup"><span data-stu-id="fdbd8-219">Set</span></span>
- <span data-ttu-id="fdbd8-220">Silme</span><span class="sxs-lookup"><span data-stu-id="fdbd8-220">Delete</span></span>
- <span data-ttu-id="fdbd8-221">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="fdbd8-221">Backup</span></span>
- <span data-ttu-id="fdbd8-222">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="fdbd8-222">Restore</span></span>
- <span data-ttu-id="fdbd8-223">Bulaşan</span><span class="sxs-lookup"><span data-stu-id="fdbd8-223">Recover</span></span>
- <span data-ttu-id="fdbd8-224">Ilmaya</span><span class="sxs-lookup"><span data-stu-id="fdbd8-224">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-225">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="fdbd8-225">-PermissionsToStorage</span></span>
<span data-ttu-id="fdbd8-226">Kullanıcıya veya hizmet sorumlusuna vermek için yönetilen depolama hesabını ve SaS tanımlama işlem izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-226">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-227">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdbd8-227">-ResourceGroupName</span></span>
<span data-ttu-id="fdbd8-228">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-228">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-229">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fdbd8-229">-ServicePrincipalName</span></span>
<span data-ttu-id="fdbd8-230">İzin verilecek uygulamanın hizmet asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-230">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="fdbd8-231">AzureActive dizininde uygulama için kaydettirilmiş olan istemci KIMLIĞI olarak da bilinen uygulama KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-231">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="fdbd8-232">Bu parametrenin belirttiği hizmet asıl adına sahip uygulama, geçerli aboneliğinizi içeren Azure dizininde kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-232">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-233">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fdbd8-233">-UserPrincipalName</span></span>
<span data-ttu-id="fdbd8-234">İzinlerin atanacağı kullanıcının Kullanıcı asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-234">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="fdbd8-235">Bu Kullanıcı asıl adı, geçerli abonelikle ilişkilendirilmiş dizinde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-235">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-236">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fdbd8-236">-VaultName</span></span>
<span data-ttu-id="fdbd8-237">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-237">Specifies the name of a key vault.</span></span>

<span data-ttu-id="fdbd8-238">Bu cmdlet, bu parametrenin belirttiği Anahtar Kasası için erişim ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-238">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd8-239">-Onay</span><span class="sxs-lookup"><span data-stu-id="fdbd8-239">-Confirm</span></span>
<span data-ttu-id="fdbd8-240">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-240">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdbd8-241">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdbd8-241">-WhatIf</span></span>
<span data-ttu-id="fdbd8-242">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-242">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdbd8-243">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-243">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdbd8-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdbd8-244">CommonParameters</span></span>
<span data-ttu-id="fdbd8-245">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fdbd8-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdbd8-246">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdbd8-246">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdbd8-247">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fdbd8-247">INPUTS</span></span>

### <span data-ttu-id="fdbd8-248">Dize, Guid, String [], anahtar</span><span class="sxs-lookup"><span data-stu-id="fdbd8-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="fdbd8-249">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fdbd8-249">OUTPUTS</span></span>

### <span data-ttu-id="fdbd8-250">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="fdbd8-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="fdbd8-251">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fdbd8-251">NOTES</span></span>

## <span data-ttu-id="fdbd8-252">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fdbd8-252">RELATED LINKS</span></span>

[<span data-ttu-id="fdbd8-253">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="fdbd8-253">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="fdbd8-254">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fdbd8-254">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

