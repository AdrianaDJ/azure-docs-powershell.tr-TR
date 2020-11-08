---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275160"
---
# <span data-ttu-id="c9c2c-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="c9c2c-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="c9c2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c2c-103">Tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="c9c2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9c2c-104">SYNTAX</span></span>

### <span data-ttu-id="c9c2c-105">StopByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9c2c-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c2c-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c2c-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c2c-107">Stopbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c9c2c-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c2c-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c2c-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c2c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9c2c-109">DESCRIPTION</span></span>
<span data-ttu-id="c9c2c-110">**Sync-AzSynapseIntegrationRuntimeCredential** cmdlet 'i tümleştirme çalışma zamanı düğümleri arasında Şirket içi kimlik bilgilerini eşitler ve bu da tüm düğümlerde aynı kimlik bilgilerini özdeş hale getirir.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="c9c2c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9c2c-111">EXAMPLES</span></span>

### <span data-ttu-id="c9c2c-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c9c2c-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="c9c2c-113">Tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="c9c2c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9c2c-114">PARAMETERS</span></span>

### <span data-ttu-id="c9c2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c2c-115">-DefaultProfile</span></span>
<span data-ttu-id="c9c2c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c2c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c9c2c-117">-Force</span></span>
<span data-ttu-id="c9c2c-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c9c2c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9c2c-119">-InputObject</span></span>
<span data-ttu-id="c9c2c-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c2c-121">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="c9c2c-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="c9c2c-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c2c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c2c-123">-ResourceGroupName</span></span>
<span data-ttu-id="c9c2c-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c2c-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c9c2c-125">-ResourceId</span></span>
<span data-ttu-id="c9c2c-126">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c2c-127">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="c9c2c-127">-WorkspaceName</span></span>
<span data-ttu-id="c9c2c-128">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9c2c-129">-</span><span class="sxs-lookup"><span data-stu-id="c9c2c-129">-WorkspaceObject</span></span>
<span data-ttu-id="c9c2c-130">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9c2c-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9c2c-131">-Confirm</span></span>
<span data-ttu-id="c9c2c-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c2c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c2c-133">-WhatIf</span></span>
<span data-ttu-id="c9c2c-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c2c-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c2c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c2c-136">CommonParameters</span></span>
<span data-ttu-id="c9c2c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c2c-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c9c2c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c2c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9c2c-139">INPUTS</span></span>

### <span data-ttu-id="c9c2c-140">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c9c2c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c9c2c-141">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="c9c2c-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c9c2c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9c2c-142">OUTPUTS</span></span>

### <span data-ttu-id="c9c2c-143">System. void</span><span class="sxs-lookup"><span data-stu-id="c9c2c-143">System.Void</span></span>

## <span data-ttu-id="c9c2c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9c2c-144">NOTES</span></span>

## <span data-ttu-id="c9c2c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9c2c-145">RELATED LINKS</span></span>
