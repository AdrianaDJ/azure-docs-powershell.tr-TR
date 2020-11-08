---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseTrigger.md
ms.openlocfilehash: 4e35814be14c2be3b5ba0fd1ca5960d297590dca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276599"
---
# <span data-ttu-id="22adf-101">Stop-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="22adf-101">Stop-AzSynapseTrigger</span></span>

## <span data-ttu-id="22adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22adf-102">SYNOPSIS</span></span>
<span data-ttu-id="22adf-103">Çalışma alanında tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="22adf-103">Stops a trigger in a workspace.</span></span>

## <span data-ttu-id="22adf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22adf-104">SYNTAX</span></span>

### <span data-ttu-id="22adf-105">StopByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="22adf-105">StopByName (Default)</span></span>
```
Stop-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22adf-106">StopByObject</span><span class="sxs-lookup"><span data-stu-id="22adf-106">StopByObject</span></span>
```
Stop-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22adf-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="22adf-107">StopByInputObject</span></span>
```
Stop-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22adf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="22adf-108">DESCRIPTION</span></span>
<span data-ttu-id="22adf-109">**Stop-AzSynapseTrigger** cmdlet 'i çalışma alanındaki bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="22adf-109">The **Stop-AzSynapseTrigger** cmdlet stops a trigger in a workspace.</span></span> <span data-ttu-id="22adf-110">Tetik ' Started ' durumundaysa, cmdlet tetikleyiciyi durdurur ve artık ardışık düzenler çağırmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="22adf-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="22adf-111">Tetik zaten ' durduruldu ' durumundaysa, bu cmdlet 'in etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="22adf-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="22adf-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22adf-112">EXAMPLES</span></span>

### <span data-ttu-id="22adf-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="22adf-113">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="22adf-114">Çalışma alanında Contosotetikleyicisi adındaki bir tetikleyiciyi durdurur.</span><span class="sxs-lookup"><span data-stu-id="22adf-114">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="22adf-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="22adf-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Stop-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="22adf-116">Çalışma alanında ContosoTrigger adındaki bir tetikleyiciyi ardışık düzen aracılığıyla durdurur.</span><span class="sxs-lookup"><span data-stu-id="22adf-116">Stops a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="22adf-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="22adf-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Stop-AzSynapseTrigger
```

<span data-ttu-id="22adf-118">Çalışma alanında ContosoTrigger adındaki bir tetikleyiciyi ardışık düzen aracılığıyla durdurma.</span><span class="sxs-lookup"><span data-stu-id="22adf-118">Stop a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="22adf-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22adf-119">PARAMETERS</span></span>

### <span data-ttu-id="22adf-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="22adf-120">-AsJob</span></span>
<span data-ttu-id="22adf-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="22adf-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22adf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22adf-122">-DefaultProfile</span></span>
<span data-ttu-id="22adf-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22adf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22adf-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22adf-124">-InputObject</span></span>
<span data-ttu-id="22adf-125">Tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="22adf-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22adf-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="22adf-126">-Name</span></span>
<span data-ttu-id="22adf-127">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="22adf-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName, StopByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22adf-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="22adf-128">-PassThru</span></span>
<span data-ttu-id="22adf-129">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="22adf-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="22adf-130">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="22adf-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="22adf-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="22adf-131">-WorkspaceName</span></span>
<span data-ttu-id="22adf-132">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="22adf-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22adf-133">-</span><span class="sxs-lookup"><span data-stu-id="22adf-133">-WorkspaceObject</span></span>
<span data-ttu-id="22adf-134">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="22adf-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22adf-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="22adf-135">-Confirm</span></span>
<span data-ttu-id="22adf-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22adf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22adf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22adf-137">-WhatIf</span></span>
<span data-ttu-id="22adf-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22adf-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22adf-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22adf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22adf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22adf-140">CommonParameters</span></span>
<span data-ttu-id="22adf-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22adf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22adf-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="22adf-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22adf-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22adf-143">INPUTS</span></span>

### <span data-ttu-id="22adf-144">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="22adf-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="22adf-145">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerresource</span><span class="sxs-lookup"><span data-stu-id="22adf-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="22adf-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22adf-146">OUTPUTS</span></span>

### <span data-ttu-id="22adf-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="22adf-147">System.Boolean</span></span>

## <span data-ttu-id="22adf-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22adf-148">NOTES</span></span>

## <span data-ttu-id="22adf-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22adf-149">RELATED LINKS</span></span>
