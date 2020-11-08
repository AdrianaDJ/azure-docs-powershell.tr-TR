---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e084894c26cee1a619f418437986593fe86876bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109593"
---
# <span data-ttu-id="ed292-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ed292-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="ed292-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed292-102">SYNOPSIS</span></span>
<span data-ttu-id="ed292-103">Bir kullanıcı veya uygulamadaki tüm izinleri anahtar kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed292-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="ed292-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed292-104">SYNTAX</span></span>

### <span data-ttu-id="ed292-105">ByUserPrincipalName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed292-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="ed292-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed292-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ed292-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed292-108">Elektronik posta</span><span class="sxs-lookup"><span data-stu-id="ed292-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-109">Forkasa</span><span class="sxs-lookup"><span data-stu-id="ed292-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-110">Inputobjectbyobjectid</span><span class="sxs-lookup"><span data-stu-id="ed292-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-111">Inputobjectbyserviceprincipalname</span><span class="sxs-lookup"><span data-stu-id="ed292-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-112">Inputobjectbyuserprincipalname</span><span class="sxs-lookup"><span data-stu-id="ed292-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-113">Inputobjectbyemail</span><span class="sxs-lookup"><span data-stu-id="ed292-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-114">Inputobjectforkasa</span><span class="sxs-lookup"><span data-stu-id="ed292-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-115">Resourceıdbyobjectid</span><span class="sxs-lookup"><span data-stu-id="ed292-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-116">Resourceıdbyserviceprincipalname</span><span class="sxs-lookup"><span data-stu-id="ed292-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-117">Resourceıdbyuserprincipalname</span><span class="sxs-lookup"><span data-stu-id="ed292-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-118">Resourceıdbyemail</span><span class="sxs-lookup"><span data-stu-id="ed292-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed292-119">KaynakKimliği</span><span class="sxs-lookup"><span data-stu-id="ed292-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed292-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed292-120">DESCRIPTION</span></span>
<span data-ttu-id="ed292-121">**Remove-Azanahtar,** bir kullanıcı veya uygulamadaki tüm izinleri veya anahtar kasasından tüm kullanıcıları ve uygulamaları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed292-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="ed292-122">Tüm izinleri kaldırsanız bile, anahtar kasası içeren Azure aboneliğinin sahibi anahtar kasasına izinler ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="ed292-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="ed292-123">Kaynak grubu, bu cmdlet için isteğe bağlı olarak belirtilmesi durumunda daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="ed292-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="ed292-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed292-124">EXAMPLES</span></span>

### <span data-ttu-id="ed292-125">Örnek 1: kullanıcının izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ed292-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

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

<span data-ttu-id="ed292-126">Bu komut, kullanıcının PattiFuller@contoso.com Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed292-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="ed292-127">Eğer-pass-belirtildiğinde, Keykasa nesnesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="ed292-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="ed292-128">Örnek 2: bir uygulamanın izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ed292-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="ed292-129">Bu komut, bir uygulamanın Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed292-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="ed292-130">Bu örnek, Azure Active Directory 'de kaydedilen hizmet asıl adını kullanarak uygulamayı tanımlar http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="ed292-130">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="ed292-131">Örnek 3: nesne KIMLIĞINI kullanarak bir uygulamanın izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="ed292-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="ed292-132">Bu komut, bir uygulamanın Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed292-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="ed292-133">Bu örnekte uygulama, hizmet sorumlusunun nesne KIMLIĞINE göre tanımlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ed292-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="ed292-134">Örnek 4: Microsoft. COMPUTE kaynak sağlayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ed292-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="ed292-135">Bu komut, Microsoft. COMPUTE Resource Provider 'ın Contoso03Vault 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed292-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="ed292-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed292-136">PARAMETERS</span></span>

