---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938361"
---
# <span data-ttu-id="4ba94-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="4ba94-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="4ba94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ba94-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba94-103">Ardışık düzen çalıştırmaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4ba94-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="4ba94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ba94-104">SYNTAX</span></span>

### <span data-ttu-id="4ba94-105">ByFactoryNameByRunId (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ba94-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ba94-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="4ba94-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ba94-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="4ba94-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ba94-108">Byfactorynamebypfeline</span><span class="sxs-lookup"><span data-stu-id="4ba94-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ba94-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ba94-109">DESCRIPTION</span></span>
<span data-ttu-id="4ba94-110">**Get-AzDataFactoryV2PipelineRun** komutu belirtilen ardışık düzen için çalıştırmalar hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="4ba94-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="4ba94-111">Ardışık düzen eylemsizlik kimliği belirtilmişse, bu KIMLIĞE sahip Run için ayrıntılar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4ba94-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="4ba94-112">Ardışık düzen eylemsizlik kimliği belirtilmemişse, önceki tüm çalıştırmalar ve LastUpdatedAfter ile Lastupdated'in değerleri arasında gerçekleşen ardışık düzenler hakkındaki bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ba94-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="4ba94-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ba94-113">EXAMPLES</span></span>

### <span data-ttu-id="4ba94-114">Örnek 1: ardışık düzen çalışması için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="4ba94-114">Example 1: Get information for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :
```

<span data-ttu-id="4ba94-115">Bu komut, "61eb095a-FE23-4591-8a97-fade6c65ca72" KIMLIĞINE sahip ardışık düzene sahip ile ilgili ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="4ba94-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="4ba94-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ba94-116">PARAMETERS</span></span>

### <span data-ttu-id="4ba94-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4ba94-117">-DataFactory</span></span>
<span data-ttu-id="4ba94-118">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4ba94-118">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba94-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4ba94-119">-DataFactoryName</span></span>
<span data-ttu-id="4ba94-120">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="4ba94-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba94-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba94-121">-DefaultProfile</span></span>
<span data-ttu-id="4ba94-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ba94-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ba94-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="4ba94-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="4ba94-124">ISO8601 biçiminde, ardışık düzen çalıştırmasının gönderildiği veya bu tarihten sonraki saati.</span><span class="sxs-lookup"><span data-stu-id="4ba94-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba94-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="4ba94-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="4ba94-126">ISO8601 biçiminde, ardışık düzen çalıştırmasının yapıldığı saat veya önceki saat.</span><span class="sxs-lookup"><span data-stu-id="4ba94-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ba94-127">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="4ba94-127">-PipelineName</span></span>
<span data-ttu-id="4ba94-128">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="4ba94-128">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba94-129">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="4ba94-129">-PipelineRunId</span></span>
<span data-ttu-id="4ba94-130">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4ba94-130">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba94-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ba94-131">-ResourceGroupName</span></span>
<span data-ttu-id="4ba94-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4ba94-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba94-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba94-133">CommonParameters</span></span>
<span data-ttu-id="4ba94-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ba94-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba94-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba94-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba94-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ba94-136">INPUTS</span></span>

### <span data-ttu-id="4ba94-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="4ba94-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="4ba94-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4ba94-138">System.String</span></span>

## <span data-ttu-id="4ba94-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ba94-139">OUTPUTS</span></span>

### <span data-ttu-id="4ba94-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pspipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="4ba94-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="4ba94-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ba94-141">NOTES</span></span>

## <span data-ttu-id="4ba94-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ba94-142">RELATED LINKS</span></span>

[<span data-ttu-id="4ba94-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4ba94-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="4ba94-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="4ba94-144">Get-AzDataFactoryV2ActivityRun</span></span>]()
