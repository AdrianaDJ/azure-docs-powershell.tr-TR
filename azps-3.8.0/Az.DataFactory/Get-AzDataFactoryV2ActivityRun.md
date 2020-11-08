---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2ActivityRun.md
ms.openlocfilehash: cdee786d338dce2663bf99916c6b6c2b250e22b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938378"
---
# <span data-ttu-id="88c6e-101">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="88c6e-101">Get-AzDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="88c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="88c6e-103">Potansiyel satış çalışması için etkinlik çalıştırmaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="88c6e-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="88c6e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88c6e-104">SYNTAX</span></span>

### <span data-ttu-id="88c6e-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88c6e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88c6e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="88c6e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88c6e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="88c6e-107">DESCRIPTION</span></span>
<span data-ttu-id="88c6e-108">**Get-AzDataFactoryV2ActivityRun** cmdlet 'i, belirli bir zaman diliminde oluşan belirtilen ardışık düzen çalışması Için Azure Data Factory 'de çalıştırmalar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="88c6e-108">The **Get-AzDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="88c6e-109">Ayrıca, etkinlik adı, çalıştırmayı yürüten bağlantılı hizmet adı ve çalıştırmanın durumu için filtreler belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="88c6e-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="88c6e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88c6e-110">EXAMPLES</span></span>

### <span data-ttu-id="88c6e-111">Örnek 1: ardışık düzen çalışması için tüm etkinlikleri alma</span><span class="sxs-lookup"><span data-stu-id="88c6e-111">Example 1: Get all activity runs for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2ActivityRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter "2017-09-01" -RunStartedBefore "2017-09-30"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    ActivityName      : MyWebActivity
    PipelineRunId     : f288712d-fb08-4cb8-96ef-82d3b9b30621
    PipelineName      : DPWikisample
    Input             : {method, url, headers, body...}
    Output            : {operationstatus}
    ActivityRunStart  : 9/14/2017 12:20:57 AM
    ActivityRunEnd    : 9/14/2017 12:21:00 AM
    DurationInMs      : 2768
    Status            : Succeeded
    Error             : {errorCode, message, failureType, target}
```

<span data-ttu-id="88c6e-112">Bu komut, "2017-09-01" ve "2017-09-30" arasında gerçekleşen ardışık düzene sahip çalışma</span><span class="sxs-lookup"><span data-stu-id="88c6e-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="88c6e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88c6e-113">PARAMETERS</span></span>

### <span data-ttu-id="88c6e-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="88c6e-114">-ActivityName</span></span>
<span data-ttu-id="88c6e-115">Etkinliğin adı.</span><span class="sxs-lookup"><span data-stu-id="88c6e-115">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c6e-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="88c6e-116">-DataFactory</span></span>
<span data-ttu-id="88c6e-117">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="88c6e-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88c6e-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="88c6e-118">-DataFactoryName</span></span>
<span data-ttu-id="88c6e-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="88c6e-119">The data factory name.</span></span>

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

### <span data-ttu-id="88c6e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c6e-120">-DefaultProfile</span></span>
<span data-ttu-id="88c6e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88c6e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88c6e-122">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="88c6e-122">-PipelineRunId</span></span>
<span data-ttu-id="88c6e-123">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="88c6e-123">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c6e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88c6e-124">-ResourceGroupName</span></span>
<span data-ttu-id="88c6e-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="88c6e-125">The resource group name.</span></span>

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

### <span data-ttu-id="88c6e-126">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="88c6e-126">-RunStartedAfter</span></span>
<span data-ttu-id="88c6e-127">Ardışık düzen çalıştırmasının çalıştırılmaya başladığı saat veya sonraki saat.</span><span class="sxs-lookup"><span data-stu-id="88c6e-127">The time at or after which the pipeline run started to execute.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c6e-128">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="88c6e-128">-RunStartedBefore</span></span>
<span data-ttu-id="88c6e-129">Ardışık düzen çalıştırmasının çalıştırılmaya başladığı saat veya önceki saat.</span><span class="sxs-lookup"><span data-stu-id="88c6e-129">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="88c6e-130">-Durum</span><span class="sxs-lookup"><span data-stu-id="88c6e-130">-Status</span></span>
<span data-ttu-id="88c6e-131">Ardışık düzenin durumu.</span><span class="sxs-lookup"><span data-stu-id="88c6e-131">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88c6e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c6e-132">CommonParameters</span></span>
<span data-ttu-id="88c6e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88c6e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c6e-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88c6e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c6e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88c6e-135">INPUTS</span></span>

### <span data-ttu-id="88c6e-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="88c6e-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="88c6e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="88c6e-137">System.String</span></span>

## <span data-ttu-id="88c6e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88c6e-138">OUTPUTS</span></span>

### <span data-ttu-id="88c6e-139">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="88c6e-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="88c6e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88c6e-140">NOTES</span></span>

## <span data-ttu-id="88c6e-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88c6e-141">RELATED LINKS</span></span>

[<span data-ttu-id="88c6e-142">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="88c6e-142">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="88c6e-143">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="88c6e-143">Get-AzDataFactoryV2PipelineRun</span></span>]()
