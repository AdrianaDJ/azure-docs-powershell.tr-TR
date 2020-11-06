---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 343cea9eb3d708e802d1e06f555fd13ab1cd8c13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590223"
---
# <span data-ttu-id="9e7d5-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9e7d5-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="9e7d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7d5-103">Bir kullanıcı veya uygulamadaki tüm izinleri anahtar kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e7d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e7d5-104">SYNTAX</span></span>

### <span data-ttu-id="9e7d5-105">ByUserPrincipalName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e7d5-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="9e7d5-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9e7d5-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-108">Elektronik posta</span><span class="sxs-lookup"><span data-stu-id="9e7d5-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-109">Forkasa</span><span class="sxs-lookup"><span data-stu-id="9e7d5-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-110">Inputobjectbyobjectid</span><span class="sxs-lookup"><span data-stu-id="9e7d5-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-111">Inputobjectbyserviceprincipalname</span><span class="sxs-lookup"><span data-stu-id="9e7d5-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-112">Inputobjectbyuserprincipalname</span><span class="sxs-lookup"><span data-stu-id="9e7d5-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-113">Inputobjectbyemail</span><span class="sxs-lookup"><span data-stu-id="9e7d5-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-114">Inputobjectforkasa</span><span class="sxs-lookup"><span data-stu-id="9e7d5-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-115">Resourceıdbyobjectid</span><span class="sxs-lookup"><span data-stu-id="9e7d5-115">ResourceIdByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-116">Resourceıdbyserviceprincipalname</span><span class="sxs-lookup"><span data-stu-id="9e7d5-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-117">Resourceıdbyuserprincipalname</span><span class="sxs-lookup"><span data-stu-id="9e7d5-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-118">Resourceıdbyemail</span><span class="sxs-lookup"><span data-stu-id="9e7d5-118">ResourceIdByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e7d5-119">KaynakKimliği</span><span class="sxs-lookup"><span data-stu-id="9e7d5-119">ResourceIdForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e7d5-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e7d5-120">DESCRIPTION</span></span>
<span data-ttu-id="9e7d5-121">**Remove-AzureRmKeyVaultAccessPolicy** cmdlet 'i bir kullanıcı veya uygulamadaki tüm izinleri veya anahtar kasasından tüm kullanıcıları ve uygulamaları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-121">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="9e7d5-122">Tüm izinleri kaldırsanız bile, anahtar kasası içeren Azure aboneliğinin sahibi anahtar kasasına izinler ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="9e7d5-123">Kaynak grubu, bu cmdlet için isteğe bağlı olarak belirtilmesi durumunda daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="9e7d5-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e7d5-124">EXAMPLES</span></span>

### <span data-ttu-id="9e7d5-125">Örnek 1: kullanıcının izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="9e7d5-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="9e7d5-126">Bu komut, kullanıcının PattiFuller@contoso.com Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="9e7d5-127">Eğer-pass-belirtildiğinde, Keykasa nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="9e7d5-128">Örnek 2: bir uygulamanın izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="9e7d5-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="9e7d5-129">Bu komut, bir uygulamanın Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="9e7d5-130">Bu örnek, Azure Active Directory 'de kaydedilen hizmet asıl adını kullanarak uygulamayı tanımlar http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="9e7d5-130">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="9e7d5-131">Örnek 3: nesne KIMLIĞINI kullanarak bir uygulamanın izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="9e7d5-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="9e7d5-132">Bu komut, bir uygulamanın Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="9e7d5-133">Bu örnekte uygulama, hizmet sorumlusunun nesne KIMLIĞINE göre tanımlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="9e7d5-134">Örnek 4: Microsoft. COMPUTE kaynak sağlayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="9e7d5-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="9e7d5-135">Bu komut, Microsoft. COMPUTE Resource Provider 'ın Contoso03Vault 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="9e7d5-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e7d5-136">PARAMETERS</span></span>

