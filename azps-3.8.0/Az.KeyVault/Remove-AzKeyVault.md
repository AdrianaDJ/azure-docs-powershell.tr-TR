---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 32060f2d9d468669f963f653f335729ca6c25761
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104880"
---
# <span data-ttu-id="3f730-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3f730-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="3f730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f730-102">SYNOPSIS</span></span>
<span data-ttu-id="3f730-103">Anahtar Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="3f730-103">Deletes a key vault.</span></span>

## <span data-ttu-id="3f730-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f730-104">SYNTAX</span></span>

### <span data-ttu-id="3f730-105">ByAvailableVault (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3f730-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f730-106">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="3f730-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f730-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="3f730-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f730-108">Inputobjectbydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="3f730-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f730-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="3f730-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f730-110">Resourceıdbydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="3f730-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f730-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f730-111">DESCRIPTION</span></span>
<span data-ttu-id="3f730-112">**Remove-Azkeykasa** cmdlet 'i, belirtilen anahtar kasası siler.</span><span class="sxs-lookup"><span data-stu-id="3f730-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="3f730-113">Bu örnekte yer alan tüm anahtarları ve gizlilikleri de siler.</span><span class="sxs-lookup"><span data-stu-id="3f730-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="3f730-114">Bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirtmek için, daha iyi performans için gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f730-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="3f730-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f730-115">EXAMPLES</span></span>

### <span data-ttu-id="3f730-116">Örnek 1: Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="3f730-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="3f730-117">Bu komut, Contoso03Vault adındaki Anahtar Kasası 'nı geçerli aboneliğinizden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f730-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="3f730-118">Örnek 2: belirtilen kaynak grubundan bir Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="3f730-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="3f730-119">Bu komut, adlandırılmış kaynak grubundan Contoso03Vault adındaki Anahtar Kasası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3f730-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="3f730-120">Kaynak grubu adını belirtmezseniz cmdlet, geçerli aboneliğinizde silinecek adlandırılmış Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="3f730-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="3f730-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f730-121">PARAMETERS</span></span>

### <span data-ttu-id="3f730-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="3f730-122">-AsJob</span></span>
<span data-ttu-id="3f730-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3f730-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f730-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f730-124">-DefaultProfile</span></span>
<span data-ttu-id="3f730-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3f730-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f730-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3f730-126">-Force</span></span>
<span data-ttu-id="3f730-127">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f730-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="3f730-128">Varsayılan olarak, bu cmdlet Anahtar Kasası silmek istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f730-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="3f730-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f730-129">-InputObject</span></span>
<span data-ttu-id="3f730-130">Silinecek anahtar kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3f730-130">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f730-131">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="3f730-131">-InRemovedState</span></span>
<span data-ttu-id="3f730-132">Önceden silinmiş kasayı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="3f730-132">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f730-133">-Konum</span><span class="sxs-lookup"><span data-stu-id="3f730-133">-Location</span></span>
<span data-ttu-id="3f730-134">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="3f730-134">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f730-135">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3f730-135">-PassThru</span></span>
<span data-ttu-id="3f730-136">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="3f730-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="3f730-137">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f730-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3f730-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f730-138">-ResourceGroupName</span></span>
<span data-ttu-id="3f730-139">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f730-139">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f730-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3f730-140">-ResourceId</span></span>
<span data-ttu-id="3f730-141">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3f730-141">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f730-142">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3f730-142">-VaultName</span></span>
<span data-ttu-id="3f730-143">Kaldırılacak anahtar kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f730-143">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f730-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f730-144">-Confirm</span></span>
<span data-ttu-id="3f730-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f730-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f730-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f730-146">-WhatIf</span></span>
<span data-ttu-id="3f730-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f730-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f730-148">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f730-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f730-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f730-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f730-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f730-150">CommonParameters</span></span>
<span data-ttu-id="3f730-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f730-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f730-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3f730-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f730-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f730-153">INPUTS</span></span>

### <span data-ttu-id="3f730-154">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="3f730-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3f730-155">System. String</span><span class="sxs-lookup"><span data-stu-id="3f730-155">System.String</span></span>

## <span data-ttu-id="3f730-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f730-156">OUTPUTS</span></span>

### <span data-ttu-id="3f730-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3f730-157">System.Boolean</span></span>

## <span data-ttu-id="3f730-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f730-158">NOTES</span></span>

## <span data-ttu-id="3f730-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f730-159">RELATED LINKS</span></span>

[<span data-ttu-id="3f730-160">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="3f730-160">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="3f730-161">Yeni-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="3f730-161">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
