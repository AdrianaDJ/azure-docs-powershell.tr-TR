---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapsePipeline.md
ms.openlocfilehash: fc8f24cb124194bc2d2acd5ab5f19a4484571079
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107476"
---
# <span data-ttu-id="c6003-101">Invoke-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="c6003-101">Invoke-AzSynapsePipeline</span></span>

## <span data-ttu-id="c6003-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6003-102">SYNOPSIS</span></span>
<span data-ttu-id="c6003-103">Bir ardışık düzeni, bir çalıştırmayı başlatmak için çağırır.</span><span class="sxs-lookup"><span data-stu-id="c6003-103">Invokes a pipeline to start a run for it.</span></span>

## <span data-ttu-id="c6003-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6003-104">SYNTAX</span></span>

### <span data-ttu-id="c6003-105">NewByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c6003-105">NewByName (Default)</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceName <String> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6003-106">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="c6003-106">NewByInputObject</span></span>
```
Invoke-AzSynapsePipeline -InputObject <PSPipelineResource> [-Parameter <Hashtable>] [-ParameterFile <String>]
 [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6003-107">Yenibyobject</span><span class="sxs-lookup"><span data-stu-id="c6003-107">NewByObject</span></span>
```
Invoke-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -PipelineName <String> [-Parameter <Hashtable>]
 [-ParameterFile <String>] [-ReferencePipelineRunId <String>] [-IsRecovery] [-StartActivityName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6003-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6003-108">DESCRIPTION</span></span>
<span data-ttu-id="c6003-109">**Invoke-AzSynapsePipeline** komutu belirtilen ardışık düzene bir çalışma başlatır ve bu çalışma IÇIN bir kimlik döndürür.</span><span class="sxs-lookup"><span data-stu-id="c6003-109">The **Invoke-AzSynapsePipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="c6003-110">Bu GUID, **Get-AzSynapsePipelineRun** veya **Get-AzSynapseActivityRun** 'a bu çalışma hakkında daha fazla ayrıntı almak için iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="c6003-110">This GUID can be passed to **Get-AzSynapsePipelineRun** or **Get-AzSynapseActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="c6003-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6003-111">EXAMPLES</span></span>

### <span data-ttu-id="c6003-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c6003-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapsePipeline -WorkspaceName ContosoWorkspace -PipelineName ContosoPipeline
```

<span data-ttu-id="c6003-113">Bu komut, çalışma alanı Contosoçalışma alanında ContosoPipeline adındaki ardışık düzen için bir çalışma başlatır.</span><span class="sxs-lookup"><span data-stu-id="c6003-113">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="c6003-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c6003-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Invoke-AzSynapsePipeline -PipelineName ContosoPipeline
```

<span data-ttu-id="c6003-115">Bu komut çalışma alanında ContosoPipeline adındaki ardışık düzen için bir çalışma alanını ardışık düzen aracılığıyla başlatır.</span><span class="sxs-lookup"><span data-stu-id="c6003-115">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="c6003-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c6003-116">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Invoke-AzSynapsePipeline
```

<span data-ttu-id="c6003-117">Bu komut çalışma alanında ContosoPipeline adındaki ardışık düzen için bir çalışma alanını ardışık düzen aracılığıyla başlatır.</span><span class="sxs-lookup"><span data-stu-id="c6003-117">This command starts a run for pipeline called ContosoPipeline in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c6003-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6003-118">PARAMETERS</span></span>

### <span data-ttu-id="c6003-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="c6003-119">-AsJob</span></span>
<span data-ttu-id="c6003-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c6003-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6003-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6003-121">-DefaultProfile</span></span>
<span data-ttu-id="c6003-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6003-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6003-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6003-123">-InputObject</span></span>
<span data-ttu-id="c6003-124">Ardışık düzen ile ilgili bilgiler.</span><span class="sxs-lookup"><span data-stu-id="c6003-124">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6003-125">-Isrecovery</span><span class="sxs-lookup"><span data-stu-id="c6003-125">-IsRecovery</span></span>
<span data-ttu-id="c6003-126">Kurtarma modu bayrağı.</span><span class="sxs-lookup"><span data-stu-id="c6003-126">Recovery mode flag.</span></span>
<span data-ttu-id="c6003-127">Kurtarma modu true olarak ayarlandıysa, belirtilen başvurulan ardışık düzen çalışır ve yeni çalışma aynı GroupID altında gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="c6003-127">If recovery mode is set to true, the specified referenced pipeline run and the new run will be grouped under the same groupId.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6003-128">-Parametre</span><span class="sxs-lookup"><span data-stu-id="c6003-128">-Parameter</span></span>
<span data-ttu-id="c6003-129">Ardışık düzen parametreleri.</span><span class="sxs-lookup"><span data-stu-id="c6003-129">Parameters for pipeline run.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6003-130">-Parameterfıle</span><span class="sxs-lookup"><span data-stu-id="c6003-130">-ParameterFile</span></span>
<span data-ttu-id="c6003-131">Ardışık düzenin parametrelerini içeren dosyanın adı.</span><span class="sxs-lookup"><span data-stu-id="c6003-131">The name of the file with parameters for pipeline run.</span></span>

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

### <span data-ttu-id="c6003-132">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="c6003-132">-PipelineName</span></span>
<span data-ttu-id="c6003-133">Ardışık Düzen adı.</span><span class="sxs-lookup"><span data-stu-id="c6003-133">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName, NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6003-134">-Referencepipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="c6003-134">-ReferencePipelineRunId</span></span>
<span data-ttu-id="c6003-135">Yeniden çalıştırma için ardışık düzen kodu.</span><span class="sxs-lookup"><span data-stu-id="c6003-135">The pipeline run ID for rerun.</span></span>
<span data-ttu-id="c6003-136">Run ID belirtildiyse, belirtilen Run parametreleri yeni bir çalışma oluşturmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c6003-136">If run ID is specified, the parameters of the specified run will be used to create a new run.</span></span>

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

### <span data-ttu-id="c6003-137">-StartActivityName</span><span class="sxs-lookup"><span data-stu-id="c6003-137">-StartActivityName</span></span>
<span data-ttu-id="c6003-138">Kurtarma modunda, yeniden çalıştırma bu aktiviteden başlar.</span><span class="sxs-lookup"><span data-stu-id="c6003-138">In recovery mode, the rerun will start from this activity.</span></span>
<span data-ttu-id="c6003-139">Belirtilmemişse tüm etkinlikler çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="c6003-139">If not specified, all activities will run.</span></span>

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

### <span data-ttu-id="c6003-140">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="c6003-140">-WorkspaceName</span></span>
<span data-ttu-id="c6003-141">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="c6003-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6003-142">-</span><span class="sxs-lookup"><span data-stu-id="c6003-142">-WorkspaceObject</span></span>
<span data-ttu-id="c6003-143">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="c6003-143">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6003-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6003-144">-Confirm</span></span>
<span data-ttu-id="c6003-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6003-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6003-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6003-146">-WhatIf</span></span>
<span data-ttu-id="c6003-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6003-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6003-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6003-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6003-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6003-149">CommonParameters</span></span>
<span data-ttu-id="c6003-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6003-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6003-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c6003-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6003-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6003-152">INPUTS</span></span>

### <span data-ttu-id="c6003-153">Microsoft. Azure. Commands. SYNAPSE. modeller. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="c6003-153">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

### <span data-ttu-id="c6003-154">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6003-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c6003-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6003-155">OUTPUTS</span></span>

### <span data-ttu-id="c6003-156">Microsoft. Azure. Commands. SYNAPSE. modeller. PSCreateRunResponse</span><span class="sxs-lookup"><span data-stu-id="c6003-156">Microsoft.Azure.Commands.Synapse.Models.PSCreateRunResponse</span></span>

## <span data-ttu-id="c6003-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6003-157">NOTES</span></span>

## <span data-ttu-id="c6003-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6003-158">RELATED LINKS</span></span>
