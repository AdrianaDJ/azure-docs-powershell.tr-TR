---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: eba11e68d23c852426a7d4541359874bd813fc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761150"
---
# <span data-ttu-id="20822-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="20822-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="20822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20822-102">SYNOPSIS</span></span>
<span data-ttu-id="20822-103">Ardışık düzen çalıştırmaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="20822-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="20822-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20822-104">SYNTAX</span></span>

### <span data-ttu-id="20822-105">ByFactoryNameByRunId (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="20822-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20822-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="20822-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20822-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="20822-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20822-108">Byfactorynamebypfeline</span><span class="sxs-lookup"><span data-stu-id="20822-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20822-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="20822-109">DESCRIPTION</span></span>
<span data-ttu-id="20822-110">**Get-AzDataFactoryV2PipelineRun** komutu belirtilen ardışık düzen için çalıştırmalar hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="20822-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="20822-111">Ardışık düzen eylemsizlik kimliği belirtilmişse, bu KIMLIĞE sahip Run için ayrıntılar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="20822-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="20822-112">Ardışık düzenin kimliği belirtilmemişse, önceki tüm çalıştırmalar hakkında, LastUpdatedAfter ve Lastupdated'in değerleri arasında gerçekleşen tüm çalıştırmalar hakkında bilgi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="20822-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="20822-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20822-113">EXAMPLES</span></span>

### <span data-ttu-id="20822-114">Örnek 1: pipline Run için bilgi alma</span><span class="sxs-lookup"><span data-stu-id="20822-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="20822-115">Bu komut, "61eb095a-FE23-4591-8a97-fade6c65ca72" KIMLIĞINE sahip ardışık düzene sahip ile ilgili ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="20822-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="20822-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20822-116">PARAMETERS</span></span>

### <span data-ttu-id="20822-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="20822-117">-DataFactory</span></span>
<span data-ttu-id="20822-118">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="20822-118">The data factory object.</span></span>

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

### <span data-ttu-id="20822-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="20822-119">-DataFactoryName</span></span>
<span data-ttu-id="20822-120">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="20822-120">The data factory name.</span></span>

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

### <span data-ttu-id="20822-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20822-121">-DefaultProfile</span></span>
<span data-ttu-id="20822-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20822-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20822-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="20822-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="20822-124">ISO8601 biçiminde, ardışık düzen çalıştırmasının gönderildiği veya bu tarihten sonraki saati.</span><span class="sxs-lookup"><span data-stu-id="20822-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="20822-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="20822-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="20822-126">ISO8601 biçiminde, ardışık düzen çalıştırmasının yapıldığı saat veya önceki saat.</span><span class="sxs-lookup"><span data-stu-id="20822-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="20822-127">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="20822-127">-PipelineName</span></span>
<span data-ttu-id="20822-128">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="20822-128">The pipeline name.</span></span>

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

### <span data-ttu-id="20822-129">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="20822-129">-PipelineRunId</span></span>
<span data-ttu-id="20822-130">Ardışık düzenin çalışma KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="20822-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="20822-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20822-131">-ResourceGroupName</span></span>
<span data-ttu-id="20822-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="20822-132">The resource group name.</span></span>

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

### <span data-ttu-id="20822-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20822-133">CommonParameters</span></span>
<span data-ttu-id="20822-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20822-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20822-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20822-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20822-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20822-136">INPUTS</span></span>

### <span data-ttu-id="20822-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="20822-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="20822-138">System. String</span><span class="sxs-lookup"><span data-stu-id="20822-138">System.String</span></span>

## <span data-ttu-id="20822-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20822-139">OUTPUTS</span></span>

### <span data-ttu-id="20822-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Pspipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="20822-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="20822-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20822-141">NOTES</span></span>

## <span data-ttu-id="20822-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20822-142">RELATED LINKS</span></span>

[<span data-ttu-id="20822-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="20822-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="20822-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="20822-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

