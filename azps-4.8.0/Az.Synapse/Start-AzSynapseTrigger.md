---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseTrigger.md
ms.openlocfilehash: d2488a99bba1813c192df5ef8561d83c06f2f6e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267963"
---
# <span data-ttu-id="d7580-101">Start-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="d7580-101">Start-AzSynapseTrigger</span></span>

## <span data-ttu-id="d7580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7580-102">SYNOPSIS</span></span>
<span data-ttu-id="d7580-103">Çalışma alanında tetik başlatır.</span><span class="sxs-lookup"><span data-stu-id="d7580-103">Starts a trigger in a workspace.</span></span>

## <span data-ttu-id="d7580-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7580-104">SYNTAX</span></span>

### <span data-ttu-id="d7580-105">StartByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7580-105">StartByName (Default)</span></span>
```
Start-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7580-106">StartByObject</span><span class="sxs-lookup"><span data-stu-id="d7580-106">StartByObject</span></span>
```
Start-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7580-107">StartByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7580-107">StartByInputObject</span></span>
```
Start-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7580-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7580-108">DESCRIPTION</span></span>
<span data-ttu-id="d7580-109">**Start-AzSynapseTrigger** cmdlet 'i bir çalışma alanında tetik başlatır.</span><span class="sxs-lookup"><span data-stu-id="d7580-109">The **Start-AzSynapseTrigger** cmdlet starts a trigger in a workspace.</span></span> <span data-ttu-id="d7580-110">Tetik ' durduruldu ' durumundaysa, cmdlet tetikleyiciyi başlatır ve sonuç olarak tanımı temelinde ardışık düzen çağırır.</span><span class="sxs-lookup"><span data-stu-id="d7580-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="d7580-111">Tetik zaten ' Started ' durumundaysa, bu cmdlet 'in etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="d7580-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span>

## <span data-ttu-id="d7580-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7580-112">EXAMPLES</span></span>

### <span data-ttu-id="d7580-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d7580-113">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="d7580-114">Çalışma alanı Contosoçalışma alanında ContosoTrigger adındaki bir tetik başlatır.</span><span class="sxs-lookup"><span data-stu-id="d7580-114">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="d7580-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d7580-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Start-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="d7580-116">Çalışma alanında ContosoTrigger adındaki bir tetik ardışık düzen aracılığıyla başlatır.</span><span class="sxs-lookup"><span data-stu-id="d7580-116">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="d7580-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d7580-117">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Start-AzSynapseTrigger
```

<span data-ttu-id="d7580-118">Çalışma alanında ContosoTrigger adındaki bir tetik ardışık düzen aracılığıyla başlatır.</span><span class="sxs-lookup"><span data-stu-id="d7580-118">Starts a trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d7580-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7580-119">PARAMETERS</span></span>

### <span data-ttu-id="d7580-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="d7580-120">-AsJob</span></span>
<span data-ttu-id="d7580-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d7580-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7580-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7580-122">-DefaultProfile</span></span>
<span data-ttu-id="d7580-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7580-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7580-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7580-124">-InputObject</span></span>
<span data-ttu-id="d7580-125">Tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d7580-125">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: StartByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7580-126">-Name</span></span>
<span data-ttu-id="d7580-127">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="d7580-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName, StartByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d7580-128">-PassThru</span></span>
<span data-ttu-id="d7580-129">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="d7580-129">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d7580-130">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="d7580-130">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d7580-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="d7580-131">-WorkspaceName</span></span>
<span data-ttu-id="d7580-132">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="d7580-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-133">-</span><span class="sxs-lookup"><span data-stu-id="d7580-133">-WorkspaceObject</span></span>
<span data-ttu-id="d7580-134">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="d7580-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StartByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7580-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7580-135">-Confirm</span></span>
<span data-ttu-id="d7580-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7580-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7580-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7580-137">-WhatIf</span></span>
<span data-ttu-id="d7580-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7580-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7580-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7580-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7580-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7580-140">CommonParameters</span></span>
<span data-ttu-id="d7580-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7580-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7580-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7580-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7580-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7580-143">INPUTS</span></span>

### <span data-ttu-id="d7580-144">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d7580-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d7580-145">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerresource</span><span class="sxs-lookup"><span data-stu-id="d7580-145">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="d7580-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7580-146">OUTPUTS</span></span>

### <span data-ttu-id="d7580-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7580-147">System.Boolean</span></span>

## <span data-ttu-id="d7580-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7580-148">NOTES</span></span>

## <span data-ttu-id="d7580-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7580-149">RELATED LINKS</span></span>
