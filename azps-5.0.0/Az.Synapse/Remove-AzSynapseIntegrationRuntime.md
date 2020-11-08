---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277914"
---
# <span data-ttu-id="57039-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="57039-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="57039-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57039-102">SYNOPSIS</span></span>
<span data-ttu-id="57039-103">Tümleştirme çalışma zamanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57039-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="57039-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57039-104">SYNTAX</span></span>

### <span data-ttu-id="57039-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57039-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57039-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57039-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57039-107">Removebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="57039-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57039-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57039-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57039-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="57039-109">DESCRIPTION</span></span>
<span data-ttu-id="57039-110">**Remove-AzSynapseIntegrationRuntime** cmdlet 'i Integration Runtime 'ı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57039-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="57039-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57039-111">EXAMPLES</span></span>

### <span data-ttu-id="57039-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="57039-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="57039-113">Bu komut, ' test edilmiş-IR ' adlı tümleştirme çalışma zamanını, ContosoWorkspace adlı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="57039-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="57039-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57039-114">PARAMETERS</span></span>

### <span data-ttu-id="57039-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57039-115">-DefaultProfile</span></span>
<span data-ttu-id="57039-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57039-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57039-117">-Force</span><span class="sxs-lookup"><span data-stu-id="57039-117">-Force</span></span>
<span data-ttu-id="57039-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="57039-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="57039-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57039-119">-InputObject</span></span>
<span data-ttu-id="57039-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="57039-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57039-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="57039-121">-Name</span></span>
<span data-ttu-id="57039-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="57039-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57039-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57039-123">-ResourceGroupName</span></span>
<span data-ttu-id="57039-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="57039-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57039-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="57039-125">-ResourceId</span></span>
<span data-ttu-id="57039-126">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="57039-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57039-127">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="57039-127">-WorkspaceName</span></span>
<span data-ttu-id="57039-128">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="57039-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57039-129">-</span><span class="sxs-lookup"><span data-stu-id="57039-129">-WorkspaceObject</span></span>
<span data-ttu-id="57039-130">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="57039-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57039-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="57039-131">-Confirm</span></span>
<span data-ttu-id="57039-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57039-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57039-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57039-133">-WhatIf</span></span>
<span data-ttu-id="57039-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57039-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57039-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57039-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57039-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57039-136">CommonParameters</span></span>
<span data-ttu-id="57039-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57039-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57039-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="57039-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57039-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57039-139">INPUTS</span></span>

### <span data-ttu-id="57039-140">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="57039-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="57039-141">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="57039-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="57039-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57039-142">OUTPUTS</span></span>

### <span data-ttu-id="57039-143">System. void</span><span class="sxs-lookup"><span data-stu-id="57039-143">System.Void</span></span>

## <span data-ttu-id="57039-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57039-144">NOTES</span></span>

## <span data-ttu-id="57039-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57039-145">RELATED LINKS</span></span>
