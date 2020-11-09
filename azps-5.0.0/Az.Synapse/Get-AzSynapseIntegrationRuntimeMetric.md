---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324202"
---
# <span data-ttu-id="b359e-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="b359e-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="b359e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b359e-102">SYNOPSIS</span></span>
<span data-ttu-id="b359e-103">Tümleştirme çalışma zamanı için ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b359e-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="b359e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b359e-104">SYNTAX</span></span>

### <span data-ttu-id="b359e-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b359e-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b359e-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b359e-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b359e-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b359e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b359e-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b359e-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b359e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b359e-109">DESCRIPTION</span></span>
<span data-ttu-id="b359e-110">**Get-AzSynapseIntegrationRuntimeMetric** cmdlet 'i, çalışma alanındaki tümleştirme çalışma zamanı hakkında ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b359e-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="b359e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b359e-111">EXAMPLES</span></span>

### <span data-ttu-id="b359e-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b359e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="b359e-113">Bu komut, ContosoWorkspace adlı çalışma alanındaki ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanı hakkında ölçüm verilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b359e-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="b359e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b359e-114">PARAMETERS</span></span>

### <span data-ttu-id="b359e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b359e-115">-DefaultProfile</span></span>
<span data-ttu-id="b359e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b359e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b359e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b359e-117">-InputObject</span></span>
<span data-ttu-id="b359e-118">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b359e-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b359e-119">-Name</span></span>
<span data-ttu-id="b359e-120">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="b359e-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b359e-121">-ResourceGroupName</span></span>
<span data-ttu-id="b359e-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b359e-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b359e-123">-ResourceId</span></span>
<span data-ttu-id="b359e-124">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b359e-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-125">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="b359e-125">-WorkspaceName</span></span>
<span data-ttu-id="b359e-126">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="b359e-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-127">-</span><span class="sxs-lookup"><span data-stu-id="b359e-127">-WorkspaceObject</span></span>
<span data-ttu-id="b359e-128">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="b359e-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b359e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b359e-129">CommonParameters</span></span>
<span data-ttu-id="b359e-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b359e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b359e-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b359e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b359e-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b359e-132">INPUTS</span></span>

### <span data-ttu-id="b359e-133">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b359e-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b359e-134">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="b359e-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b359e-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b359e-135">OUTPUTS</span></span>

### <span data-ttu-id="b359e-136">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntimeölçüler</span><span class="sxs-lookup"><span data-stu-id="b359e-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="b359e-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b359e-137">NOTES</span></span>

## <span data-ttu-id="b359e-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b359e-138">RELATED LINKS</span></span>
