---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275996"
---
# <span data-ttu-id="58ad8-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="58ad8-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="58ad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="58ad8-103">Self-hosted Integration Runtime için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="58ad8-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="58ad8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58ad8-104">SYNTAX</span></span>

### <span data-ttu-id="58ad8-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58ad8-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58ad8-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58ad8-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58ad8-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="58ad8-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58ad8-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58ad8-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58ad8-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="58ad8-109">DESCRIPTION</span></span>
<span data-ttu-id="58ad8-110">**Get-AzSynapseIntegrationRuntimeKey** cmdlet 'i Integration Runtime için anahtarlar alır.</span><span class="sxs-lookup"><span data-stu-id="58ad8-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="58ad8-111">Anahtarlar, tümleştirme çalışma zamanı düğümünü kaydettirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="58ad8-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="58ad8-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58ad8-112">EXAMPLES</span></span>

### <span data-ttu-id="58ad8-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="58ad8-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="58ad8-114">Cmdlet ' test-Selfhost-IR ' adlı bir tümleştirme çalışma zamanı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="58ad8-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="58ad8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58ad8-115">PARAMETERS</span></span>

### <span data-ttu-id="58ad8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ad8-116">-DefaultProfile</span></span>
<span data-ttu-id="58ad8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58ad8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58ad8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58ad8-118">-InputObject</span></span>
<span data-ttu-id="58ad8-119">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="58ad8-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="58ad8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="58ad8-120">-Name</span></span>
<span data-ttu-id="58ad8-121">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="58ad8-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="58ad8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ad8-122">-ResourceGroupName</span></span>
<span data-ttu-id="58ad8-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="58ad8-123">Resource group name.</span></span>

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

### <span data-ttu-id="58ad8-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="58ad8-124">-ResourceId</span></span>
<span data-ttu-id="58ad8-125">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="58ad8-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="58ad8-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="58ad8-126">-WorkspaceName</span></span>
<span data-ttu-id="58ad8-127">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="58ad8-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="58ad8-128">-</span><span class="sxs-lookup"><span data-stu-id="58ad8-128">-WorkspaceObject</span></span>
<span data-ttu-id="58ad8-129">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="58ad8-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="58ad8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ad8-130">CommonParameters</span></span>
<span data-ttu-id="58ad8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58ad8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ad8-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="58ad8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ad8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58ad8-133">INPUTS</span></span>

### <span data-ttu-id="58ad8-134">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="58ad8-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="58ad8-135">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="58ad8-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="58ad8-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58ad8-136">OUTPUTS</span></span>

### <span data-ttu-id="58ad8-137">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntimekeys</span><span class="sxs-lookup"><span data-stu-id="58ad8-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="58ad8-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58ad8-138">NOTES</span></span>

## <span data-ttu-id="58ad8-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58ad8-139">RELATED LINKS</span></span>
