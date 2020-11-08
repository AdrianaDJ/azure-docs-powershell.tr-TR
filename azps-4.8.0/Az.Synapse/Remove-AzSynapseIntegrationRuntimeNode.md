---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109912"
---
# <span data-ttu-id="23306-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="23306-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="23306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23306-102">SYNOPSIS</span></span>
<span data-ttu-id="23306-103">Tümleştirme çalışma zamanında verilen ada sahip düğümü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="23306-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="23306-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23306-104">SYNTAX</span></span>

### <span data-ttu-id="23306-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="23306-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23306-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23306-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23306-107">Removebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="23306-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23306-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23306-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23306-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="23306-109">DESCRIPTION</span></span>
<span data-ttu-id="23306-110">**Remove-AzSynapseIntegrationRuntimeNode** cmdlet 'i Integration Runtime 'de bir düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="23306-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="23306-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23306-111">EXAMPLES</span></span>

### <span data-ttu-id="23306-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="23306-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="23306-113">Tümleştirme çalışma zamanında verilen ada sahip düğümü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="23306-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="23306-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23306-114">PARAMETERS</span></span>

### <span data-ttu-id="23306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23306-115">-DefaultProfile</span></span>
<span data-ttu-id="23306-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23306-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23306-117">-Force</span><span class="sxs-lookup"><span data-stu-id="23306-117">-Force</span></span>
<span data-ttu-id="23306-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="23306-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="23306-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23306-119">-InputObject</span></span>
<span data-ttu-id="23306-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="23306-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="23306-121">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="23306-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="23306-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="23306-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23306-123">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="23306-123">-NodeName</span></span>
<span data-ttu-id="23306-124">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="23306-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23306-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23306-125">-ResourceGroupName</span></span>
<span data-ttu-id="23306-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="23306-126">Resource group name.</span></span>

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

### <span data-ttu-id="23306-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="23306-127">-ResourceId</span></span>
<span data-ttu-id="23306-128">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="23306-128">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="23306-129">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="23306-129">-WorkspaceName</span></span>
<span data-ttu-id="23306-130">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="23306-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="23306-131">-</span><span class="sxs-lookup"><span data-stu-id="23306-131">-WorkspaceObject</span></span>
<span data-ttu-id="23306-132">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="23306-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="23306-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="23306-133">-Confirm</span></span>
<span data-ttu-id="23306-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23306-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23306-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23306-135">-WhatIf</span></span>
<span data-ttu-id="23306-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23306-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23306-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23306-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23306-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23306-138">CommonParameters</span></span>
<span data-ttu-id="23306-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23306-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23306-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="23306-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23306-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23306-141">INPUTS</span></span>

### <span data-ttu-id="23306-142">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="23306-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="23306-143">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="23306-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="23306-144">System. String</span><span class="sxs-lookup"><span data-stu-id="23306-144">System.String</span></span>

## <span data-ttu-id="23306-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23306-145">OUTPUTS</span></span>

### <span data-ttu-id="23306-146">System. void</span><span class="sxs-lookup"><span data-stu-id="23306-146">System.Void</span></span>

## <span data-ttu-id="23306-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23306-147">NOTES</span></span>

## <span data-ttu-id="23306-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23306-148">RELATED LINKS</span></span>
