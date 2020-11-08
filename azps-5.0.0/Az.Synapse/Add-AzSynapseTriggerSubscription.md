---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/add-azsynapsetriggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Add-AzSynapseTriggerSubscription.md
ms.openlocfilehash: ca5501115b7c75b2e3c1baca368ebaac841e0ae1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277965"
---
# <span data-ttu-id="1701b-101">Add-AzSynapseTriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="1701b-101">Add-AzSynapseTriggerSubscription</span></span>

## <span data-ttu-id="1701b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1701b-102">SYNOPSIS</span></span>
<span data-ttu-id="1701b-103">Olay tetikleyicisini dış hizmet olaylarına abone olun.</span><span class="sxs-lookup"><span data-stu-id="1701b-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="1701b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1701b-104">SYNTAX</span></span>

### <span data-ttu-id="1701b-105">AddByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1701b-105">AddByName (Default)</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1701b-106">AddByObject</span><span class="sxs-lookup"><span data-stu-id="1701b-106">AddByObject</span></span>
```
Add-AzSynapseTriggerSubscription -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1701b-107">AddByInputObject</span><span class="sxs-lookup"><span data-stu-id="1701b-107">AddByInputObject</span></span>
```
Add-AzSynapseTriggerSubscription -InputObject <PSTriggerResource> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1701b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1701b-108">DESCRIPTION</span></span>
<span data-ttu-id="1701b-109">**Add-AzSynapseTriggerSubscription** cmdlet 'i tetik tanımı 'ndan belirtilen dış hizmet olaylarına olay tetikleyicisini abone olur.</span><span class="sxs-lookup"><span data-stu-id="1701b-109">The **Add-AzSynapseTriggerSubscription** cmdlet subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="1701b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1701b-110">EXAMPLES</span></span>

### <span data-ttu-id="1701b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1701b-111">Example 1</span></span>
```powershell
PS C:\> Add-AzSynapseTriggerSubscription -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="1701b-112">Bu komut, ContosoTrigger adındaki tetik 'i tetik tanımı 'ndan belirtilen olaylara abone olur.</span><span class="sxs-lookup"><span data-stu-id="1701b-112">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion.</span></span>

### <span data-ttu-id="1701b-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1701b-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Add-AzSynapseTriggerSubscription -Name ContosoTrigger
```

<span data-ttu-id="1701b-114">Bu komut, ContosoTrigger adındaki tetikleyiciye, ardışık düzene göre tetik ile belirtilen olaylara abone olur.</span><span class="sxs-lookup"><span data-stu-id="1701b-114">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

### <span data-ttu-id="1701b-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1701b-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Add-AzSynapseTriggerSubscription
```

<span data-ttu-id="1701b-116">Bu komut, ContosoTrigger adındaki tetikleyiciye, ardışık düzene göre tetik ile belirtilen olaylara abone olur.</span><span class="sxs-lookup"><span data-stu-id="1701b-116">This command will subscribe trigger called ContosoTrigger to the specified events from the trigger defintion through pipeline.</span></span>

## <span data-ttu-id="1701b-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1701b-117">PARAMETERS</span></span>

### <span data-ttu-id="1701b-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="1701b-118">-AsJob</span></span>
<span data-ttu-id="1701b-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1701b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1701b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1701b-120">-DefaultProfile</span></span>
<span data-ttu-id="1701b-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1701b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1701b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1701b-122">-InputObject</span></span>
<span data-ttu-id="1701b-123">Tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1701b-123">The trigger object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource
Parameter Sets: AddByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1701b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1701b-124">-Name</span></span>
<span data-ttu-id="1701b-125">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="1701b-125">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName, AddByObject
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1701b-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="1701b-126">-WorkspaceName</span></span>
<span data-ttu-id="1701b-127">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="1701b-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: AddByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1701b-128">-</span><span class="sxs-lookup"><span data-stu-id="1701b-128">-WorkspaceObject</span></span>
<span data-ttu-id="1701b-129">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="1701b-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: AddByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1701b-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="1701b-130">-Confirm</span></span>
<span data-ttu-id="1701b-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1701b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1701b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1701b-132">-WhatIf</span></span>
<span data-ttu-id="1701b-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1701b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1701b-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1701b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1701b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1701b-135">CommonParameters</span></span>
<span data-ttu-id="1701b-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1701b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1701b-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1701b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1701b-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1701b-138">INPUTS</span></span>

### <span data-ttu-id="1701b-139">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1701b-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1701b-140">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerresource</span><span class="sxs-lookup"><span data-stu-id="1701b-140">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="1701b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1701b-141">OUTPUTS</span></span>

### <span data-ttu-id="1701b-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="1701b-142">System.Object</span></span>
## <span data-ttu-id="1701b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1701b-143">NOTES</span></span>

## <span data-ttu-id="1701b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1701b-144">RELATED LINKS</span></span>
