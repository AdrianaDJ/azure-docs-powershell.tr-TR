---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593575"
---
# <span data-ttu-id="50e09-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="50e09-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="50e09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50e09-102">SYNOPSIS</span></span>
<span data-ttu-id="50e09-103">Veri Fabrikası 'nden bir veri kümesi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50e09-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50e09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50e09-104">SYNTAX</span></span>

### <span data-ttu-id="50e09-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50e09-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="50e09-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="50e09-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="50e09-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="50e09-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="50e09-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="50e09-108">DESCRIPTION</span></span>
<span data-ttu-id="50e09-109">Remove-AzureRmDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'ndan veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50e09-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="50e09-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50e09-110">EXAMPLES</span></span>

### <span data-ttu-id="50e09-111">Örnek 1: veri kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="50e09-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="50e09-112">Bu komut, wikiadf adlı veri fabrikası 'ndan dawikiaggreg</span><span class="sxs-lookup"><span data-stu-id="50e09-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="50e09-113">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="50e09-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="50e09-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50e09-114">PARAMETERS</span></span>

### <span data-ttu-id="50e09-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="50e09-115">-Confirm</span></span>
<span data-ttu-id="50e09-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50e09-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50e09-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="50e09-117">-DataFactoryName</span></span>
<span data-ttu-id="50e09-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50e09-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="50e09-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50e09-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50e09-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50e09-120">-InputObject</span></span>
<span data-ttu-id="50e09-121">Kaldırılacak veri kümesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="50e09-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50e09-122">-Force</span><span class="sxs-lookup"><span data-stu-id="50e09-122">-Force</span></span>
<span data-ttu-id="50e09-123">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="50e09-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="50e09-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="50e09-124">-Name</span></span>
<span data-ttu-id="50e09-125">Kaldırılacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50e09-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e09-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50e09-126">-ResourceGroupName</span></span>
<span data-ttu-id="50e09-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50e09-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="50e09-128">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="50e09-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50e09-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="50e09-129">-ResourceId</span></span>
<span data-ttu-id="50e09-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="50e09-130">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50e09-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50e09-131">-WhatIf</span></span>
<span data-ttu-id="50e09-132">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="50e09-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="50e09-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50e09-133">INPUTS</span></span>

### <span data-ttu-id="50e09-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="50e09-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="50e09-135">System. String</span><span class="sxs-lookup"><span data-stu-id="50e09-135">System.String</span></span>


## <span data-ttu-id="50e09-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50e09-136">OUTPUTS</span></span>

### <span data-ttu-id="50e09-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="50e09-137">System.Object</span></span>

## <span data-ttu-id="50e09-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50e09-138">NOTES</span></span>
<span data-ttu-id="50e09-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="50e09-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="50e09-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50e09-140">RELATED LINKS</span></span>
[<span data-ttu-id="50e09-141">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="50e09-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="50e09-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="50e09-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
