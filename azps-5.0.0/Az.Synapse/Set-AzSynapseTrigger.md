---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseTrigger.md
ms.openlocfilehash: 289e601ab80e4842b493cd6852839bec544bcc36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324859"
---
# <span data-ttu-id="fce5b-101">Set-AzSynapseTrigger</span><span class="sxs-lookup"><span data-stu-id="fce5b-101">Set-AzSynapseTrigger</span></span>

## <span data-ttu-id="fce5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fce5b-102">SYNOPSIS</span></span>
<span data-ttu-id="fce5b-103">Çalışma alanında tetik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fce5b-103">Creates a trigger in a workspace.</span></span>

## <span data-ttu-id="fce5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fce5b-104">SYNTAX</span></span>

### <span data-ttu-id="fce5b-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fce5b-105">SetByName (Default)</span></span>
```
Set-AzSynapseTrigger -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fce5b-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="fce5b-106">SetByObject</span></span>
```
Set-AzSynapseTrigger -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fce5b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fce5b-107">DESCRIPTION</span></span>
<span data-ttu-id="fce5b-108">**Set-AzSynapseTrigger** cmdlet 'i çalışma alanında bir tetik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fce5b-108">The **Set-AzSynapseTrigger** cmdlet creates a trigger in a workspace.</span></span> <span data-ttu-id="fce5b-109">Tetikleyiciler ' durduruldu ' durumunda oluşturulur ve bunların başvuruda bulundukları ardışık düzenleri hemen çağırmaya başlamalardır.</span><span class="sxs-lookup"><span data-stu-id="fce5b-109">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="fce5b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fce5b-110">EXAMPLES</span></span>

### <span data-ttu-id="fce5b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fce5b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseTrigger -WorkspaceName ContosoWorkspace -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="fce5b-112">Çalışma alanında ContosoTrigger adındaki yeni bir tetik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fce5b-112">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace.</span></span> <span data-ttu-id="fce5b-113">Tetik ' durduruldu ' durumunda oluşturulur ve bu da hemen başlamadır.</span><span class="sxs-lookup"><span data-stu-id="fce5b-113">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="fce5b-114">Tetik cmdlet kullanılarak başlatılabilir `Start-AzDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="fce5b-114">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

### <span data-ttu-id="fce5b-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fce5b-115">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseTrigger -Name ContosoTrigger -DefinitionFile ".\scheduledTrigger.json"
```

<span data-ttu-id="fce5b-116">Çalışma alanında, ardışık düzen aracılığıyla ContosoTrigger tetikleyicisi adındaki yeni bir tetik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fce5b-116">Create a new trigger called ContosoTrigger in the workspace ContosoWorkspace through pipeline.</span></span> <span data-ttu-id="fce5b-117">Tetik ' durduruldu ' durumunda oluşturulur ve bu da hemen başlamadır.</span><span class="sxs-lookup"><span data-stu-id="fce5b-117">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="fce5b-118">Tetik cmdlet kullanılarak başlatılabilir `Start-AzDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="fce5b-118">A trigger can be started using the `Start-AzDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="fce5b-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fce5b-119">PARAMETERS</span></span>

### <span data-ttu-id="fce5b-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="fce5b-120">-AsJob</span></span>
<span data-ttu-id="fce5b-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fce5b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fce5b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce5b-122">-DefaultProfile</span></span>
<span data-ttu-id="fce5b-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fce5b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fce5b-124">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="fce5b-124">-DefinitionFile</span></span>
<span data-ttu-id="fce5b-125">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="fce5b-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce5b-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="fce5b-126">-Name</span></span>
<span data-ttu-id="fce5b-127">Tetik adı.</span><span class="sxs-lookup"><span data-stu-id="fce5b-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce5b-128">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="fce5b-128">-WorkspaceName</span></span>
<span data-ttu-id="fce5b-129">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="fce5b-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce5b-130">-</span><span class="sxs-lookup"><span data-stu-id="fce5b-130">-WorkspaceObject</span></span>
<span data-ttu-id="fce5b-131">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="fce5b-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fce5b-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="fce5b-132">-Confirm</span></span>
<span data-ttu-id="fce5b-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fce5b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fce5b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fce5b-134">-WhatIf</span></span>
<span data-ttu-id="fce5b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fce5b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fce5b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fce5b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fce5b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce5b-137">CommonParameters</span></span>
<span data-ttu-id="fce5b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fce5b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce5b-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fce5b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce5b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fce5b-140">INPUTS</span></span>

### <span data-ttu-id="fce5b-141">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fce5b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fce5b-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fce5b-142">OUTPUTS</span></span>

### <span data-ttu-id="fce5b-143">Microsoft. Azure. Commands. SYNAPSE. modeller. Pçarpıcı Ggerresource</span><span class="sxs-lookup"><span data-stu-id="fce5b-143">Microsoft.Azure.Commands.Synapse.Models.PSTriggerResource</span></span>

## <span data-ttu-id="fce5b-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fce5b-144">NOTES</span></span>

## <span data-ttu-id="fce5b-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fce5b-145">RELATED LINKS</span></span>
