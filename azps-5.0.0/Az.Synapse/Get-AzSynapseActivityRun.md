---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseactivityrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseActivityRun.md
ms.openlocfilehash: fd300a54b3f35aa69a94bfee69cfcf7ca60f95a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276505"
---
# <span data-ttu-id="5d612-101">Get-AzSynapseActivityRun</span><span class="sxs-lookup"><span data-stu-id="5d612-101">Get-AzSynapseActivityRun</span></span>

## <span data-ttu-id="5d612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d612-102">SYNOPSIS</span></span>
<span data-ttu-id="5d612-103">Potansiyel satış çalışması için etkinlik çalıştırmaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5d612-103">Gets information about activity runs for a pipeline run.</span></span>

## <span data-ttu-id="5d612-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d612-104">SYNTAX</span></span>

### <span data-ttu-id="5d612-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d612-105">GetByName (Default)</span></span>
```
Get-AzSynapseActivityRun -WorkspaceName <String> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d612-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="5d612-106">GetByObject</span></span>
```
Get-AzSynapseActivityRun -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> -PipelineRunId <String>
 -RunStartedAfter <DateTimeOffset> -RunStartedBefore <DateTimeOffset> [-ActivityName <String>]
 [-Status <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d612-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d612-107">DESCRIPTION</span></span>
<span data-ttu-id="5d612-108">**Get-AzSynapseActivityRun** cmdlet 'i, belirli bir zaman diliminde oluşan belirtilen ardışık düzen çalıştırmasına yönelik çalışma alanında çalıştırmalar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="5d612-108">The **Get-AzSynapseActivityRun** cmdlet gets information about runs in workspace for the specified pipeline run that happened in the given timeframe.</span></span> <span data-ttu-id="5d612-109">Ayrıca, etkinlik adı ve çalıştırmanın durumu için filtreler belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5d612-109">Additionally, you can specify filters for activity name and the status of the run.</span></span>

## <span data-ttu-id="5d612-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d612-110">EXAMPLES</span></span>

### <span data-ttu-id="5d612-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5d612-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseActivityRun -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="5d612-112">Bu komut, ContosoPipeline "2018-09-01T21:00" ve "2018-09-30T21:00" arasında gerçekleşen "f288712d-fb08-4cb8-96ef-82d3b9b30621" KIMLIĞIYLE çalışma</span><span class="sxs-lookup"><span data-stu-id="5d612-112">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00".</span></span>

### <span data-ttu-id="5d612-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5d612-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseActivityRun -PipelineName ContosoPipeline -PipelineRunId "f288712d-fb08-4cb8-96ef-82d3b9b30621" -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2018-09-30T21:00"
```

<span data-ttu-id="5d612-114">Bu komut, ContosoPipeline, "2018-09-01T21:00" ve "2018-09-30T21:00" arasında "</span><span class="sxs-lookup"><span data-stu-id="5d612-114">This command gets details about all activity runs in the pipeline called ContosoPipeline run with ID "f288712d-fb08-4cb8-96ef-82d3b9b30621" that happened between "2018-09-01T21:00" and "2018-09-30T21:00" through pipeline.</span></span>

## <span data-ttu-id="5d612-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d612-115">PARAMETERS</span></span>

### <span data-ttu-id="5d612-116">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="5d612-116">-ActivityName</span></span>
<span data-ttu-id="5d612-117">Etkinliğin adı.</span><span class="sxs-lookup"><span data-stu-id="5d612-117">The name of the activity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d612-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d612-118">-DefaultProfile</span></span>
<span data-ttu-id="5d612-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d612-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d612-120">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="5d612-120">-PipelineName</span></span>
<span data-ttu-id="5d612-121">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="5d612-121">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d612-122">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="5d612-122">-PipelineRunId</span></span>
<span data-ttu-id="5d612-123">Ardışık düzen çalışma tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="5d612-123">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d612-124">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="5d612-124">-RunStartedAfter</span></span>
<span data-ttu-id="5d612-125">Run olayının ' ISO 8601 ' biçiminde güncelleştirildiği saat veya daha sonrası.</span><span class="sxs-lookup"><span data-stu-id="5d612-125">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d612-126">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="5d612-126">-RunStartedBefore</span></span>
<span data-ttu-id="5d612-127">Run olayının ' ISO 8601 ' biçiminde güncelleştirildiği saat veya daha önce.</span><span class="sxs-lookup"><span data-stu-id="5d612-127">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d612-128">-Durum</span><span class="sxs-lookup"><span data-stu-id="5d612-128">-Status</span></span>
<span data-ttu-id="5d612-129">Ardışık düzenin durumu.</span><span class="sxs-lookup"><span data-stu-id="5d612-129">The status of the pipeline run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d612-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="5d612-130">-WorkspaceName</span></span>
<span data-ttu-id="5d612-131">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="5d612-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d612-132">-</span><span class="sxs-lookup"><span data-stu-id="5d612-132">-WorkspaceObject</span></span>
<span data-ttu-id="5d612-133">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="5d612-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d612-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d612-134">CommonParameters</span></span>
<span data-ttu-id="5d612-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d612-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d612-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5d612-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d612-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d612-137">INPUTS</span></span>

### <span data-ttu-id="5d612-138">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d612-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5d612-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d612-139">OUTPUTS</span></span>

### <span data-ttu-id="5d612-140">Microsoft. Azure. Commands. SYNAPSE. modeller. PSActivityRunsQueryResponse</span><span class="sxs-lookup"><span data-stu-id="5d612-140">Microsoft.Azure.Commands.Synapse.Models.PSActivityRunsQueryResponse</span></span>

## <span data-ttu-id="5d612-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d612-141">NOTES</span></span>

## <span data-ttu-id="5d612-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d612-142">RELATED LINKS</span></span>
