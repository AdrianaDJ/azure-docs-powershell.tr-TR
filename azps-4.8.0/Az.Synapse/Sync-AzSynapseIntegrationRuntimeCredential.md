---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107462"
---
# <span data-ttu-id="96482-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="96482-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="96482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96482-102">SYNOPSIS</span></span>
<span data-ttu-id="96482-103">Tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="96482-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="96482-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96482-104">SYNTAX</span></span>

### <span data-ttu-id="96482-105">StopByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="96482-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96482-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96482-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96482-107">Stopbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="96482-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96482-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96482-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96482-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="96482-109">DESCRIPTION</span></span>
<span data-ttu-id="96482-110">**Sync-AzSynapseIntegrationRuntimeCredential** cmdlet 'i tümleştirme çalışma zamanı düğümleri arasında Şirket içi kimlik bilgilerini eşitler ve bu da tüm düğümlerde aynı kimlik bilgilerini özdeş hale getirir.</span><span class="sxs-lookup"><span data-stu-id="96482-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="96482-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96482-111">EXAMPLES</span></span>

### <span data-ttu-id="96482-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="96482-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="96482-113">Tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="96482-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="96482-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96482-114">PARAMETERS</span></span>

### <span data-ttu-id="96482-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96482-115">-DefaultProfile</span></span>
<span data-ttu-id="96482-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96482-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96482-117">-Force</span><span class="sxs-lookup"><span data-stu-id="96482-117">-Force</span></span>
<span data-ttu-id="96482-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="96482-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="96482-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96482-119">-InputObject</span></span>
<span data-ttu-id="96482-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="96482-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="96482-121">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="96482-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="96482-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="96482-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="96482-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96482-123">-ResourceGroupName</span></span>
<span data-ttu-id="96482-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="96482-124">Resource group name.</span></span>

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

### <span data-ttu-id="96482-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="96482-125">-ResourceId</span></span>
<span data-ttu-id="96482-126">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="96482-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="96482-127">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="96482-127">-WorkspaceName</span></span>
<span data-ttu-id="96482-128">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="96482-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="96482-129">-</span><span class="sxs-lookup"><span data-stu-id="96482-129">-WorkspaceObject</span></span>
<span data-ttu-id="96482-130">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="96482-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="96482-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="96482-131">-Confirm</span></span>
<span data-ttu-id="96482-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96482-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96482-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96482-133">-WhatIf</span></span>
<span data-ttu-id="96482-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96482-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96482-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96482-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96482-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96482-136">CommonParameters</span></span>
<span data-ttu-id="96482-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96482-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96482-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="96482-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96482-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96482-139">INPUTS</span></span>

### <span data-ttu-id="96482-140">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="96482-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="96482-141">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="96482-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="96482-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96482-142">OUTPUTS</span></span>

### <span data-ttu-id="96482-143">System. void</span><span class="sxs-lookup"><span data-stu-id="96482-143">System.Void</span></span>

## <span data-ttu-id="96482-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96482-144">NOTES</span></span>

## <span data-ttu-id="96482-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96482-145">RELATED LINKS</span></span>
