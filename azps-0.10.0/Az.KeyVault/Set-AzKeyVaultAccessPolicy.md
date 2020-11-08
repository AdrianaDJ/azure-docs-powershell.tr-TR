---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: a774c438f9be25dc55f48c5121031956374a2cb7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107369"
---
# <span data-ttu-id="f676f-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f676f-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="f676f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f676f-102">SYNOPSIS</span></span>
<span data-ttu-id="f676f-103">Bir Kullanıcı, uygulama veya güvenlik grubuna anahtar kasası ile işlemler gerçekleştirmesi için var olan izinleri verir veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f676f-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="f676f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f676f-104">SYNTAX</span></span>

### <span data-ttu-id="f676f-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f676f-105">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f676f-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f676f-106">ByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f676f-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="f676f-107">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f676f-108">Her bir</span><span class="sxs-lookup"><span data-stu-id="f676f-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f676f-109">Forkasa</span><span class="sxs-lookup"><span data-stu-id="f676f-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f676f-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="f676f-110">DESCRIPTION</span></span>
<span data-ttu-id="f676f-111">**Set-Azanahtarvaultaccesspolicy** cmdlet 'i, bir Kullanıcı, uygulama veya güvenlik grubuna anahtar kasası ile belirtilen işlemleri gerçekleştirecek varolan izinleri verir veya bunları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f676f-111">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="f676f-112">Diğer kullanıcıların, uygulamaların veya güvenlik gruplarının Anahtar Kasası 'ndaki izinleri değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="f676f-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="f676f-113">Güvenlik grubunun izinlerini ayarlıyorsanız, bu işlem yalnızca bu güvenlik grubundaki kullanıcıları etkiler.</span><span class="sxs-lookup"><span data-stu-id="f676f-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="f676f-114">Aşağıdaki dizinlerin tümü aynı Azure dizini olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="f676f-114">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="f676f-115">Anahtar Kasası 'nın bulunduğu Azure aboneliğinin varsayılan dizini.</span><span class="sxs-lookup"><span data-stu-id="f676f-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="f676f-116">İzinleri verdiğiniz Kullanıcı veya uygulama grubunu içeren Azure dizini.</span><span class="sxs-lookup"><span data-stu-id="f676f-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="f676f-117">Bu koşullar karşılanmazsa senaryoların örnekleri ve bu cmdlet çalışmaz:</span><span class="sxs-lookup"><span data-stu-id="f676f-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>

- <span data-ttu-id="f676f-118">Anahtar kasayı yönetmek için kullanıcıya farklı bir kuruluştan yetki verme.</span><span class="sxs-lookup"><span data-stu-id="f676f-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="f676f-119">Her kuruluşun kendi dizini vardır.</span><span class="sxs-lookup"><span data-stu-id="f676f-119">Each organization has its own directory.</span></span>
- <span data-ttu-id="f676f-120">Azure hesabınızda birden çok dizin vardır.</span><span class="sxs-lookup"><span data-stu-id="f676f-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="f676f-121">Bir uygulamayı varsayılan dizin dışında bir dizine kaydedersiniz, bu uygulamayı anahtar kasayı kullanacak şekilde yetkilenmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="f676f-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="f676f-122">Uygulama varsayılan dizinde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f676f-122">The application must be in the default directory.</span></span>

<span data-ttu-id="f676f-123">Kaynak grubu, bu cmdlet için isteğe bağlı olarak belirtilmesi durumunda daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="f676f-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="f676f-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f676f-124">EXAMPLES</span></span>