### <span data-ttu-id="9e7d5-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9e7d5-137">-ApplicationId</span></span>
<span data-ttu-id="9e7d5-138">İzinleri kaldırılacak uygulamanın KIMLIĞINI belirtir</span><span class="sxs-lookup"><span data-stu-id="9e7d5-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="9e7d5-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7d5-139">-DefaultProfile</span></span>
<span data-ttu-id="9e7d5-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9e7d5-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7d5-141">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="9e7d5-141">-EmailAddress</span></span>
<span data-ttu-id="9e7d5-142">Erişimini kaldırmak istediğiniz kullanıcının kullanıcı e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7d5-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="9e7d5-143">-EnabledForDeployment</span></span>
<span data-ttu-id="9e7d5-144">Belirtilmişse, bu anahtar kasasından Microsoft tarafından bu anahtar kasasından parolaların alınmasını devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="9e7d5-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="9e7d5-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9e7d5-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="9e7d5-146">Belirtilmişse, bu anahtar kasasından Azure disk şifrelemesi ile parolaların alınmasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="9e7d5-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="9e7d5-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="9e7d5-148">Belirtilmişse, şablonlarda başvurulduğunda, bu anahtar kasasından Azure Resource Manager ile gizliliklerin alınmasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="9e7d5-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e7d5-149">-InputObject</span></span>
<span data-ttu-id="9e7d5-150">Anahtar kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e7d5-151">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="9e7d5-151">-ObjectId</span></span>
<span data-ttu-id="9e7d5-152">İzinleri kaldırmak için Azure Active Directory 'de Kullanıcı veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="9e7d5-153">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9e7d5-153">-PassThru</span></span>
<span data-ttu-id="9e7d5-154">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e7d5-155">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9e7d5-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e7d5-156">-ResourceGroupName</span></span>
<span data-ttu-id="9e7d5-157">Erişim ilkesi değiştirildikleri Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="9e7d5-158">Belirtilmemişse, bu cmdlet geçerli abonelikte Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7d5-159">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9e7d5-159">-ResourceId</span></span>
<span data-ttu-id="9e7d5-160">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e7d5-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9e7d5-161">-ServicePrincipalName</span></span>
<span data-ttu-id="9e7d5-162">İzinlerini kaldırmak istediğiniz uygulamanın hizmet asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="9e7d5-163">Azure Active Directory 'de uygulama için kaydettirilmiş olan uygulama KIMLIĞI 'ni belirtin.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="9e7d5-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9e7d5-164">-UserPrincipalName</span></span>
<span data-ttu-id="9e7d5-165">Erişimini kaldırmak istediğiniz kullanıcının Kullanıcı asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="9e7d5-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9e7d5-166">-VaultName</span></span>
<span data-ttu-id="9e7d5-167">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="9e7d5-168">Bu cmdlet, bu parametrenin belirttiği Anahtar Kasası izinlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e7d5-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="9e7d5-169">-Confirm</span></span>
<span data-ttu-id="9e7d5-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e7d5-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e7d5-171">-WhatIf</span></span>
<span data-ttu-id="9e7d5-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e7d5-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e7d5-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7d5-174">CommonParameters</span></span>
<span data-ttu-id="9e7d5-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e7d5-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7d5-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e7d5-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7d5-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e7d5-177">INPUTS</span></span>

### <span data-ttu-id="9e7d5-178">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="9e7d5-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="9e7d5-179">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9e7d5-179">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9e7d5-180">System. String</span><span class="sxs-lookup"><span data-stu-id="9e7d5-180">System.String</span></span>

## <span data-ttu-id="9e7d5-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e7d5-181">OUTPUTS</span></span>

### <span data-ttu-id="9e7d5-182">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="9e7d5-182">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9e7d5-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e7d5-183">NOTES</span></span>

## <span data-ttu-id="9e7d5-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e7d5-184">RELATED LINKS</span></span>

[<span data-ttu-id="9e7d5-185">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9e7d5-185">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

