---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapsePipelineRun.md
ms.openlocfilehash: f907afbc573d558a08d514c019cbcbe3fa999bf6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267965"
---
# <span data-ttu-id="a4761-101">Stop-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="a4761-101">Stop-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="a4761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4761-102">SYNOPSIS</span></span>
<span data-ttu-id="a4761-103">Çalışma alanında bir ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="a4761-103">Stops a pipeline run in a workspace.</span></span>

## <span data-ttu-id="a4761-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4761-104">SYNTAX</span></span>

### <span data-ttu-id="a4761-105">RemoveByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a4761-105">RemoveByName (Default)</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4761-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a4761-106">RemoveByObject</span></span>
```
Stop-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4761-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a4761-107">RemoveByInputObject</span></span>
```
Stop-AzSynapsePipelineRun -InputObject <PSPipelineRun> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4761-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4761-108">DESCRIPTION</span></span>
<span data-ttu-id="a4761-109">**Stop-AzSynapsePipelineRun** cmdlet 'i, ARDıŞıK düzen kodu ile belirtilen çalışma alanında bir ardışık düzeni durdurur.</span><span class="sxs-lookup"><span data-stu-id="a4761-109">The **Stop-AzSynapsePipelineRun** cmdlet stops a pipeline run in a workspace specified with the pipeline run ID.</span></span>

## <span data-ttu-id="a4761-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4761-110">EXAMPLES</span></span>

### <span data-ttu-id="a4761-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a4761-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="a4761-112">Bu komut, çalışma alanı contoso</span><span class="sxs-lookup"><span data-stu-id="a4761-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a4761-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a4761-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapsePipelineRun -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
```

<span data-ttu-id="a4761-114">Bu komut çalışma alanı 'nda b9730a13-AA12-4926-a8b3-8e3a974ab0bd kimliği olan ardışık düzen çalışmasını ardışık düzen aracılığıyla durdurur.</span><span class="sxs-lookup"><span data-stu-id="a4761-114">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="a4761-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a4761-115">Example 3</span></span>
```powershell
PS C:\> $pipelineRun = Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd
PS C:\> $pipelineRun | Stop-AzSynapsePipelineRun
```

<span data-ttu-id="a4761-116">Bu komut çalışma alanı 'nda b9730a13-AA12-4926-a8b3-8e3a974ab0bd kimliği olan ardışık düzen çalışmasını ardışık düzen aracılığıyla durdurur.</span><span class="sxs-lookup"><span data-stu-id="a4761-116">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a4761-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4761-117">PARAMETERS</span></span>

### <span data-ttu-id="a4761-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="a4761-118">-AsJob</span></span>
<span data-ttu-id="a4761-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a4761-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4761-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4761-120">-DefaultProfile</span></span>
<span data-ttu-id="a4761-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4761-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4761-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4761-122">-InputObject</span></span>
<span data-ttu-id="a4761-123">Ardışık düzen ile ilgili bilgiler.</span><span class="sxs-lookup"><span data-stu-id="a4761-123">The information about the pipeline run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4761-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a4761-124">-PassThru</span></span>
<span data-ttu-id="a4761-125">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="a4761-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a4761-126">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="a4761-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a4761-127">-Ardışık düzen eylemsizlik</span><span class="sxs-lookup"><span data-stu-id="a4761-127">-PipelineRunId</span></span>
<span data-ttu-id="a4761-128">Ardışık düzen çalışma tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a4761-128">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4761-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="a4761-129">-WorkspaceName</span></span>
<span data-ttu-id="a4761-130">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="a4761-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4761-131">-</span><span class="sxs-lookup"><span data-stu-id="a4761-131">-WorkspaceObject</span></span>
<span data-ttu-id="a4761-132">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="a4761-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4761-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a4761-133">-Confirm</span></span>
<span data-ttu-id="a4761-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a4761-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4761-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4761-135">-WhatIf</span></span>
<span data-ttu-id="a4761-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4761-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4761-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a4761-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4761-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4761-138">CommonParameters</span></span>
<span data-ttu-id="a4761-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4761-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4761-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a4761-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4761-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4761-141">INPUTS</span></span>

### <span data-ttu-id="a4761-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4761-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a4761-143">Microsoft. Azure. Commands. SYNAPSE. modeller. Pspipeleylemsizlik</span><span class="sxs-lookup"><span data-stu-id="a4761-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="a4761-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4761-144">OUTPUTS</span></span>

### <span data-ttu-id="a4761-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4761-145">System.Boolean</span></span>

## <span data-ttu-id="a4761-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4761-146">NOTES</span></span>

## <span data-ttu-id="a4761-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4761-147">RELATED LINKS</span></span>
