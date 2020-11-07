---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 2000e489dcb5a0bab384ac0aad8a1ffbe53aba15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764872"
---
# <span data-ttu-id="41eaa-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="41eaa-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="41eaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="41eaa-103">Potansiyel satış çalışması için etkinlik çalıştırmaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="41eaa-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41eaa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41eaa-104">SYNTAX</span></span>

### <span data-ttu-id="41eaa-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="41eaa-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="41eaa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="41eaa-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>]
 [[-LinkedServiceName] <String>] [-DataFactory] <PSDataFactory>
```


## <span data-ttu-id="41eaa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="41eaa-107">DESCRIPTION</span></span>

<span data-ttu-id="41eaa-108">**Get-AzureRmDataFactoryV2ActivityRun** cmdlet 'i, belirli bir zaman diliminde oluşan belirtilen ardışık düzen çalışması Için Azure Data Factory 'de çalıştırmalar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="41eaa-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="41eaa-109">Ayrıca, etkinlik adı, çalıştırmayı yürüten bağlantılı hizmet adı ve çalıştırmanın durumu için filtreler belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41eaa-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="41eaa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41eaa-110">EXAMPLES</span></span>

### <span data-ttu-id="41eaa-111">Örnek 1: ardışık düzen çalışması için tüm etkinlikleri alma</span><span class="sxs-lookup"><span data-stu-id="41eaa-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    LinkedServiceName :
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}

```

<span data-ttu-id="41eaa-112">Bu komut, "2017-09-01" ve "2017-09-30" arasında gerçekleşen ardışık düzene sahip çalışma</span><span class="sxs-lookup"><span data-stu-id="41eaa-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="41eaa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41eaa-113">PARAMETERS</span></span>

### <span data-ttu-id="41eaa-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="41eaa-114">-ActivityName</span></span>
<span data-ttu-id="41eaa-115">Etkinliğin adı.</span><span class="sxs-lookup"><span data-stu-id="41eaa-115">The name of the activity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eaa-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="41eaa-116">-DataFactory</span></span>
<span data-ttu-id="41eaa-117">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="41eaa-117">The data factory object.</span></span>

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

### <span data-ttu-id="41eaa-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="41eaa-118">-DataFactoryName</span></span>
<span data-ttu-id="41eaa-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="41eaa-119">The data factory name.</span></span>

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

### <span data-ttu-id="41eaa-120">-Linkedhizmetadı</span><span class="sxs-lookup"><span data-stu-id="41eaa-120">-LinkedServiceName</span></span>
<span data-ttu-id="41eaa-121">Bağlantılı hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="41eaa-121">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eaa-122">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="41eaa-122">-PipelineRunId</span></span>
<span data-ttu-id="41eaa-123">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="41eaa-123">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eaa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41eaa-124">-ResourceGroupName</span></span>
<span data-ttu-id="41eaa-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="41eaa-125">The resource group name.</span></span>

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

### <span data-ttu-id="41eaa-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="41eaa-126">-RunStartedAfter</span></span>
<span data-ttu-id="41eaa-127">Ardışık düzen çalıştırmasının çalıştırılmaya başladığı saat veya sonraki saat.</span><span class="sxs-lookup"><span data-stu-id="41eaa-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eaa-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="41eaa-128">-RunStartedBefore</span></span>
<span data-ttu-id="41eaa-129">Ardışık düzen çalıştırmasının çalıştırılmaya başladığı saat veya önceki saat.</span><span class="sxs-lookup"><span data-stu-id="41eaa-129">The time at or before which the pipeline run started to execute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41eaa-130">-Durum</span><span class="sxs-lookup"><span data-stu-id="41eaa-130">-Status</span></span>
<span data-ttu-id="41eaa-131">Ardışık düzenin durumu.</span><span class="sxs-lookup"><span data-stu-id="41eaa-131">The status of the pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="41eaa-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41eaa-132">INPUTS</span></span>

### <span data-ttu-id="41eaa-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="41eaa-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="41eaa-134">System. String</span><span class="sxs-lookup"><span data-stu-id="41eaa-134">System.String</span></span>


## <span data-ttu-id="41eaa-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41eaa-135">OUTPUTS</span></span>

### <span data-ttu-id="41eaa-136">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. PSActivityRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="41eaa-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="41eaa-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="41eaa-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>


## <span data-ttu-id="41eaa-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41eaa-138">NOTES</span></span>

## <span data-ttu-id="41eaa-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41eaa-139">RELATED LINKS</span></span>
[<span data-ttu-id="41eaa-140">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="41eaa-140">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="41eaa-141">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="41eaa-141">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

