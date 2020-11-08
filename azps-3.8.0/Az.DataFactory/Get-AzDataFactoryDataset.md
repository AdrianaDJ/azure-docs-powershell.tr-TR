---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: 44db491986f42bc37df250f5949690efe874c997
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104555"
---
# <span data-ttu-id="c7990-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="c7990-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="c7990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7990-102">SYNOPSIS</span></span>
<span data-ttu-id="c7990-103">Azure Veri Fabrikası 'ndaki veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c7990-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="c7990-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7990-104">SYNTAX</span></span>

### <span data-ttu-id="c7990-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c7990-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7990-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c7990-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7990-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7990-107">DESCRIPTION</span></span>
<span data-ttu-id="c7990-108">**Get-AzDataFactoryDataset** cmdlet 'ı Azure Veri Fabrikası 'ndaki veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c7990-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="c7990-109">Bir veri kümesinin adını belirtirseniz, bu cmdlet bu veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c7990-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="c7990-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c7990-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="c7990-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7990-111">EXAMPLES</span></span>

### <span data-ttu-id="c7990-112">Örnek 1: tüm veri kümeleri hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="c7990-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="c7990-113">Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c7990-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="c7990-114">Örnek 2: belirli bir veri kümesi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="c7990-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="c7990-115">Bu komut WikiADF adındaki DAWikipediaClickEvents adındaki veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c7990-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="c7990-116">Örnek 3: belirli bir veri kümesinin konumunu alma</span><span class="sxs-lookup"><span data-stu-id="c7990-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="c7990-117">Bu komut WikiADF adındaki DAWikipediaClickEvents adındaki veri kümesi için bilgi alır ve bu veri kümesiyle ilişkili **konumu** görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c7990-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="c7990-118">Alternatif olarak, **Get-Azverifactorydataset** cmdlet 'inin çıkışını bir değişkene atayın ve sonra bu değişkende depolanan veri kümesi nesnesiyle ilişkili Location özelliğini görüntülemek için nokta gösterimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c7990-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="c7990-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7990-119">PARAMETERS</span></span>

### <span data-ttu-id="c7990-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c7990-120">-DataFactory</span></span>
<span data-ttu-id="c7990-121">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7990-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c7990-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c7990-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7990-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c7990-123">-DataFactoryName</span></span>
<span data-ttu-id="c7990-124">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7990-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c7990-125">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c7990-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7990-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7990-126">-DefaultProfile</span></span>
<span data-ttu-id="c7990-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c7990-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7990-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7990-128">-Name</span></span>
<span data-ttu-id="c7990-129">Bu cmdlet 'in bilgi aldığı veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7990-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7990-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7990-130">-ResourceGroupName</span></span>
<span data-ttu-id="c7990-131">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7990-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c7990-132">Bu cmdlet, bu parametrenin belirttiği gruba ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="c7990-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7990-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7990-133">CommonParameters</span></span>
<span data-ttu-id="c7990-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7990-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7990-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7990-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7990-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7990-136">INPUTS</span></span>

### <span data-ttu-id="c7990-137">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="c7990-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="c7990-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c7990-138">System.String</span></span>

## <span data-ttu-id="c7990-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7990-139">OUTPUTS</span></span>

### <span data-ttu-id="c7990-140">Microsoft.Azure.Commands.DataFactories.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="c7990-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="c7990-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7990-141">NOTES</span></span>
* <span data-ttu-id="c7990-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="c7990-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c7990-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7990-143">RELATED LINKS</span></span>

[<span data-ttu-id="c7990-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="c7990-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="c7990-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="c7990-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


