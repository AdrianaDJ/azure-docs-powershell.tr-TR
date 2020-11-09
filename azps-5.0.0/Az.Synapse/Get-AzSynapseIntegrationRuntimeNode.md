---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324196"
---
# <span data-ttu-id="45c1f-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="45c1f-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="45c1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="45c1f-103">Tümleştirme çalışma zamanı düğümü bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="45c1f-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="45c1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45c1f-104">SYNTAX</span></span>

### <span data-ttu-id="45c1f-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="45c1f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45c1f-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c1f-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c1f-107">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="45c1f-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c1f-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45c1f-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45c1f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="45c1f-109">DESCRIPTION</span></span>
<span data-ttu-id="45c1f-110">**Get-AzSynapseIntegrationRuntimeNode** cmdlet 'i Integration Runtime düğümünün ayrıntı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="45c1f-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="45c1f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45c1f-111">EXAMPLES</span></span>

### <span data-ttu-id="45c1f-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="45c1f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="45c1f-113">Cmdlet, ' Node_1 ' adlı düğümün çalışma alanı Contosoçalışma zamanında ' test-Selfhost-IR ' adlı düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="45c1f-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="45c1f-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="45c1f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="45c1f-115">Cmdlet, IP adresi de içinde olmak üzere, ' test-df-EU2 ' çalışma alanındaki ' test-Selfhost-IR ' ' Node_1 ' adlı düğümün bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="45c1f-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="45c1f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45c1f-116">PARAMETERS</span></span>

### <span data-ttu-id="45c1f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c1f-117">-DefaultProfile</span></span>
<span data-ttu-id="45c1f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45c1f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c1f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45c1f-119">-InputObject</span></span>
<span data-ttu-id="45c1f-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="45c1f-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="45c1f-121">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="45c1f-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="45c1f-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="45c1f-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c1f-123">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="45c1f-123">-IpAddress</span></span>
<span data-ttu-id="45c1f-124">Tümleştirme çalışma zamanı düğümünün IP adresi.</span><span class="sxs-lookup"><span data-stu-id="45c1f-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="45c1f-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="45c1f-125">-Name</span></span>
<span data-ttu-id="45c1f-126">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="45c1f-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="45c1f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c1f-127">-ResourceGroupName</span></span>
<span data-ttu-id="45c1f-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="45c1f-128">Resource group name.</span></span>

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

### <span data-ttu-id="45c1f-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="45c1f-129">-ResourceId</span></span>
<span data-ttu-id="45c1f-130">SYNAPSE tümleştirme çalışma zamanının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="45c1f-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="45c1f-131">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="45c1f-131">-WorkspaceName</span></span>
<span data-ttu-id="45c1f-132">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="45c1f-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="45c1f-133">-</span><span class="sxs-lookup"><span data-stu-id="45c1f-133">-WorkspaceObject</span></span>
<span data-ttu-id="45c1f-134">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="45c1f-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="45c1f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c1f-135">CommonParameters</span></span>
<span data-ttu-id="45c1f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45c1f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c1f-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45c1f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c1f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45c1f-138">INPUTS</span></span>

### <span data-ttu-id="45c1f-139">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="45c1f-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="45c1f-140">Microsoft. Azure. Commands. SYNAPSE. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="45c1f-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="45c1f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45c1f-141">OUTPUTS</span></span>

### <span data-ttu-id="45c1f-142">Microsoft. Azure. Commands. SYNAPSE. modeller. Psmanagedıntegrationruntimenode</span><span class="sxs-lookup"><span data-stu-id="45c1f-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="45c1f-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="45c1f-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="45c1f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45c1f-144">NOTES</span></span>

## <span data-ttu-id="45c1f-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45c1f-145">RELATED LINKS</span></span>
