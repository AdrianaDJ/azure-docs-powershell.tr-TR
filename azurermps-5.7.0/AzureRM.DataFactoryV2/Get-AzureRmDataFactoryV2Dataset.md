---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 171431e317b9edbafe83f7c0c836f5543fcbd65d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590506"
---
# <span data-ttu-id="527e3-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="527e3-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="527e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="527e3-102">SYNOPSIS</span></span>
<span data-ttu-id="527e3-103">Veri Fabrikası 'nde veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="527e3-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="527e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="527e3-104">SYNTAX</span></span>

### <span data-ttu-id="527e3-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="527e3-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="527e3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="527e3-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="527e3-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="527e3-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Dataset -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="527e3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="527e3-108">DESCRIPTION</span></span>
<span data-ttu-id="527e3-109">Get-AzureRmDataFactoryV2Dataset cmdlet 'i Azure Veri Fabrikası 'ndaki veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="527e3-109">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="527e3-110">Bir veri kümesinin adını belirtirseniz, bu cmdlet bu veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="527e3-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="527e3-111">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="527e3-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="527e3-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="527e3-112">EXAMPLES</span></span>

### <span data-ttu-id="527e3-113">Örnek 1: tüm veri kümeleri hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="527e3-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="527e3-114">Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="527e3-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="527e3-115">Örnek 2: belirli bir veri kümesi hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="527e3-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="527e3-116">Bu komut WikiADF adındaki DAWikipediaClickEvents adındaki veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="527e3-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="527e3-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="527e3-117">PARAMETERS</span></span>

### <span data-ttu-id="527e3-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="527e3-118">-DataFactory</span></span>
<span data-ttu-id="527e3-119">PSDataFactory nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="527e3-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="527e3-120">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="527e3-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="527e3-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="527e3-121">-DataFactoryName</span></span>
<span data-ttu-id="527e3-122">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="527e3-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="527e3-123">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="527e3-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="527e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="527e3-124">-DefaultProfile</span></span>
<span data-ttu-id="527e3-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="527e3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="527e3-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="527e3-126">-Name</span></span>
<span data-ttu-id="527e3-127">Bilgi alınacak veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="527e3-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="527e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="527e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="527e3-129">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="527e3-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="527e3-130">Bu cmdlet, bu parametrenin belirttiği gruba ait veri kümelerini alır.</span><span class="sxs-lookup"><span data-stu-id="527e3-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="527e3-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="527e3-131">-ResourceId</span></span>
<span data-ttu-id="527e3-132">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="527e3-132">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="527e3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="527e3-133">CommonParameters</span></span>
<span data-ttu-id="527e3-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="527e3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="527e3-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="527e3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="527e3-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="527e3-136">INPUTS</span></span>

### <span data-ttu-id="527e3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="527e3-137">System.String</span></span>
<span data-ttu-id="527e3-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="527e3-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="527e3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="527e3-139">OUTPUTS</span></span>

### <span data-ttu-id="527e3-140">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="527e3-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="527e3-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDatakümesi</span><span class="sxs-lookup"><span data-stu-id="527e3-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="527e3-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="527e3-142">NOTES</span></span>
<span data-ttu-id="527e3-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="527e3-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="527e3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="527e3-144">RELATED LINKS</span></span>

[<span data-ttu-id="527e3-145">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="527e3-145">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="527e3-146">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="527e3-146">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
