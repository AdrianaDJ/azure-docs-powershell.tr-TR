---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 4192350397a9ba23e57b77b017ff7409afac7a39
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275147"
---
# <span data-ttu-id="3ca0a-101">Update-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="3ca0a-101">Update-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="3ca0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca0a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca0a-103">Self-hosted Integration Runtime düğümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="3ca0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ca0a-104">SYNTAX</span></span>

### <span data-ttu-id="3ca0a-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ca0a-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca0a-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca0a-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ca0a-107">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3ca0a-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> -ConcurrentJobsLimit <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca0a-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca0a-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String>
 -ConcurrentJobsLimit <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ca0a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ca0a-109">DESCRIPTION</span></span>
<span data-ttu-id="3ca0a-110">**Update-AzSynapseIntegrationRuntimeNode** cmdlet 'i, çalışma alanındaki self-hosted Integration Runtime düğümünün özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-110">The **Update-AzSynapseIntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a workspace.</span></span> <span data-ttu-id="3ca0a-111">Şu anda yalnızca ' Concurrentjobslimıt ' güncelleştirmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-111">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="3ca0a-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ca0a-112">EXAMPLES</span></span>

### <span data-ttu-id="3ca0a-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3ca0a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -ConcurrentJobsLimit 3
```

<span data-ttu-id="3ca0a-114">Cmdlet, Self ile barındırılan tümleştirme çalışma zamanı ' test-Selfhost-IR ' ' Node_1</span><span class="sxs-lookup"><span data-stu-id="3ca0a-114">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="3ca0a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ca0a-115">PARAMETERS</span></span>

### <span data-ttu-id="3ca0a-116">-Concurrentjobslimıt</span><span class="sxs-lookup"><span data-stu-id="3ca0a-116">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="3ca0a-117">Tümleştirme çalışma zamanı düğümünde çalışmasına izin verilen eşzamanlı iş sayısı.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-117">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="3ca0a-118">1 ila maxConcurrentJobs değerlerine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-118">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca0a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca0a-119">-DefaultProfile</span></span>
<span data-ttu-id="3ca0a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca0a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca0a-121">-InputObject</span></span>
<span data-ttu-id="3ca0a-122">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-122">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca0a-123">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="3ca0a-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="3ca0a-124">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca0a-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ca0a-125">-Name</span></span>
<span data-ttu-id="3ca0a-126">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="3ca0a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca0a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ca0a-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca0a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3ca0a-129">-ResourceId</span></span>
<span data-ttu-id="3ca0a-130">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca0a-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="3ca0a-131">-WorkspaceName</span></span>
<span data-ttu-id="3ca0a-132">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca0a-133">-</span><span class="sxs-lookup"><span data-stu-id="3ca0a-133">-WorkspaceObject</span></span>
<span data-ttu-id="3ca0a-134">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca0a-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="3ca0a-135">-Confirm</span></span>
<span data-ttu-id="3ca0a-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca0a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca0a-137">-WhatIf</span></span>
<span data-ttu-id="3ca0a-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca0a-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca0a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca0a-140">CommonParameters</span></span>
<span data-ttu-id="3ca0a-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca0a-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3ca0a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca0a-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ca0a-143">INPUTS</span></span>

### <span data-ttu-id="3ca0a-144">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ca0a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="3ca0a-145">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="3ca0a-145">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3ca0a-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ca0a-146">OUTPUTS</span></span>

### <span data-ttu-id="3ca0a-147">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="3ca0a-147">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="3ca0a-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ca0a-148">NOTES</span></span>

## <span data-ttu-id="3ca0a-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ca0a-149">RELATED LINKS</span></span>
