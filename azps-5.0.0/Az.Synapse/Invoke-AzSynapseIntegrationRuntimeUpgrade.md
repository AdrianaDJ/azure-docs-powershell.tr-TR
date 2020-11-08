---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275164"
---
# <span data-ttu-id="5eb68-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="5eb68-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="5eb68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eb68-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb68-103">Self ile barındırılan tümleştirme çalışma zamanını yükseltir.</span><span class="sxs-lookup"><span data-stu-id="5eb68-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="5eb68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5eb68-104">SYNTAX</span></span>

### <span data-ttu-id="5eb68-105">Invokebynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5eb68-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eb68-106">Invokebyparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="5eb68-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eb68-107">Invokebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5eb68-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eb68-108">Invokebyinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="5eb68-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eb68-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5eb68-109">DESCRIPTION</span></span>
<span data-ttu-id="5eb68-110">**Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet 'i, yeni sürüm kullanılabiliyorsa kendi içinde barındırılan tümleştirme çalışma zamanını yükseltir.</span><span class="sxs-lookup"><span data-stu-id="5eb68-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="5eb68-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5eb68-111">EXAMPLES</span></span>

### <span data-ttu-id="5eb68-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5eb68-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="5eb68-113">Cmdlet, çalışma alanı 'nda ' test-Selfhost-IR ' adlı Self olarak barındırılan tümleştirme çalışma zamanını yükseltir.</span><span class="sxs-lookup"><span data-stu-id="5eb68-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="5eb68-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5eb68-114">PARAMETERS</span></span>

### <span data-ttu-id="5eb68-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb68-115">-DefaultProfile</span></span>
<span data-ttu-id="5eb68-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5eb68-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eb68-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5eb68-117">-InputObject</span></span>
<span data-ttu-id="5eb68-118">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5eb68-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb68-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5eb68-119">-Name</span></span>
<span data-ttu-id="5eb68-120">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="5eb68-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb68-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb68-121">-ResourceGroupName</span></span>
<span data-ttu-id="5eb68-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5eb68-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb68-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5eb68-123">-ResourceId</span></span>
<span data-ttu-id="5eb68-124">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="5eb68-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb68-125">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="5eb68-125">-WorkspaceName</span></span>
<span data-ttu-id="5eb68-126">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="5eb68-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb68-127">-</span><span class="sxs-lookup"><span data-stu-id="5eb68-127">-WorkspaceObject</span></span>
<span data-ttu-id="5eb68-128">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="5eb68-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb68-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5eb68-129">-Confirm</span></span>
<span data-ttu-id="5eb68-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5eb68-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eb68-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb68-131">-WhatIf</span></span>
<span data-ttu-id="5eb68-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5eb68-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eb68-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5eb68-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eb68-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb68-134">CommonParameters</span></span>
<span data-ttu-id="5eb68-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5eb68-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb68-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5eb68-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb68-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5eb68-137">INPUTS</span></span>

### <span data-ttu-id="5eb68-138">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5eb68-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5eb68-139">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="5eb68-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5eb68-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5eb68-140">OUTPUTS</span></span>

### <span data-ttu-id="5eb68-141">System. void</span><span class="sxs-lookup"><span data-stu-id="5eb68-141">System.Void</span></span>

## <span data-ttu-id="5eb68-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5eb68-142">NOTES</span></span>

## <span data-ttu-id="5eb68-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5eb68-143">RELATED LINKS</span></span>
