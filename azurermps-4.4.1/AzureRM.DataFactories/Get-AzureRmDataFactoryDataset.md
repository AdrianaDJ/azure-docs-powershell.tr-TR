---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 0898b65c0a124b278d0878ac1749e955011e1dab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586912"
---
# <span data-ttu-id="84733-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="84733-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="84733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84733-102">SYNOPSIS</span></span>
<span data-ttu-id="84733-103">Azure Veri Fabrikası 'ndaki veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="84733-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84733-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84733-104">SYNTAX</span></span>

### <span data-ttu-id="84733-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84733-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84733-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="84733-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84733-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="84733-107">DESCRIPTION</span></span>
<span data-ttu-id="84733-108">**Get-AzureRmDataFactoryDataset** cmdlet 'ı Azure Veri Fabrikası 'ndaki veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="84733-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="84733-109">Bir veri kümesinin adını belirtirseniz, bu cmdlet bu veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="84733-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="84733-110">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="84733-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="84733-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84733-111">EXAMPLES</span></span>

### <span data-ttu-id="84733-112">Örnek 1: tüm veri kümeleri hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="84733-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
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

<span data-ttu-id="84733-113">Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="84733-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="84733-114">Örnek 2: belirli bir veri kümesi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="84733-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="84733-115">Bu komut WikiADF adındaki DAWikipediaClickEvents adındaki veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="84733-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="84733-116">Örnek 3: belirli bir veri kümesinin konumunu alma</span><span class="sxs-lookup"><span data-stu-id="84733-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="84733-117">Bu komut WikiADF adındaki DAWikipediaClickEvents adındaki veri kümesi için bilgi alır ve bu veri kümesiyle ilişkili **konumu** görüntülemek için standart nokta gösterimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="84733-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="84733-118">Alternatif olarak, **Get-AzureRmDataFactoryDataset** cmdlet 'inin çıkışını bir değişkene atayın ve sonra bu değişkende depolanan veri kümesi nesnesiyle ilişkili konum özelliğini görüntülemek için nokta gösterimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="84733-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="84733-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84733-119">PARAMETERS</span></span>

### <span data-ttu-id="84733-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="84733-120">-DataFactory</span></span>
<span data-ttu-id="84733-121">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84733-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="84733-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="84733-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="84733-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="84733-123">-DataFactoryName</span></span>
<span data-ttu-id="84733-124">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84733-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="84733-125">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="84733-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="84733-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="84733-126">-Name</span></span>
<span data-ttu-id="84733-127">Bu cmdlet 'in bilgi aldığı veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84733-127">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="84733-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84733-128">-ResourceGroupName</span></span>
<span data-ttu-id="84733-129">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84733-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="84733-130">Bu cmdlet, bu parametrenin belirttiği gruba ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="84733-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="84733-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84733-131">-DefaultProfile</span></span>
<span data-ttu-id="84733-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84733-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84733-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84733-133">CommonParameters</span></span>
<span data-ttu-id="84733-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84733-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84733-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84733-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84733-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84733-136">INPUTS</span></span>

## <span data-ttu-id="84733-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84733-137">OUTPUTS</span></span>

### <span data-ttu-id="84733-138">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDatakümesi, Microsoft. Windowsazve. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="84733-138">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="84733-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84733-139">NOTES</span></span>
* <span data-ttu-id="84733-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="84733-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="84733-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84733-141">RELATED LINKS</span></span>

[<span data-ttu-id="84733-142">Yeni-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="84733-142">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="84733-143">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="84733-143">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


