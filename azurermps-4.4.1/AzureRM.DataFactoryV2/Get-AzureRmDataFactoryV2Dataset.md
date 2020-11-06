---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594753"
---
# <span data-ttu-id="312af-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="312af-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="312af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="312af-102">SYNOPSIS</span></span>
<span data-ttu-id="312af-103">Veri Fabrikası 'nde veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="312af-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="312af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="312af-104">SYNTAX</span></span>

### <span data-ttu-id="312af-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="312af-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="312af-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="312af-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="312af-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="312af-107">DESCRIPTION</span></span>
<span data-ttu-id="312af-108">Get-AzureRmDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'ndaki veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="312af-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="312af-109">Bir veri kümesinin adını belirtirseniz, bu cmdlet bu veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="312af-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="312af-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="312af-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="312af-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="312af-111">EXAMPLES</span></span>

### <span data-ttu-id="312af-112">Örnek 1: tüm veri kümeleri hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="312af-112">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="312af-113">Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="312af-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="312af-114">Örnek 2: belirli bir veri kümesi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="312af-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="312af-115">Bu komut WikiADF adındaki DAWikipediaClickEvents adındaki veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="312af-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="312af-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="312af-116">PARAMETERS</span></span>

### <span data-ttu-id="312af-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="312af-117">-DataFactory</span></span>
<span data-ttu-id="312af-118">PSDataFactory nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="312af-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="312af-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="312af-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="312af-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="312af-120">-DataFactoryName</span></span>
<span data-ttu-id="312af-121">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="312af-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="312af-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="312af-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="312af-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="312af-123">-Name</span></span>
<span data-ttu-id="312af-124">Bilgi alınacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="312af-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="312af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="312af-125">-ResourceGroupName</span></span>
<span data-ttu-id="312af-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="312af-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="312af-127">Bu cmdlet, bu parametrenin belirttiği gruba ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="312af-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="312af-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="312af-128">INPUTS</span></span>

### <span data-ttu-id="312af-129">System. String</span><span class="sxs-lookup"><span data-stu-id="312af-129">System.String</span></span>
<span data-ttu-id="312af-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="312af-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="312af-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="312af-131">OUTPUTS</span></span>

### <span data-ttu-id="312af-132">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="312af-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="312af-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="312af-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="312af-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="312af-134">NOTES</span></span>
<span data-ttu-id="312af-135">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="312af-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="312af-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="312af-136">RELATED LINKS</span></span>
[<span data-ttu-id="312af-137">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="312af-137">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="312af-138">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="312af-138">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