### <span data-ttu-id="f676f-125">Örnek 1: bir Anahtar Kasası için kullanıcıya izinler verme ve izinleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="f676f-125">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="f676f-126">İlk komut, Azure Active Directory 'nizde bir kullanıcıya izinler PattiFuller@contoso.com vererek, Contoso03Vault adlı bir anahtar kasası ile anahtar ve gizli işlemler gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="f676f-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="f676f-127">İkinci komut, ilk komutta verilen izinleri değiştirir PattiFuller@contoso.com , şimdi de bunları ayarlama ve silmenin yanı sıra gizli erişime izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="f676f-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="f676f-128">Bu komuttan sonra anahtar işlemlerinin izinleri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="f676f-128">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="f676f-129">*Passby* parametresi, cmdlet tarafından döndürülen güncelleştirilmiş nesneye yol.</span><span class="sxs-lookup"><span data-stu-id="f676f-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="f676f-130">Son komut, PattiFuller@contoso.com anahtar işlemler için tüm izinleri kaldırmak üzere var olan izinleri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f676f-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="f676f-131">Gizli operasyonların izinleri bu komuttan sonra değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="f676f-131">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="f676f-132">*Passby* parametresi, cmdlet tarafından döndürülen güncelleştirilmiş nesneye yol.</span><span class="sxs-lookup"><span data-stu-id="f676f-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="f676f-133">Örnek 2: gizlilikleri okumak ve yazmak için uygulama hizmeti sorumlusunun izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="f676f-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="f676f-134">Bu komut, Contoso03Vault adlı bir Anahtar Kasası için uygulama izinleri verir.</span><span class="sxs-lookup"><span data-stu-id="f676f-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="f676f-135">*ServicePrincipalName* parametresi uygulamayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-135">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="f676f-136">Uygulama, Azure Active Directory 'inizde kaydettirilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f676f-136">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="f676f-137">*ServicePrincipalName* parametresinin değeri uygulamanın hizmet asıl adı veya uygulama kimliği GUID 'si olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f676f-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="f676f-138">Bu örnekte, hizmet asıl adı belirtilir `http://payroll.contoso.com` ve komut uygulama izinlerini okuma ve yazma</span><span class="sxs-lookup"><span data-stu-id="f676f-138">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="f676f-139">Örnek 3: nesne KIMLIĞINI kullanarak bir uygulamanın izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="f676f-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="f676f-140">Bu komut, uygulama izinlerinin gizli bilgileri okuyup yazabilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="f676f-140">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="f676f-141">Bu örnekte, uygulamanın hizmet sorumlusunun nesne KIMLIĞINI kullanan uygulama belirtilir.</span><span class="sxs-lookup"><span data-stu-id="f676f-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="f676f-142">Örnek 4: Kullanıcı asıl adı için izinler verme</span><span class="sxs-lookup"><span data-stu-id="f676f-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="f676f-143">Bu komut, gizli erişim için belirtilen kullanıcı asıl adı için Get, LIST ve Permissions izinleri verir.</span><span class="sxs-lookup"><span data-stu-id="f676f-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="f676f-144">Örnek 5: Microsoft. COMPUTE kaynak sağlayıcısı tarafından bir Anahtar Kasası kasasından alınabilmesini sağlama</span><span class="sxs-lookup"><span data-stu-id="f676f-144">Example 5: Enable secrets to be retrieved from a key vault vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="f676f-145">Bu komut, Microsoft. COMPUTE kaynak sağlayıcısı tarafından Contoso03Vault Key kasasından alınan gizliliklerin izinlerini verir.</span><span class="sxs-lookup"><span data-stu-id="f676f-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="f676f-146">Örnek 6: güvenlik grubuna izinler verme</span><span class="sxs-lookup"><span data-stu-id="f676f-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="f676f-147">İlk komut, tüm Active Directory gruplarını almak için Get-AzADGroup cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f676f-147">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="f676f-148">Çıkışta, Group2 adlı **Group1** , **group2** ve **Group3** adlı 3 Grup görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="f676f-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="f676f-149">Birden çok grup aynı ada sahip olabilir ancak her zaman benzersiz bir ObjectID olabilir.</span><span class="sxs-lookup"><span data-stu-id="f676f-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="f676f-150">Aynı ada sahip birden fazla grup döndürülürse, kullanmak istediğiniz birini belirlemek için çıkışta ObjectID 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f676f-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="f676f-151">Bu komutun çıkışını Set-AzKeyVaultAccessPolicy ile Anahtar Kasası için izin vermek üzere, **myownkasa** Group2.</span><span class="sxs-lookup"><span data-stu-id="f676f-151">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="f676f-152">Bu örnek, aynı komut satırında ' Group2 ' adlı grupları satır içinde numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="f676f-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="f676f-153">Döndürülen listede ' Group2 ' adlı birden çok grup olabilir.</span><span class="sxs-lookup"><span data-stu-id="f676f-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="f676f-154">Bu örnek, ilk olarak döndürülen listedeki dizin 0 ile gösterilen ilkini seçer \[ \] .</span><span class="sxs-lookup"><span data-stu-id="f676f-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="f676f-155">Örnek 7: müşteri yönetimli kiracı anahtarına Azure Information Protection erişimi verme (BYOK)</span><span class="sxs-lookup"><span data-stu-id="f676f-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="f676f-156">Bu komut, Azure bilgi koruması 'nı bir müşteri tarafından yönetilen anahtar (kendi anahtarınızı veya "BYOK" senaryosunu) Azure Information Protection kiracı anahtarı olarak kullanacak şekilde yetkilendirir.</span><span class="sxs-lookup"><span data-stu-id="f676f-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="f676f-157">Bu komutu çalıştırdığınızda, kendi tuş kasa adınızı belirtin, ancak *servicePrincipalName* parametresini GUID **00000012-0000-0000-C000-000000000000** ile belirtmeniz ve örnekteki izinleri belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f676f-157">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="f676f-158">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f676f-158">PARAMETERS</span></span>

