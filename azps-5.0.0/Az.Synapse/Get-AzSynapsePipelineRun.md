---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323551"
---
# <span data-ttu-id="36290-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="36290-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="36290-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36290-102">SYNOPSIS</span></span>
<span data-ttu-id="36290-103">Ardışık düzen çalıştırmaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="36290-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="36290-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36290-104">SYNTAX</span></span>

### <span data-ttu-id="36290-105">Getbynair (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36290-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36290-106">Tüm</span><span class="sxs-lookup"><span data-stu-id="36290-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36290-107">Getbyobjectangerçekleşti</span><span class="sxs-lookup"><span data-stu-id="36290-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36290-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="36290-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36290-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="36290-109">DESCRIPTION</span></span>
<span data-ttu-id="36290-110">**Get-AzSynapsePipelineRun** komutu belirtilen ardışık düzen için çalıştırmalar hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="36290-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="36290-111">Ardışık düzen eylemsizlik kimliği belirtilmişse, bu KIMLIĞE sahip Run için ayrıntılar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="36290-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="36290-112">Ardışık düzen eylemsizlik kimliği belirtilmemişse, önceki RunStartedAfter ve Runstartedvalue arasında gerçekleşen ardışık düzenler için tüm çalıştırmalar hakkında bilgiler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="36290-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="36290-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36290-113">EXAMPLES</span></span>

### <span data-ttu-id="36290-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36290-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="36290-115">Bu komut, "61eb095a-FE23-4591-8a97-fade6c65ca72" KIMLIĞINE sahip ardışık düzene sahip ile ilgili ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="36290-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="36290-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36290-116">PARAMETERS</span></span>

### <span data-ttu-id="36290-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36290-117">-DefaultProfile</span></span>
<span data-ttu-id="36290-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36290-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36290-119">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="36290-119">-PipelineName</span></span>
<span data-ttu-id="36290-120">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="36290-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36290-121">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="36290-121">-PipelineRunId</span></span>
<span data-ttu-id="36290-122">Ardışık düzen çalışma tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="36290-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36290-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="36290-123">-RunStartedAfter</span></span>
<span data-ttu-id="36290-124">Run olayının ' ISO 8601 ' biçiminde güncelleştirildiği saat veya daha sonrası.</span><span class="sxs-lookup"><span data-stu-id="36290-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36290-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="36290-125">-RunStartedBefore</span></span>
<span data-ttu-id="36290-126">Run olayının ' ISO 8601 ' biçiminde güncelleştirildiği saat veya daha önce.</span><span class="sxs-lookup"><span data-stu-id="36290-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36290-127">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="36290-127">-WorkspaceName</span></span>
<span data-ttu-id="36290-128">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="36290-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36290-129">-</span><span class="sxs-lookup"><span data-stu-id="36290-129">-WorkspaceObject</span></span>
<span data-ttu-id="36290-130">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="36290-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36290-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36290-131">CommonParameters</span></span>
<span data-ttu-id="36290-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36290-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36290-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="36290-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36290-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36290-134">INPUTS</span></span>

### <span data-ttu-id="36290-135">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="36290-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="36290-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36290-136">OUTPUTS</span></span>

### <span data-ttu-id="36290-137">Microsoft. Azure. Commands. SYNAPSE. modeller. Pspipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="36290-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="36290-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36290-138">NOTES</span></span>

## <span data-ttu-id="36290-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36290-139">RELATED LINKS</span></span>
