---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeMetric.md
ms.openlocfilehash: 0b6700d11b017f00f10328afae2cc6638087f216
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268644"
---
# <span data-ttu-id="dd4c0-101">Get-AzSynapseIntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="dd4c0-101">Get-AzSynapseIntegrationRuntimeMetric</span></span>

## <span data-ttu-id="dd4c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4c0-103">Tümleştirme çalışma zamanı için ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="dd4c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd4c0-104">SYNTAX</span></span>

### <span data-ttu-id="dd4c0-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd4c0-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd4c0-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd4c0-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd4c0-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dd4c0-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd4c0-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd4c0-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeMetric -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd4c0-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd4c0-109">DESCRIPTION</span></span>
<span data-ttu-id="dd4c0-110">**Get-AzSynapseIntegrationRuntimeMetric** cmdlet 'i, çalışma alanındaki tümleştirme çalışma zamanı hakkında ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-110">The **Get-AzSynapseIntegrationRuntimeMetric** cmdlet gets metric data about integration runtime in a workspace.</span></span>

## <span data-ttu-id="dd4c0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd4c0-111">EXAMPLES</span></span>

### <span data-ttu-id="dd4c0-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd4c0-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeMetric -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="dd4c0-113">Bu komut, ContosoWorkspace adlı çalışma alanındaki ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanı hakkında ölçüm verilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-113">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="dd4c0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd4c0-114">PARAMETERS</span></span>

### <span data-ttu-id="dd4c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4c0-115">-DefaultProfile</span></span>
<span data-ttu-id="dd4c0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd4c0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd4c0-117">-InputObject</span></span>
<span data-ttu-id="dd4c0-118">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="dd4c0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd4c0-119">-Name</span></span>
<span data-ttu-id="dd4c0-120">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="dd4c0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd4c0-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd4c0-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-122">Resource group name.</span></span>

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

### <span data-ttu-id="dd4c0-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dd4c0-123">-ResourceId</span></span>
<span data-ttu-id="dd4c0-124">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-124">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="dd4c0-125">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="dd4c0-125">-WorkspaceName</span></span>
<span data-ttu-id="dd4c0-126">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="dd4c0-127">-</span><span class="sxs-lookup"><span data-stu-id="dd4c0-127">-WorkspaceObject</span></span>
<span data-ttu-id="dd4c0-128">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="dd4c0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4c0-129">CommonParameters</span></span>
<span data-ttu-id="dd4c0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4c0-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4c0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd4c0-132">INPUTS</span></span>

### <span data-ttu-id="dd4c0-133">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dd4c0-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dd4c0-134">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="dd4c0-134">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dd4c0-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd4c0-135">OUTPUTS</span></span>

### <span data-ttu-id="dd4c0-136">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntimeölçüler</span><span class="sxs-lookup"><span data-stu-id="dd4c0-136">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="dd4c0-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd4c0-137">NOTES</span></span>

## <span data-ttu-id="dd4c0-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd4c0-138">RELATED LINKS</span></span>
