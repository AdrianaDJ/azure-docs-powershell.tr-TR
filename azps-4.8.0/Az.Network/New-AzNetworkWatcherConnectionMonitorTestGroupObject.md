---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109472"
---
# <span data-ttu-id="f11ec-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="f11ec-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="f11ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f11ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f11ec-103">Bir bağlantı izleme testi grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f11ec-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="f11ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f11ec-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f11ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f11ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f11ec-106">New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet 'i bir bağlantı İzleyicisi test grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f11ec-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="f11ec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f11ec-107">EXAMPLES</span></span>

### <span data-ttu-id="f11ec-108">Örnek 1:2 testConfigurations, w Source ve 2 varış uç noktası içeren bir test grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="f11ec-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="f11ec-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f11ec-109">PARAMETERS</span></span>

### <span data-ttu-id="f11ec-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11ec-110">-DefaultProfile</span></span>
<span data-ttu-id="f11ec-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f11ec-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f11ec-112">-Hedef</span><span class="sxs-lookup"><span data-stu-id="f11ec-112">-Destination</span></span>
<span data-ttu-id="f11ec-113">Hedef uç noktaları listesi.</span><span class="sxs-lookup"><span data-stu-id="f11ec-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11ec-114">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="f11ec-114">-Disable</span></span>
<span data-ttu-id="f11ec-115">Test grubunun devre dışı bırakılıp bırakılmadığını belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="f11ec-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="f11ec-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f11ec-116">-Name</span></span>
<span data-ttu-id="f11ec-117">Test grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f11ec-117">The test group name.</span></span>

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

### <span data-ttu-id="f11ec-118">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="f11ec-118">-Source</span></span>
<span data-ttu-id="f11ec-119">Kaynak uç noktaları listesi.</span><span class="sxs-lookup"><span data-stu-id="f11ec-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11ec-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="f11ec-120">-TestConfiguration</span></span>
<span data-ttu-id="f11ec-121">Test yapılandırması listesi.</span><span class="sxs-lookup"><span data-stu-id="f11ec-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11ec-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="f11ec-122">-Confirm</span></span>
<span data-ttu-id="f11ec-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f11ec-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f11ec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f11ec-124">-WhatIf</span></span>
<span data-ttu-id="f11ec-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f11ec-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f11ec-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f11ec-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f11ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11ec-127">CommonParameters</span></span>
<span data-ttu-id="f11ec-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f11ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11ec-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f11ec-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11ec-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f11ec-130">INPUTS</span></span>

### <span data-ttu-id="f11ec-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f11ec-131">None</span></span>

## <span data-ttu-id="f11ec-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f11ec-132">OUTPUTS</span></span>

### <span data-ttu-id="f11ec-133">Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="f11ec-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="f11ec-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f11ec-134">NOTES</span></span>

## <span data-ttu-id="f11ec-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f11ec-135">RELATED LINKS</span></span>
