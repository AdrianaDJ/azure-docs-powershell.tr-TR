---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: 712aa1012269c6207b078fefa3a04a46bea4c573
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109915"
---
# <span data-ttu-id="36e83-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="36e83-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="36e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36e83-102">SYNOPSIS</span></span>
<span data-ttu-id="36e83-103">Veri kümesini çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36e83-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="36e83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36e83-104">SYNTAX</span></span>

### <span data-ttu-id="36e83-105">RemoveByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36e83-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36e83-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="36e83-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36e83-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="36e83-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36e83-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="36e83-108">DESCRIPTION</span></span>
<span data-ttu-id="36e83-109">**Remove-AzSynapseDataset** cmdlet 'i çalışma alanından bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36e83-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="36e83-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36e83-110">EXAMPLES</span></span>

### <span data-ttu-id="36e83-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36e83-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="36e83-112">Bu komut, ContosoDataset adlı veri kümesini ContosoWorkspace adlı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36e83-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="36e83-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36e83-113">PARAMETERS</span></span>

### <span data-ttu-id="36e83-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="36e83-114">-AsJob</span></span>
<span data-ttu-id="36e83-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="36e83-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36e83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e83-116">-DefaultProfile</span></span>
<span data-ttu-id="36e83-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36e83-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e83-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36e83-118">-InputObject</span></span>
<span data-ttu-id="36e83-119">Veri kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="36e83-119">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36e83-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="36e83-120">-Name</span></span>
<span data-ttu-id="36e83-121">Veri kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="36e83-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e83-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="36e83-122">-PassThru</span></span>
<span data-ttu-id="36e83-123">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="36e83-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="36e83-124">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="36e83-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="36e83-125">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="36e83-125">-WorkspaceName</span></span>
<span data-ttu-id="36e83-126">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="36e83-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36e83-127">-</span><span class="sxs-lookup"><span data-stu-id="36e83-127">-WorkspaceObject</span></span>
<span data-ttu-id="36e83-128">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="36e83-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36e83-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="36e83-129">-Confirm</span></span>
<span data-ttu-id="36e83-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36e83-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36e83-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36e83-131">-WhatIf</span></span>
<span data-ttu-id="36e83-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36e83-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36e83-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36e83-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36e83-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e83-134">CommonParameters</span></span>
<span data-ttu-id="36e83-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36e83-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e83-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="36e83-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e83-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36e83-137">INPUTS</span></span>

### <span data-ttu-id="36e83-138">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="36e83-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="36e83-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="36e83-139">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="36e83-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36e83-140">OUTPUTS</span></span>

### <span data-ttu-id="36e83-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36e83-141">System.Boolean</span></span>

## <span data-ttu-id="36e83-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36e83-142">NOTES</span></span>

## <span data-ttu-id="36e83-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36e83-143">RELATED LINKS</span></span>