### <span data-ttu-id="f676f-159">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f676f-159">-ApplicationId</span></span>
<span data-ttu-id="f676f-160">.</span><span class="sxs-lookup"><span data-stu-id="f676f-160">For future use.</span></span>

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

### <span data-ttu-id="f676f-161">-Bypassobjectivseçvalidation</span><span class="sxs-lookup"><span data-stu-id="f676f-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="f676f-162">Nesnenin Azure Active Directory 'de bulunduğunu doğrulamadan bir nesne KIMLIĞI belirtmenize imkan verir.</span><span class="sxs-lookup"><span data-stu-id="f676f-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="f676f-163">Bu parametreyi yalnızca, başka bir Azure kiracısından temsilci seçilen güvenlik grubuna başvuran bir nesne KIMLIĞINE anahtar kasaya erişim vermek istiyorsanız kullanın.</span><span class="sxs-lookup"><span data-stu-id="f676f-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="f676f-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f676f-164">-DefaultProfile</span></span>
<span data-ttu-id="f676f-165">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f676f-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f676f-166">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="f676f-166">-EmailAddress</span></span>
<span data-ttu-id="f676f-167">İzin verilecek kullanıcının kullanıcı e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-167">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="f676f-168">Bu e-posta adresinin geçerli abonelikle ilişkilendirilmiş dizinde varolması ve benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f676f-168">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="f676f-169">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="f676f-169">-EnabledForDeployment</span></span>
<span data-ttu-id="f676f-170">Kaynak oluşturmada bu Anahtar Kasası, örneğin sanal makine oluştururken bu anahtar kasasına başvurulduğunda, Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f676f-170">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="f676f-171">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f676f-171">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="f676f-172">Azure disk şifreleme hizmeti 'nin, bu anahtar kasasından parolaları almasını ve anahtarları kaydırılmasını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="f676f-172">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="f676f-173">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="f676f-173">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="f676f-174">Bu anahtar kasası bir şablon dağıtımında başvuruluyorsa, Azure Resource Manager 'ın bu anahtar kasasından gizli kod almasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="f676f-174">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="f676f-175">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="f676f-175">-ObjectId</span></span>
<span data-ttu-id="f676f-176">İzin verilecek Azure Active Directory 'deki Kullanıcı veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-176">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="f676f-177">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f676f-177">-PassThru</span></span>
<span data-ttu-id="f676f-178">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f676f-178">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="f676f-179">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f676f-179">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f676f-180">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="f676f-180">-PermissionsToCertificates</span></span>
<span data-ttu-id="f676f-181">Kullanıcıya veya hizmet sorumlusuna verilecek sertifika izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-181">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="f676f-182">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="f676f-182">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="f676f-183">Al</span><span class="sxs-lookup"><span data-stu-id="f676f-183">Get</span></span>
- <span data-ttu-id="f676f-184">Listeniz</span><span class="sxs-lookup"><span data-stu-id="f676f-184">List</span></span>
- <span data-ttu-id="f676f-185">Silme</span><span class="sxs-lookup"><span data-stu-id="f676f-185">Delete</span></span>
- <span data-ttu-id="f676f-186">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="f676f-186">Create</span></span>
- <span data-ttu-id="f676f-187">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="f676f-187">Import</span></span>
- <span data-ttu-id="f676f-188">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="f676f-188">Update</span></span>
- <span data-ttu-id="f676f-189">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="f676f-189">Managecontacts</span></span>
- <span data-ttu-id="f676f-190">Jedokulu</span><span class="sxs-lookup"><span data-stu-id="f676f-190">Getissuers</span></span>
- <span data-ttu-id="f676f-191">Listissuers</span><span class="sxs-lookup"><span data-stu-id="f676f-191">Listissuers</span></span>
- <span data-ttu-id="f676f-192">Setiçilere</span><span class="sxs-lookup"><span data-stu-id="f676f-192">Setissuers</span></span>
- <span data-ttu-id="f676f-193">Deleteverenler</span><span class="sxs-lookup"><span data-stu-id="f676f-193">Deleteissuers</span></span>
- <span data-ttu-id="f676f-194">Manageverenler</span><span class="sxs-lookup"><span data-stu-id="f676f-194">Manageissuers</span></span>

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