### <span data-ttu-id="ed292-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ed292-137">-ApplicationId</span></span>
<span data-ttu-id="ed292-138">İzinleri kaldırılacak uygulamanın KIMLIĞINI belirtir</span><span class="sxs-lookup"><span data-stu-id="ed292-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="ed292-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed292-139">-DefaultProfile</span></span>
<span data-ttu-id="ed292-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ed292-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed292-141">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="ed292-141">-EmailAddress</span></span>
<span data-ttu-id="ed292-142">Erişimini kaldırmak istediğiniz kullanıcının kullanıcı e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed292-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="ed292-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="ed292-143">-EnabledForDeployment</span></span>
<span data-ttu-id="ed292-144">Belirtilmişse, bu anahtar kasasından Microsoft tarafından bu anahtar kasasından parolaların alınmasını devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="ed292-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="ed292-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ed292-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="ed292-146">Belirtilmişse, bu anahtar kasasından Azure disk şifrelemesi ile parolaların alınmasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ed292-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="ed292-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="ed292-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="ed292-148">Belirtilmişse, şablonlarda başvurulduğunda, bu anahtar kasasından Azure Resource Manager ile gizliliklerin alınmasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ed292-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="ed292-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed292-149">-InputObject</span></span>
<span data-ttu-id="ed292-150">Anahtar kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ed292-150">Key Vault object.</span></span>

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

### <span data-ttu-id="ed292-151">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="ed292-151">-ObjectId</span></span>
<span data-ttu-id="ed292-152">İzinleri kaldırmak için Azure Active Directory 'de Kullanıcı veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed292-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="ed292-153">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ed292-153">-PassThru</span></span>
<span data-ttu-id="ed292-154">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ed292-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed292-155">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ed292-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed292-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed292-156">-ResourceGroupName</span></span>
<span data-ttu-id="ed292-157">Erişim ilkesi değiştirildikleri Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed292-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="ed292-158">Belirtilmemişse, bu cmdlet geçerli abonelikte Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="ed292-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="ed292-159">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ed292-159">-ResourceId</span></span>
<span data-ttu-id="ed292-160">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ed292-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="ed292-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ed292-161">-ServicePrincipalName</span></span>
<span data-ttu-id="ed292-162">İzinlerini kaldırmak istediğiniz uygulamanın hizmet asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed292-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="ed292-163">Azure Active Directory 'de uygulama için kaydettirilmiş olan uygulama KIMLIĞI 'ni belirtin.</span><span class="sxs-lookup"><span data-stu-id="ed292-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="ed292-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ed292-164">-UserPrincipalName</span></span>
<span data-ttu-id="ed292-165">Erişimini kaldırmak istediğiniz kullanıcının Kullanıcı asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed292-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="ed292-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ed292-166">-VaultName</span></span>
<span data-ttu-id="ed292-167">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed292-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="ed292-168">Bu cmdlet, bu parametrenin belirttiği Anahtar Kasası izinlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed292-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="ed292-169">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed292-169">-Confirm</span></span>
<span data-ttu-id="ed292-170">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed292-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed292-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed292-171">-WhatIf</span></span>
<span data-ttu-id="ed292-172">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed292-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed292-173">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed292-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed292-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed292-174">CommonParameters</span></span>
<span data-ttu-id="ed292-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed292-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed292-176">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed292-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed292-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed292-177">INPUTS</span></span>

### <span data-ttu-id="ed292-178">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="ed292-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ed292-179">System. String</span><span class="sxs-lookup"><span data-stu-id="ed292-179">System.String</span></span>

## <span data-ttu-id="ed292-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed292-180">OUTPUTS</span></span>

### <span data-ttu-id="ed292-181">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="ed292-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ed292-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed292-182">NOTES</span></span>

## <span data-ttu-id="ed292-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed292-183">RELATED LINKS</span></span>

[<span data-ttu-id="ed292-184">Set-Azanahtarvaultaccesspolicy</span><span class="sxs-lookup"><span data-stu-id="ed292-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

