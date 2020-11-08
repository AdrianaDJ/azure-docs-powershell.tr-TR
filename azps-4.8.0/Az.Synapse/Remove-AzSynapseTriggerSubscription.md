---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTriggerSubscription.md
ms.openlocfilehash: 69e7c17d28c94ce00f054a0e5b71eadc4d8ade76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267967"
---
# <span data-ttu-id="26c15-101">Remove-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="26c15-101">Remove-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="26c15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26c15-102">SYNOPSIS</span></span>
<span data-ttu-id="26c15-103">Olay tetikleyicisini dış hizmet olaylarına aboneliğini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="26c15-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="26c15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26c15-104">SYNTAX</span></span>

### <span data-ttu-id="26c15-105">RemoveByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26c15-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c15-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="26c15-106">RemoveByObject</span></span>
```
Remove-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26c15-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="26c15-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26c15-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="26c15-108">DESCRIPTION</span></span>
<span data-ttu-id="26c15-109">**Remove-AzSynapseTriggerSubscription** cmdlet 'i tetik tanımı 'ndan belirtilen dış hizmet olaylarına olay tetiği aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26c15-109">The **Remove-AzSynapseTriggerSubscription** cmdlet unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="26c15-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26c15-110">EXAMPLES</span></span>

### <span data-ttu-id="26c15-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="26c15-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="26c15-112">Bu komut, ContosoTrigger adındaki tetik adındaki tetik 'i tetik tanımı</span><span class="sxs-lookup"><span data-stu-id="26c15-112">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="26c15-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="26c15-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="26c15-114">Bu komut, Contosotetikleyicisi adındaki bir etkinlik aboneliğini, belirtilen olaylarla ardışık düzen aracılığıyla tetikleyerek tetikler.</span><span class="sxs-lookup"><span data-stu-id="26c15-114">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="26c15-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="26c15-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTriggerSubscription
```

<span data-ttu-id="26c15-116">Bu komut, Contosotetikleyicisi adındaki bir etkinlik aboneliğini, belirtilen olaylarla ardışık düzen aracılığıyla tetikleyerek tetikler.</span><span class="sxs-lookup"><span data-stu-id="26c15-116">This command will unsubscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="26c15-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26c15-117">PARAMETERS</span></span>

### <span data-ttu-id="26c15-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="26c15-118">-AsJob</span></span>
<span data-ttu-id="26c15-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="26c15-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26c15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c15-120">-DefaultProfile</span></span>
<span data-ttu-id="26c15-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26c15-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26c15-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26c15-122">-InputObject</span></span>
<span data-ttu-id="26c15-123">Tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="26c15-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26c15-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="26c15-124">-Name</span></span>
<span data-ttu-id="26c15-125">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="26c15-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26c15-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="26c15-126">-PassThru</span></span>
<span data-ttu-id="26c15-127">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="26c15-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="26c15-128">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="26c15-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="26c15-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="26c15-129">-WorkspaceName</span></span>
<span data-ttu-id="26c15-130">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="26c15-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="26c15-131">-</span><span class="sxs-lookup"><span data-stu-id="26c15-131">-WorkspaceObject</span></span>
<span data-ttu-id="26c15-132">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="26c15-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="26c15-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="26c15-133">-Confirm</span></span>
<span data-ttu-id="26c15-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26c15-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26c15-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26c15-135">-WhatIf</span></span>
<span data-ttu-id="26c15-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26c15-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26c15-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26c15-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26c15-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c15-138">CommonParameters</span></span>
<span data-ttu-id="26c15-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26c15-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c15-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="26c15-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c15-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26c15-141">INPUTS</span></span>

### <span data-ttu-id="26c15-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="26c15-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="26c15-143">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerresource</span><span class="sxs-lookup"><span data-stu-id="26c15-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="26c15-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26c15-144">OUTPUTS</span></span>

### <span data-ttu-id="26c15-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26c15-145">System.Boolean</span></span>

## <span data-ttu-id="26c15-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26c15-146">NOTES</span></span>

## <span data-ttu-id="26c15-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26c15-147">RELATED LINKS</span></span>