### <span data-ttu-id="f676f-195">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="f676f-195">-PermissionsToKeys</span></span>
<span data-ttu-id="f676f-196">Bir kullanıcı veya hizmet sorumlusuna atamak için anahtar işlem izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-196">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="f676f-197">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="f676f-197">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="f676f-198">Çözmeye</span><span class="sxs-lookup"><span data-stu-id="f676f-198">Decrypt</span></span>
- <span data-ttu-id="f676f-199">Şifre</span><span class="sxs-lookup"><span data-stu-id="f676f-199">Encrypt</span></span>
- <span data-ttu-id="f676f-200">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="f676f-200">UnwrapKey</span></span>
- <span data-ttu-id="f676f-201">WrapKey</span><span class="sxs-lookup"><span data-stu-id="f676f-201">WrapKey</span></span>
- <span data-ttu-id="f676f-202">Ayarlandığını</span><span class="sxs-lookup"><span data-stu-id="f676f-202">Verify</span></span>
- <span data-ttu-id="f676f-203">ISS</span><span class="sxs-lookup"><span data-stu-id="f676f-203">Sign</span></span>
- <span data-ttu-id="f676f-204">Al</span><span class="sxs-lookup"><span data-stu-id="f676f-204">Get</span></span>
- <span data-ttu-id="f676f-205">Listeniz</span><span class="sxs-lookup"><span data-stu-id="f676f-205">List</span></span>
- <span data-ttu-id="f676f-206">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="f676f-206">Update</span></span>
- <span data-ttu-id="f676f-207">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="f676f-207">Create</span></span>
- <span data-ttu-id="f676f-208">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="f676f-208">Import</span></span>
- <span data-ttu-id="f676f-209">Silme</span><span class="sxs-lookup"><span data-stu-id="f676f-209">Delete</span></span>
- <span data-ttu-id="f676f-210">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="f676f-210">Backup</span></span>
- <span data-ttu-id="f676f-211">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="f676f-211">Restore</span></span>
- <span data-ttu-id="f676f-212">Bulaşan</span><span class="sxs-lookup"><span data-stu-id="f676f-212">Recover</span></span>
- <span data-ttu-id="f676f-213">Ilmaya</span><span class="sxs-lookup"><span data-stu-id="f676f-213">Purge</span></span>

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

