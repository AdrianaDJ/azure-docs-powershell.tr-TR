---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265996"
---
# <span data-ttu-id="e6878-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="e6878-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="e6878-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6878-102">SYNOPSIS</span></span>
<span data-ttu-id="e6878-103">Bağlantı İzleyicisi uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6878-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="e6878-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6878-104">SYNTAX</span></span>

### <span data-ttu-id="e6878-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e6878-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6878-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="e6878-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6878-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6878-107">DESCRIPTION</span></span>
<span data-ttu-id="e6878-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet Bağlantı İzleyicisi uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6878-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="e6878-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6878-109">EXAMPLES</span></span>

### <span data-ttu-id="e6878-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e6878-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="e6878-111">Ad: Çalışmanoktası RESOURCEID:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: filtre: {"tür": "Içer", "öğeler": [{"tür": "Me Taddress", "adres": "WıN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="e6878-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="e6878-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6878-112">PARAMETERS</span></span>

### <span data-ttu-id="e6878-113">-Adres</span><span class="sxs-lookup"><span data-stu-id="e6878-113">-Address</span></span>
<span data-ttu-id="e6878-114">Bağlantı İzleyicisi uç noktasının adresi (IP veya etki alanı adı).</span><span class="sxs-lookup"><span data-stu-id="e6878-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6878-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6878-115">-DefaultProfile</span></span>
<span data-ttu-id="e6878-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6878-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6878-117">-Filterıtem</span><span class="sxs-lookup"><span data-stu-id="e6878-117">-FilterItem</span></span>
<span data-ttu-id="e6878-118">Filtredeki öğelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="e6878-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6878-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="e6878-119">-FilterType</span></span>
<span data-ttu-id="e6878-120">Uç nokta filtresinin davranışı.</span><span class="sxs-lookup"><span data-stu-id="e6878-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="e6878-121">Şu anda yalnızca ' Include ' destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="e6878-121">Currently only 'Include' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6878-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6878-122">-Name</span></span>
<span data-ttu-id="e6878-123">Bağlantı İzleyicisi uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="e6878-123">The name of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6878-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e6878-124">-ResourceId</span></span>
<span data-ttu-id="e6878-125">Bağlantı İzleyicisi uç noktasının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e6878-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6878-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6878-126">-Confirm</span></span>
<span data-ttu-id="e6878-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6878-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6878-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6878-128">-WhatIf</span></span>
<span data-ttu-id="e6878-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6878-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6878-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6878-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6878-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6878-131">CommonParameters</span></span>
<span data-ttu-id="e6878-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6878-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6878-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e6878-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6878-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6878-134">INPUTS</span></span>

### <span data-ttu-id="e6878-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e6878-135">None</span></span>

## <span data-ttu-id="e6878-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6878-136">OUTPUTS</span></span>

### <span data-ttu-id="e6878-137">Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="e6878-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="e6878-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6878-138">NOTES</span></span>

## <span data-ttu-id="e6878-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6878-139">RELATED LINKS</span></span>
