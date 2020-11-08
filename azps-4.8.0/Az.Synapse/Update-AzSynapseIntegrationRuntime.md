---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 31647da87319ca6be90962f34d128f5e2c922d47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109338"
---
# <span data-ttu-id="e410d-101">Update-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e410d-101">Update-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="e410d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e410d-102">SYNOPSIS</span></span>
<span data-ttu-id="e410d-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e410d-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="e410d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e410d-104">SYNTAX</span></span>

### <span data-ttu-id="e410d-105">UpdateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e410d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e410d-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e410d-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e410d-107">Updatebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e410d-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -ResourceId <String> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e410d-108">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e410d-108">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-AutoUpdate <String>]
 [-AutoUpdateDelayOffset <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e410d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e410d-109">DESCRIPTION</span></span>
<span data-ttu-id="e410d-110">**Update-AzSynapseIntegrationRuntime** cmdlet 'i Integration Runtime özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="e410d-110">The **Update-AzSynapseIntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="e410d-111">Şu anda cmdlet, self-hosted Integration Runtime için yalnızca ' otomatik güncelleştirme ' ve ' AutoUpdateDelayOffset ' güncelleştirmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="e410d-111">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="e410d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e410d-112">EXAMPLES</span></span>

### <span data-ttu-id="e410d-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e410d-113">Example 1</span></span>
```powershell
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -AutoUpdate Off -AutoUpdateDelayOffset $ts
```

<span data-ttu-id="e410d-114">Cmdlet, ' test-Selfhost-IR ' adlı Self olarak barındırılan tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e410d-114">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="e410d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e410d-115">PARAMETERS</span></span>

### <span data-ttu-id="e410d-116">-Otomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e410d-116">-AutoUpdate</span></span>
<span data-ttu-id="e410d-117">Self-hosted Integration Runtime otomatik güncelleştirmesini etkinleştirin veya devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="e410d-117">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e410d-118">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="e410d-118">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="e410d-119">Self-hosted Integration Runtime otomatik güncelleştirmesi için günün saati.</span><span class="sxs-lookup"><span data-stu-id="e410d-119">The time of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e410d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e410d-120">-DefaultProfile</span></span>
<span data-ttu-id="e410d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e410d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e410d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e410d-122">-InputObject</span></span>
<span data-ttu-id="e410d-123">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e410d-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="e410d-124">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="e410d-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="e410d-125">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="e410d-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="e410d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e410d-126">-ResourceGroupName</span></span>
<span data-ttu-id="e410d-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e410d-127">Resource group name.</span></span>

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

### <span data-ttu-id="e410d-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e410d-128">-ResourceId</span></span>
<span data-ttu-id="e410d-129">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e410d-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="e410d-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e410d-130">-WorkspaceName</span></span>
<span data-ttu-id="e410d-131">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="e410d-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="e410d-132">-</span><span class="sxs-lookup"><span data-stu-id="e410d-132">-WorkspaceObject</span></span>
<span data-ttu-id="e410d-133">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="e410d-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="e410d-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e410d-134">-Confirm</span></span>
<span data-ttu-id="e410d-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e410d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e410d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e410d-136">-WhatIf</span></span>
<span data-ttu-id="e410d-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e410d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e410d-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e410d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e410d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e410d-139">CommonParameters</span></span>
<span data-ttu-id="e410d-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e410d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e410d-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e410d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e410d-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e410d-142">INPUTS</span></span>

### <span data-ttu-id="e410d-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e410d-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="e410d-144">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="e410d-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e410d-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e410d-145">OUTPUTS</span></span>

### <span data-ttu-id="e410d-146">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="e410d-146">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="e410d-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e410d-147">NOTES</span></span>

## <span data-ttu-id="e410d-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e410d-148">RELATED LINKS</span></span>
