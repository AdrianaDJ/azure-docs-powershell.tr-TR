---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: b3524f0886c5c433c6ec36d907126e6ca04828de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752552"
---
# <span data-ttu-id="0d82c-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="0d82c-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="0d82c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d82c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d82c-103">Azure Veri Fabrikası 'nde veri kümesinin veri dilimi için çalışır.</span><span class="sxs-lookup"><span data-stu-id="0d82c-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="0d82c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d82c-104">SYNTAX</span></span>

### <span data-ttu-id="0d82c-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d82c-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d82c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0d82c-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d82c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d82c-107">DESCRIPTION</span></span>
<span data-ttu-id="0d82c-108">**Get-AzDataFactoryRun** cmdlet 'ı, Azure Veri Fabrikası 'nde veri kümesinin veri Slice 'ın çalışmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="0d82c-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="0d82c-109">Veri Fabrikası içindeki veri kümesi, zaman ekseninin diliminden oluşur.</span><span class="sxs-lookup"><span data-stu-id="0d82c-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="0d82c-110">Dilimin genişliği, saatlik veya günlük zamanlama tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="0d82c-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="0d82c-111">Bir çalışma, bir dilim için bir işlem birimidir.</span><span class="sxs-lookup"><span data-stu-id="0d82c-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="0d82c-112">Bir veya daha fazla çalışma süresi dışında bir dilim için bir veya daha fazla çalışan olabilir</span><span class="sxs-lookup"><span data-stu-id="0d82c-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="0d82c-113">Dilim, başlangıç saatine göre tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="0d82c-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="0d82c-114">Bir dilimin başlangıç saatini almak için Get-AzDataFactorySlice cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0d82c-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="0d82c-115">Örneğin, aşağıdaki dilim için bir çalıştırma elde etmek için, 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="0d82c-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="0d82c-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingCampaignEffectivenessBlobDataset başlangıç: 5/2/2014 8:00:00 PM End: 5/3/2014 8:00:00 PM</span><span class="sxs-lookup"><span data-stu-id="0d82c-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="0d82c-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d82c-117">EXAMPLES</span></span>

### <span data-ttu-id="0d82c-118">Örnek 1: veri kümesi alma</span><span class="sxs-lookup"><span data-stu-id="0d82c-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="0d82c-119">Bu komut, 05/21/2014 tarihinde PM GMT ile başlayan wikiadf adlı veri fabrikası adındaki dawikiaggreg</span><span class="sxs-lookup"><span data-stu-id="0d82c-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="0d82c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d82c-120">PARAMETERS</span></span>

### <span data-ttu-id="0d82c-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0d82c-121">-DataFactory</span></span>
<span data-ttu-id="0d82c-122">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d82c-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0d82c-123">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimler için çalışır.</span><span class="sxs-lookup"><span data-stu-id="0d82c-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0d82c-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0d82c-124">-DataFactoryName</span></span>
<span data-ttu-id="0d82c-125">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d82c-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0d82c-126">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait olan dilimler için çalışır.</span><span class="sxs-lookup"><span data-stu-id="0d82c-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0d82c-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="0d82c-127">-DatasetName</span></span>
<span data-ttu-id="0d82c-128">Veri kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d82c-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="0d82c-129">Bu cmdlet, bu parametrenin belirttiği veri kümesine ait olan dilimler için çalışır.</span><span class="sxs-lookup"><span data-stu-id="0d82c-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d82c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d82c-130">-DefaultProfile</span></span>
<span data-ttu-id="0d82c-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0d82c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d82c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d82c-132">-ResourceGroupName</span></span>
<span data-ttu-id="0d82c-133">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d82c-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0d82c-134">Bu cmdlet, bu parametrenin belirttiği gruba ait olan dilimler için fabrika çalışmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="0d82c-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0d82c-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="0d82c-135">-StartDateTime</span></span>
<span data-ttu-id="0d82c-136">Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d82c-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="0d82c-137">Bu cmdlet bu süre ile eşleşen veri dilimleri için çalışır.</span><span class="sxs-lookup"><span data-stu-id="0d82c-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="0d82c-138">*Startdatetıme* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:</span><span class="sxs-lookup"><span data-stu-id="0d82c-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d82c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d82c-139">CommonParameters</span></span>
<span data-ttu-id="0d82c-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d82c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d82c-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d82c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d82c-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d82c-142">INPUTS</span></span>

### <span data-ttu-id="0d82c-143">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="0d82c-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0d82c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0d82c-144">System.String</span></span>

## <span data-ttu-id="0d82c-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d82c-145">OUTPUTS</span></span>

### <span data-ttu-id="0d82c-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="0d82c-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="0d82c-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d82c-147">NOTES</span></span>
* <span data-ttu-id="0d82c-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="0d82c-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0d82c-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d82c-149">RELATED LINKS</span></span>

[<span data-ttu-id="0d82c-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="0d82c-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


