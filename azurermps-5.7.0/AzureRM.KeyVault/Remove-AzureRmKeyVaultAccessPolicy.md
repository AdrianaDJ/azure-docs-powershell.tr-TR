---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591669"
---
# <span data-ttu-id="4f610-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4f610-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="4f610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f610-102">SYNOPSIS</span></span>
<span data-ttu-id="4f610-103">Bir kullanıcı veya uygulamadaki tüm izinleri anahtar kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f610-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f610-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f610-104">SYNTAX</span></span>

### <span data-ttu-id="4f610-105">ByUserPrincipalName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f610-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f610-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="4f610-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f610-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4f610-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4f610-108">Elektronik posta</span><span class="sxs-lookup"><span data-stu-id="4f610-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f610-109">Forkasa</span><span class="sxs-lookup"><span data-stu-id="4f610-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f610-110">Inputobjectbyobjectid</span><span class="sxs-lookup"><span data-stu-id="4f610-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f610-111">Inputobjectbyserviceprincipalname</span><span class="sxs-lookup"><span data-stu-id="4f610-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f610-112">Inputobjectbyuserprincipalname</span><span class="sxs-lookup"><span data-stu-id="4f610-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f610-113">Inputobjectbyemail</span><span class="sxs-lookup"><span data-stu-id="4f610-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f610-114">Inputobjectforkasa</span><span class="sxs-lookup"><span data-stu-id="4f610-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f610-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f610-115">DESCRIPTION</span></span>
<span data-ttu-id="4f610-116">**Remove-AzureRmKeyVaultAccessPolicy** cmdlet 'i bir kullanıcı veya uygulamadaki tüm izinleri veya anahtar kasasından tüm kullanıcıları ve uygulamaları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f610-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="4f610-117">Tüm izinleri kaldırsanız bile, anahtar kasası içeren Azure aboneliğinin sahibi anahtar kasasına izinler ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="4f610-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="4f610-118">Kaynak grubu, bu cmdlet için isteğe bağlı olarak belirtilmesi durumunda daha iyi performans için bunu yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="4f610-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="4f610-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f610-119">EXAMPLES</span></span>

### <span data-ttu-id="4f610-120">Örnek 1: kullanıcının izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4f610-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="4f610-121">Bu komut, kullanıcının PattiFuller@contoso.com Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f610-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="4f610-122">Örnek 2: bir uygulamanın izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4f610-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="4f610-123">Bu komut, bir uygulamanın Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f610-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="4f610-124">Bu örnek, Azure Active Directory 'de kaydedilen hizmet asıl adını kullanarak uygulamayı tanımlar http://payroll.contoso.com .</span><span class="sxs-lookup"><span data-stu-id="4f610-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="4f610-125">Örnek 3: nesne KIMLIĞINI kullanarak bir uygulamanın izinlerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4f610-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="4f610-126">Bu komut, bir uygulamanın Contoso03Vault adındaki anahtar kasasına sahip olduğu tüm izinleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f610-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="4f610-127">Bu örnekte uygulama, hizmet sorumlusunun nesne KIMLIĞINE göre tanımlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4f610-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="4f610-128">Örnek 4: Microsoft. COMPUTE kaynak sağlayıcısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4f610-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="4f610-129">Bu komut, Microsoft. COMPUTE Resource Provider 'ın Contoso03Vault 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f610-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="4f610-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f610-130">PARAMETERS</span></span>

### <span data-ttu-id="4f610-131">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4f610-131">-ApplicationId</span></span>
<span data-ttu-id="4f610-132">İzinleri kaldırılacak uygulamanın KIMLIĞINI belirtir</span><span class="sxs-lookup"><span data-stu-id="4f610-132">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="4f610-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f610-133">-DefaultProfile</span></span>
<span data-ttu-id="4f610-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4f610-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f610-135">-EpostaAdresi</span><span class="sxs-lookup"><span data-stu-id="4f610-135">-EmailAddress</span></span>
<span data-ttu-id="4f610-136">Erişimini kaldırmak istediğiniz kullanıcının kullanıcı e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f610-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f610-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="4f610-137">-EnabledForDeployment</span></span>
<span data-ttu-id="4f610-138">Belirtilmişse, bu anahtar kasasından Microsoft tarafından bu anahtar kasasından parolaların alınmasını devre dışı bırakır</span><span class="sxs-lookup"><span data-stu-id="4f610-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="4f610-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4f610-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="4f610-140">Belirtilmişse, bu anahtar kasasından Azure disk şifrelemesi ile parolaların alınmasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4f610-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="4f610-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="4f610-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="4f610-142">Belirtilmişse, şablonlarda başvurulduğunda, bu anahtar kasasından Azure Resource Manager ile gizliliklerin alınmasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4f610-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="4f610-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f610-143">-InputObject</span></span>
<span data-ttu-id="4f610-144">Anahtar kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4f610-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f610-145">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="4f610-145">-ObjectId</span></span>
<span data-ttu-id="4f610-146">İzinleri kaldırmak için Azure Active Directory 'de Kullanıcı veya hizmet sorumlusunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f610-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="4f610-147">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4f610-147">-PassThru</span></span>
<span data-ttu-id="4f610-148">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4f610-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4f610-149">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4f610-149">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f610-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f610-150">-ResourceGroupName</span></span>
<span data-ttu-id="4f610-151">Erişim ilkesi değiştirildikleri Anahtar Kasası ile ilişkili kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f610-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="4f610-152">Belirtilmemişse, bu cmdlet geçerli abonelikte Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="4f610-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f610-153">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4f610-153">-ServicePrincipalName</span></span>
<span data-ttu-id="4f610-154">İzinlerini kaldırmak istediğiniz uygulamanın hizmet asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f610-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="4f610-155">Azure Active Directory 'de uygulama için kaydettirilmiş olan uygulama KIMLIĞI 'ni belirtin.</span><span class="sxs-lookup"><span data-stu-id="4f610-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="4f610-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4f610-156">-UserPrincipalName</span></span>
<span data-ttu-id="4f610-157">Erişimini kaldırmak istediğiniz kullanıcının Kullanıcı asıl adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f610-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="4f610-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4f610-158">-VaultName</span></span>
<span data-ttu-id="4f610-159">Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f610-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="4f610-160">Bu cmdlet, bu parametrenin belirttiği Anahtar Kasası izinlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4f610-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f610-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f610-161">-Confirm</span></span>
<span data-ttu-id="4f610-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f610-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f610-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f610-163">-WhatIf</span></span>
<span data-ttu-id="4f610-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f610-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f610-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f610-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f610-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f610-166">CommonParameters</span></span>
<span data-ttu-id="4f610-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f610-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f610-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f610-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f610-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f610-169">INPUTS</span></span>

### <span data-ttu-id="4f610-170">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4f610-170">None</span></span>
<span data-ttu-id="4f610-171">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4f610-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f610-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f610-172">OUTPUTS</span></span>

### <span data-ttu-id="4f610-173">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="4f610-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="4f610-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f610-174">NOTES</span></span>

## <span data-ttu-id="4f610-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f610-175">RELATED LINKS</span></span>

[<span data-ttu-id="4f610-176">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4f610-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

