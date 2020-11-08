---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275302"
---
# <span data-ttu-id="039a2-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="039a2-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="039a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="039a2-102">SYNOPSIS</span></span>
<span data-ttu-id="039a2-103">Anahtar Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="039a2-103">Deletes a key vault.</span></span>

## <span data-ttu-id="039a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="039a2-104">SYNTAX</span></span>

### <span data-ttu-id="039a2-105">ByAvailableVault (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="039a2-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039a2-106">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="039a2-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039a2-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="039a2-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039a2-108">Inputobjectbydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="039a2-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039a2-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="039a2-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="039a2-110">Resourceıdbydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="039a2-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="039a2-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="039a2-111">DESCRIPTION</span></span>
<span data-ttu-id="039a2-112">**Remove-Azkeykasa** cmdlet 'i, belirtilen anahtar kasası siler.</span><span class="sxs-lookup"><span data-stu-id="039a2-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="039a2-113">Bu örnekte yer alan tüm anahtarları ve gizlilikleri de siler.</span><span class="sxs-lookup"><span data-stu-id="039a2-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="039a2-114">Bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirtmek için, daha iyi performans için gerekir.</span><span class="sxs-lookup"><span data-stu-id="039a2-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="039a2-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="039a2-115">EXAMPLES</span></span>

### <span data-ttu-id="039a2-116">Örnek 1: Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="039a2-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="039a2-117">Bu komut, Contoso03Vault adındaki Anahtar Kasası 'nı geçerli aboneliğinizden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="039a2-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="039a2-118">Örnek 2: belirtilen kaynak grubundan bir Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="039a2-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="039a2-119">Bu komut, adlandırılmış kaynak grubundan Contoso03Vault adındaki Anahtar Kasası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="039a2-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="039a2-120">Kaynak grubu adını belirtmezseniz cmdlet, geçerli aboneliğinizde silinecek adlandırılmış Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="039a2-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="039a2-121">Örnek 3: yönetilen HSM 'yi kaldırma</span><span class="sxs-lookup"><span data-stu-id="039a2-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="039a2-122">Bu komut, geçerli aboneliğinizden testManagedHsm adlı yönetilen HSM 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="039a2-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="039a2-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="039a2-123">PARAMETERS</span></span>

### <span data-ttu-id="039a2-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="039a2-124">-AsJob</span></span>
<span data-ttu-id="039a2-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="039a2-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="039a2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="039a2-126">-DefaultProfile</span></span>
<span data-ttu-id="039a2-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="039a2-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="039a2-128">-Force</span><span class="sxs-lookup"><span data-stu-id="039a2-128">-Force</span></span>
<span data-ttu-id="039a2-129">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="039a2-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="039a2-130">Varsayılan olarak, bu cmdlet Anahtar Kasası silmek istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="039a2-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="039a2-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="039a2-131">-InputObject</span></span>
<span data-ttu-id="039a2-132">Silinecek anahtar kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="039a2-132">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="039a2-133">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="039a2-133">-InRemovedState</span></span>
<span data-ttu-id="039a2-134">Önceden silinmiş kasayı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="039a2-134">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="039a2-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="039a2-135">-Location</span></span>
<span data-ttu-id="039a2-136">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="039a2-136">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="039a2-137">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="039a2-137">-PassThru</span></span>
<span data-ttu-id="039a2-138">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="039a2-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="039a2-139">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="039a2-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="039a2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="039a2-140">-ResourceGroupName</span></span>
<span data-ttu-id="039a2-141">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="039a2-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="039a2-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="039a2-142">-ResourceId</span></span>
<span data-ttu-id="039a2-143">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="039a2-143">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="039a2-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="039a2-144">-VaultName</span></span>
<span data-ttu-id="039a2-145">Kaldırılacak anahtar kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="039a2-145">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="039a2-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="039a2-146">-Confirm</span></span>
<span data-ttu-id="039a2-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="039a2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="039a2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="039a2-148">-WhatIf</span></span>
<span data-ttu-id="039a2-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="039a2-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="039a2-150">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="039a2-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="039a2-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="039a2-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="039a2-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="039a2-152">CommonParameters</span></span>
<span data-ttu-id="039a2-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="039a2-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="039a2-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="039a2-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="039a2-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="039a2-155">INPUTS</span></span>

### <span data-ttu-id="039a2-156">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="039a2-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="039a2-157">System. String</span><span class="sxs-lookup"><span data-stu-id="039a2-157">System.String</span></span>

## <span data-ttu-id="039a2-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="039a2-158">OUTPUTS</span></span>

### <span data-ttu-id="039a2-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="039a2-159">System.Boolean</span></span>

## <span data-ttu-id="039a2-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="039a2-160">NOTES</span></span>

## <span data-ttu-id="039a2-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="039a2-161">RELATED LINKS</span></span>

[<span data-ttu-id="039a2-162">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="039a2-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="039a2-163">Yeni-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="039a2-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
