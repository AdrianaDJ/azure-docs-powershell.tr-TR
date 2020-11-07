---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937735"
---
# <span data-ttu-id="928fe-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="928fe-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="928fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="928fe-102">SYNOPSIS</span></span>
<span data-ttu-id="928fe-103">Azure Anahtar Kasası 'nın durumunu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="928fe-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="928fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="928fe-104">SYNTAX</span></span>

### <span data-ttu-id="928fe-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="928fe-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="928fe-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="928fe-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="928fe-107">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="928fe-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="928fe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="928fe-108">DESCRIPTION</span></span>
<span data-ttu-id="928fe-109">Bu cmdlet, bir Azure Anahtar Kasası 'nın durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="928fe-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="928fe-110">Lütfen bu özelliklerden bazılarının güncellenmesi geri alınamaz bir eylemdir; Örneğin, yumuşak silme etkinleştirildikten sonra artık devre dışı bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="928fe-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="928fe-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="928fe-111">EXAMPLES</span></span>

### <span data-ttu-id="928fe-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="928fe-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="928fe-113">Kaynak grubunda adı geçen anahtar kasasına yazılımdan silme özelliği etkinleştirilir `$keyVaultName` `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="928fe-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="928fe-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="928fe-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="928fe-115">Boru söz dizimini kullanarak Temizleme korumasını etkinleştirsin.</span><span class="sxs-lookup"><span data-stu-id="928fe-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="928fe-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="928fe-116">PARAMETERS</span></span>

### <span data-ttu-id="928fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928fe-117">-DefaultProfile</span></span>
<span data-ttu-id="928fe-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="928fe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928fe-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="928fe-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="928fe-120">Bu anahtar kasası için Temizleme koruması işlevini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="928fe-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="928fe-121">Etkinleştirildikten sonra devre dışı bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="928fe-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="928fe-122">Yumuşak silmenin açılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="928fe-122">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="928fe-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="928fe-123">-EnableSoftDelete</span></span>
<span data-ttu-id="928fe-124">Bu anahtar kasası için yazılımla silme işlevini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="928fe-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="928fe-125">Etkinleştirildikten sonra devre dışı bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="928fe-125">Once enabled it cannot be disabled.</span></span>

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

### <span data-ttu-id="928fe-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="928fe-126">-InputObject</span></span>
<span data-ttu-id="928fe-127">Anahtar kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="928fe-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="928fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="928fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="928fe-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="928fe-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928fe-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="928fe-130">-ResourceId</span></span>
<span data-ttu-id="928fe-131">Anahtar Kasası kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="928fe-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="928fe-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="928fe-132">-VaultName</span></span>
<span data-ttu-id="928fe-133">Anahtar Kasası adı.</span><span class="sxs-lookup"><span data-stu-id="928fe-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928fe-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="928fe-134">-Confirm</span></span>
<span data-ttu-id="928fe-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="928fe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="928fe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="928fe-136">-WhatIf</span></span>
<span data-ttu-id="928fe-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="928fe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="928fe-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="928fe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="928fe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928fe-139">CommonParameters</span></span>
<span data-ttu-id="928fe-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="928fe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928fe-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="928fe-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928fe-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="928fe-142">INPUTS</span></span>

### <span data-ttu-id="928fe-143">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="928fe-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="928fe-144">System. String</span><span class="sxs-lookup"><span data-stu-id="928fe-144">System.String</span></span>

## <span data-ttu-id="928fe-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="928fe-145">OUTPUTS</span></span>

### <span data-ttu-id="928fe-146">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="928fe-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="928fe-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="928fe-147">NOTES</span></span>

## <span data-ttu-id="928fe-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="928fe-148">RELATED LINKS</span></span>
