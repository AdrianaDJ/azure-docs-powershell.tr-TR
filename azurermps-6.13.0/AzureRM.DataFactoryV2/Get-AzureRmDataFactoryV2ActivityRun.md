---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2activityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2ActivityRun.md
ms.openlocfilehash: 4bfebac1d37dbdc0cac2bc8262993a6c81b0c9ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590336"
---
# <span data-ttu-id="2b37c-101">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="2b37c-101">Get-AzureRmDataFactoryV2ActivityRun</span></span>

## <span data-ttu-id="2b37c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b37c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b37c-103">Potansiyel satış çalışması için etkinlik çalıştırmaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2b37c-103">Gets information about activity runs for a pipeline run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b37c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b37c-104">SYNTAX</span></span>

### <span data-ttu-id="2b37c-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b37c-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b37c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2b37c-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2ActivityRun [-PipelineRunId] <String> [-RunStartedAfter] <DateTime>
 [-RunStartedBefore] <DateTime> [[-ActivityName] <String>] [[-Status] <String>] [[-LinkedServiceName] <String>]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b37c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b37c-107">DESCRIPTION</span></span>
<span data-ttu-id="2b37c-108">**Get-AzureRmDataFactoryV2ActivityRun** cmdlet 'i, belirli bir zaman diliminde oluşan belirtilen ardışık düzen çalışması Için Azure Data Factory 'de çalıştırmalar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2b37c-108">The **Get-AzureRmDataFactoryV2ActivityRun** cmdlet gets information about runs in Azure Data Factory for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="2b37c-109">Ayrıca, etkinlik adı, çalıştırmayı yürüten bağlantılı hizmet adı ve çalıştırmanın durumu için filtreler belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b37c-109">Additionally, you can specify filters for activity name, linked service name that executed the run, and the status of the run.</span></span>

## <span data-ttu-id="2b37c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b37c-110">EXAMPLES</span></span>

### <span data-ttu-id="2b37c-111">Örnek 1: ardışık düzen çalışması için tüm etkinlikleri alma</span><span class="sxs-lookup"><span data-stu-id="2b37c-111">Example 1: Get all activity runs for a pipeline run</span></span>
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

<span data-ttu-id="2b37c-112">Bu komut, "2017-09-01" ve "2017-09-30" arasında gerçekleşen ardışık düzene sahip çalışma</span><span class="sxs-lookup"><span data-stu-id="2b37c-112">This command gets details about all activity runs in the pipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2017-09-01" and "2017-09-30".</span></span>

## <span data-ttu-id="2b37c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b37c-113">PARAMETERS</span></span>

### <span data-ttu-id="2b37c-114">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="2b37c-114">-ActivityName</span></span>
<span data-ttu-id="2b37c-115">Etkinliğin adı.</span><span class="sxs-lookup"><span data-stu-id="2b37c-115">The name of the activity.</span></span>

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

### <span data-ttu-id="2b37c-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2b37c-116">-DataFactory</span></span>
<span data-ttu-id="2b37c-117">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2b37c-117">The data factory object.</span></span>

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

### <span data-ttu-id="2b37c-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2b37c-118">-DataFactoryName</span></span>
<span data-ttu-id="2b37c-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="2b37c-119">The data factory name.</span></span>

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

### <span data-ttu-id="2b37c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b37c-120">-DefaultProfile</span></span>
<span data-ttu-id="2b37c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b37c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b37c-122">-Linkedhizmetadı</span><span class="sxs-lookup"><span data-stu-id="2b37c-122">-LinkedServiceName</span></span>
<span data-ttu-id="2b37c-123">Bağlantılı hizmet adı.</span><span class="sxs-lookup"><span data-stu-id="2b37c-123">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b37c-124">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="2b37c-124">-PipelineRunId</span></span>
<span data-ttu-id="2b37c-125">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2b37c-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="2b37c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b37c-126">-ResourceGroupName</span></span>
<span data-ttu-id="2b37c-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2b37c-127">The resource group name.</span></span>

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

### <span data-ttu-id="2b37c-128">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="2b37c-128">-RunStartedAfter</span></span>
<span data-ttu-id="2b37c-129">Ardışık düzen çalıştırmasının çalıştırılmaya başladığı saat veya sonraki saat.</span><span class="sxs-lookup"><span data-stu-id="2b37c-129">The time at or after which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="2b37c-130">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="2b37c-130">-RunStartedBefore</span></span>
<span data-ttu-id="2b37c-131">Ardışık düzen çalıştırmasının çalıştırılmaya başladığı saat veya önceki saat.</span><span class="sxs-lookup"><span data-stu-id="2b37c-131">The time at or before which the pipeline run started to execute.</span></span>

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

### <span data-ttu-id="2b37c-132">-Durum</span><span class="sxs-lookup"><span data-stu-id="2b37c-132">-Status</span></span>
<span data-ttu-id="2b37c-133">Ardışık düzenin durumu.</span><span class="sxs-lookup"><span data-stu-id="2b37c-133">The status of the pipeline run.</span></span>

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

### <span data-ttu-id="2b37c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b37c-134">CommonParameters</span></span>
<span data-ttu-id="2b37c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b37c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b37c-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b37c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b37c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b37c-137">INPUTS</span></span>

### <span data-ttu-id="2b37c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="2b37c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="2b37c-139">Parametreler: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2b37c-139">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="2b37c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2b37c-140">System.String</span></span>

## <span data-ttu-id="2b37c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b37c-141">OUTPUTS</span></span>

### <span data-ttu-id="2b37c-142">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSActivityRun</span><span class="sxs-lookup"><span data-stu-id="2b37c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSActivityRun</span></span>

## <span data-ttu-id="2b37c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b37c-143">NOTES</span></span>

## <span data-ttu-id="2b37c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b37c-144">RELATED LINKS</span></span>

[<span data-ttu-id="2b37c-145">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="2b37c-145">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="2b37c-146">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="2b37c-146">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

