---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323284"
---
# <span data-ttu-id="dcd3a-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="dcd3a-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="dcd3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd3a-103">Bağlantı İzleyicisi uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="dcd3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcd3a-104">SYNTAX</span></span>

### <span data-ttu-id="dcd3a-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="dcd3a-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd3a-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="dcd3a-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd3a-107">Azuyeniden ağ</span><span class="sxs-lookup"><span data-stu-id="dcd3a-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd3a-108">Dış adres</span><span class="sxs-lookup"><span data-stu-id="dcd3a-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd3a-109">Mmate makinesi</span><span class="sxs-lookup"><span data-stu-id="dcd3a-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcd3a-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="dcd3a-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcd3a-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcd3a-111">DESCRIPTION</span></span>
<span data-ttu-id="dcd3a-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet Bağlantı İzleyicisi uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="dcd3a-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcd3a-113">EXAMPLES</span></span>

### <span data-ttu-id="dcd3a-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dcd3a-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="dcd3a-115">Ad: Çalışmanoktası türü: Mmaın, MACHINE RESOURCEID:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: scope: {"Include": [{"Address": "WıN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="dcd3a-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="dcd3a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcd3a-116">PARAMETERS</span></span>

### <span data-ttu-id="dcd3a-117">-Adres</span><span class="sxs-lookup"><span data-stu-id="dcd3a-117">-Address</span></span>
<span data-ttu-id="dcd3a-118">Bağlantı İzleyicisi uç noktasının adresi (IP veya etki alanı adı).</span><span class="sxs-lookup"><span data-stu-id="dcd3a-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-119">-Azuyeniden gönderme</span><span class="sxs-lookup"><span data-stu-id="dcd3a-119">-AzureSubnet</span></span>
<span data-ttu-id="dcd3a-120">Azure alt ağı uç noktası anahtarı.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="dcd3a-121">-AzureVM</span></span>
<span data-ttu-id="dcd3a-122">Azure VM uç noktası anahtarı.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="dcd3a-123">-AzureVNet</span></span>
<span data-ttu-id="dcd3a-124">Azure VNET uç noktası anahtarı.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-125">-Kapak Agelevel</span><span class="sxs-lookup"><span data-stu-id="dcd3a-125">-CoverageLevel</span></span>
<span data-ttu-id="dcd3a-126">Uç nokta için test kapsamı.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="dcd3a-127">Desteklenen değerler varsayılan, düşük, BelowAverage, Average, AboveAvergae, Full değerleridir.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd3a-128">-DefaultProfile</span></span>
<span data-ttu-id="dcd3a-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcd3a-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="dcd3a-130">-ExcludeItem</span></span>
<span data-ttu-id="dcd3a-131">Uç nokta kapsamından dışlanmak zorunda olan öğelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="dcd3a-132">-ExternalAddress</span></span>
<span data-ttu-id="dcd3a-133">Dış adres uç noktası anahtarı.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-134">-Includeıtem</span><span class="sxs-lookup"><span data-stu-id="dcd3a-134">-IncludeItem</span></span>
<span data-ttu-id="dcd3a-135">Endpont kapsamına eklenmesi gereken öğelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-136">-MMA</span><span class="sxs-lookup"><span data-stu-id="dcd3a-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="dcd3a-137">MMA çalışma alanı makine uç noktası anahtarı.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="dcd3a-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="dcd3a-139">MMA çalışma alanı ağı uç noktası anahtarı.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcd3a-140">-Name</span></span>
<span data-ttu-id="dcd3a-141">Bağlantı İzleyicisi uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="dcd3a-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dcd3a-142">-ResourceId</span></span>
<span data-ttu-id="dcd3a-143">Bağlantı İzleyicisi uç noktasının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd3a-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="dcd3a-144">-Confirm</span></span>
<span data-ttu-id="dcd3a-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcd3a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcd3a-146">-WhatIf</span></span>
<span data-ttu-id="dcd3a-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcd3a-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcd3a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd3a-149">CommonParameters</span></span>
<span data-ttu-id="dcd3a-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd3a-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dcd3a-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd3a-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcd3a-152">INPUTS</span></span>

### <span data-ttu-id="dcd3a-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dcd3a-153">None</span></span>

## <span data-ttu-id="dcd3a-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcd3a-154">OUTPUTS</span></span>

### <span data-ttu-id="dcd3a-155">Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="dcd3a-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="dcd3a-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcd3a-156">NOTES</span></span>

## <span data-ttu-id="dcd3a-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcd3a-157">RELATED LINKS</span></span>