### <span data-ttu-id="f676f-214">-Permissionstogizlilikler</span><span class="sxs-lookup"><span data-stu-id="f676f-214">-PermissionsToSecrets</span></span>
<span data-ttu-id="f676f-215">Kullanıcıya veya hizmet sorumlusuna verilecek gizli işlem izinleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-215">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="f676f-216">Bu parametre için kabul edilebilir değerler:</span><span class="sxs-lookup"><span data-stu-id="f676f-216">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="f676f-217">Al</span><span class="sxs-lookup"><span data-stu-id="f676f-217">Get</span></span>
- <span data-ttu-id="f676f-218">Listeniz</span><span class="sxs-lookup"><span data-stu-id="f676f-218">List</span></span>
- <span data-ttu-id="f676f-219">Ayarlanırsa</span><span class="sxs-lookup"><span data-stu-id="f676f-219">Set</span></span>
- <span data-ttu-id="f676f-220">Silme</span><span class="sxs-lookup"><span data-stu-id="f676f-220">Delete</span></span>
- <span data-ttu-id="f676f-221">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="f676f-221">Backup</span></span>
- <span data-ttu-id="f676f-222">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="f676f-222">Restore</span></span>
- <span data-ttu-id="f676f-223">Bulaşan</span><span class="sxs-lookup"><span data-stu-id="f676f-223">Recover</span></span>
- <span data-ttu-id="f676f-224">Ilmaya</span><span class="sxs-lookup"><span data-stu-id="f676f-224">Purge</span></span>

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

### <span data-ttu-id="f676f-225">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="f676f-225">-PermissionsToStorage</span></span>
<span data-ttu-id="f676f-226">Kullanıcıya veya hizmet sorumlusuna vermek için yönetilen depolama hesabını ve SaS tanımlama işlem izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-226">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

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

### <span data-ttu-id="f676f-227">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f676f-227">-ResourceGroupName</span></span>
<span data-ttu-id="f676f-228">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-228">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f676f-229">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f676f-229">-ServicePrincipalName</span></span>
<span data-ttu-id="f676f-230">İzin verilecek uygulamanın hizmet asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-230">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="f676f-231">AzureActive dizininde uygulama için kaydettirilmiş olan istemci KIMLIĞI olarak da bilinen uygulama KIMLIĞINI belirtin.</span><span class="sxs-lookup"><span data-stu-id="f676f-231">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="f676f-232">Bu parametrenin belirttiği hizmet asıl adına sahip uygulama, geçerli aboneliğinizi içeren Azure dizininde kaydedilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f676f-232">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="f676f-233">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f676f-233">-UserPrincipalName</span></span>
<span data-ttu-id="f676f-234">İzinlerin atanacağı kullanıcının Kullanıcı asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-234">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="f676f-235">Bu Kullanıcı asıl adı, geçerli abonelikle ilişkilendirilmiş dizinde bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f676f-235">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="f676f-236">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f676f-236">-VaultName</span></span>
<span data-ttu-id="f676f-237">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f676f-237">Specifies the name of a key vault.</span></span>

<span data-ttu-id="f676f-238">Bu cmdlet, bu parametrenin belirttiği Anahtar Kasası için erişim ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f676f-238">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="f676f-239">-Onay</span><span class="sxs-lookup"><span data-stu-id="f676f-239">-Confirm</span></span>
<span data-ttu-id="f676f-240">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f676f-240">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f676f-241">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f676f-241">-WhatIf</span></span>
<span data-ttu-id="f676f-242">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f676f-242">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f676f-243">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f676f-243">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f676f-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f676f-244">CommonParameters</span></span>
<span data-ttu-id="f676f-245">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f676f-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f676f-246">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f676f-246">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f676f-247">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f676f-247">INPUTS</span></span>

### <span data-ttu-id="f676f-248">Dize, Guid, String [], anahtar</span><span class="sxs-lookup"><span data-stu-id="f676f-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="f676f-249">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f676f-249">OUTPUTS</span></span>

### <span data-ttu-id="f676f-250">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="f676f-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="f676f-251">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f676f-251">NOTES</span></span>

## <span data-ttu-id="f676f-252">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f676f-252">RELATED LINKS</span></span>

[<span data-ttu-id="f676f-253">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="f676f-253">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="f676f-254">Remove-Azanahtar,</span><span class="sxs-lookup"><span data-stu-id="f676f-254">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

