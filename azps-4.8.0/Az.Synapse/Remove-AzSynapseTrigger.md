---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseTrigger.md
ms.openlocfilehash: 0882789e230c012fe9f23dcdbeeb5378e9b91781
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268943"
---
# <span data-ttu-id="a4b8e-101">Remove-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="a4b8e-101">Remove-AzSynapseTrigger</span></span>

## <span data-ttu-id="a4b8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b8e-103">Çalışma alanından tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-103">Removes a trigger from a workspace.</span></span>

## <span data-ttu-id="a4b8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4b8e-104">SYNTAX</span></span>

### <span data-ttu-id="a4b8e-105">RemoveByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a4b8e-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseTrigger -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4b8e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="a4b8e-106">RemoveByObject</span></span>
```
Remove-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4b8e-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a4b8e-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseTrigger -InputObject <PSTriggerResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4b8e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4b8e-108">DESCRIPTION</span></span>
<span data-ttu-id="a4b8e-109">**Remove-AzSynapseTrigger** cmdlet 'i çalışma alanından bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-109">The **Remove-AzSynapseTrigger** cmdlet removes a trigger from a workspace.</span></span>

## <span data-ttu-id="a4b8e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4b8e-110">EXAMPLES</span></span>

### <span data-ttu-id="a4b8e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a4b8e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
```

<span data-ttu-id="a4b8e-112">Contosotrigger adındaki bir tetikleyiciyi çalışma alanı contoso</span><span class="sxs-lookup"><span data-stu-id="a4b8e-112">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="a4b8e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a4b8e-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseTrigger -Name ContosoTrigger
```

<span data-ttu-id="a4b8e-114">Çalışma alanı 'nda ContosoTrigger adındaki bir tetikleyiciyi ardışık düzen aracılığıyla kaldırma.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-114">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="a4b8e-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a4b8e-115">Example 3</span></span>
```powershell
PS C:\> $trigger = Get-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger
PS C:\> $trigger | Remove-AzSynapseTrigger
```

<span data-ttu-id="a4b8e-116">Çalışma alanı 'nda ContosoTrigger adındaki bir tetikleyiciyi ardışık düzen aracılığıyla kaldırma.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-116">Remove a trigger called ContosoTrigger from the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a4b8e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4b8e-117">PARAMETERS</span></span>

### <span data-ttu-id="a4b8e-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="a4b8e-118">-AsJob</span></span>
<span data-ttu-id="a4b8e-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a4b8e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4b8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b8e-120">-DefaultProfile</span></span>
<span data-ttu-id="a4b8e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4b8e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4b8e-122">-InputObject</span></span>
<span data-ttu-id="a4b8e-123">Tetik nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-123">The trigger object.</span></span>

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

### <span data-ttu-id="a4b8e-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="a4b8e-124">-Name</span></span>
<span data-ttu-id="a4b8e-125">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-125">The trigger name.</span></span>

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

### <span data-ttu-id="a4b8e-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a4b8e-126">-PassThru</span></span>
<span data-ttu-id="a4b8e-127">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a4b8e-128">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a4b8e-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="a4b8e-129">-WorkspaceName</span></span>
<span data-ttu-id="a4b8e-130">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a4b8e-131">-</span><span class="sxs-lookup"><span data-stu-id="a4b8e-131">-WorkspaceObject</span></span>
<span data-ttu-id="a4b8e-132">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a4b8e-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="a4b8e-133">-Confirm</span></span>
<span data-ttu-id="a4b8e-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4b8e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b8e-135">-WhatIf</span></span>
<span data-ttu-id="a4b8e-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4b8e-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4b8e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b8e-138">CommonParameters</span></span>
<span data-ttu-id="a4b8e-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b8e-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a4b8e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b8e-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4b8e-141">INPUTS</span></span>

### <span data-ttu-id="a4b8e-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a4b8e-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a4b8e-143">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerresource</span><span class="sxs-lookup"><span data-stu-id="a4b8e-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="a4b8e-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4b8e-144">OUTPUTS</span></span>

### <span data-ttu-id="a4b8e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4b8e-145">System.Boolean</span></span>

## <span data-ttu-id="a4b8e-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4b8e-146">NOTES</span></span>

## <span data-ttu-id="a4b8e-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4b8e-147">RELATED LINKS</span></span>
