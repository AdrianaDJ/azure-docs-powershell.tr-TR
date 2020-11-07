---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: c1ea29572bb42bea0c7e64c3ec818fe2f2d0ed0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937693"
---
# <span data-ttu-id="4e8d0-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e8d0-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="4e8d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e8d0-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8d0-103">Ağ Izleyicisi özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="4e8d0-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="4e8d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4e8d0-104">SYNTAX</span></span>

### <span data-ttu-id="4e8d0-105">Listeniz</span><span class="sxs-lookup"><span data-stu-id="4e8d0-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e8d0-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4e8d0-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e8d0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4e8d0-107">DESCRIPTION</span></span>
<span data-ttu-id="4e8d0-108">Get-AzNetworkWatcher cmdlet bir veya birden çok Azure ağ Izleyicisi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="4e8d0-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="4e8d0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4e8d0-109">EXAMPLES</span></span>

### <span data-ttu-id="4e8d0-110">Örnek 1: ağ Izleyicisi alma</span><span class="sxs-lookup"><span data-stu-id="4e8d0-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="4e8d0-111">NetworkWatcherRG kaynak grubundaki ağ Izleyicisi NetworkWatcher_westcentralus 'Ni alır.</span><span class="sxs-lookup"><span data-stu-id="4e8d0-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="4e8d0-112">Örnek 2: filtreleme kullanarak ağ Watchers</span><span class="sxs-lookup"><span data-stu-id="4e8d0-112">Example 2: List Network Watchers using filtering</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher*

Name              : NetworkWatcher_westcentralus1
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus1
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded

Name              : NetworkWatcher_westcentralus2
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus2
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="4e8d0-113">"Ağizleyicisi" ile başlayan ağ Watchers</span><span class="sxs-lookup"><span data-stu-id="4e8d0-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="4e8d0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4e8d0-114">PARAMETERS</span></span>

### <span data-ttu-id="4e8d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8d0-115">-DefaultProfile</span></span>
<span data-ttu-id="4e8d0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4e8d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e8d0-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="4e8d0-117">-Location</span></span>
<span data-ttu-id="4e8d0-118">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="4e8d0-118">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e8d0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="4e8d0-119">-Name</span></span>
<span data-ttu-id="4e8d0-120">Ağ İzleyici adı.</span><span class="sxs-lookup"><span data-stu-id="4e8d0-120">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4e8d0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e8d0-121">-ResourceGroupName</span></span>
<span data-ttu-id="4e8d0-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4e8d0-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="4e8d0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8d0-123">CommonParameters</span></span>
<span data-ttu-id="4e8d0-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4e8d0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8d0-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4e8d0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8d0-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4e8d0-126">INPUTS</span></span>

### <span data-ttu-id="4e8d0-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4e8d0-127">None</span></span>

## <span data-ttu-id="4e8d0-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4e8d0-128">OUTPUTS</span></span>

### <span data-ttu-id="4e8d0-129">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4e8d0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="4e8d0-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4e8d0-130">NOTES</span></span>
<span data-ttu-id="4e8d0-131">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="4e8d0-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="4e8d0-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4e8d0-132">RELATED LINKS</span></span>

[<span data-ttu-id="4e8d0-133">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="4e8d0-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4e8d0-134">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4e8d0-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4e8d0-135">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4e8d0-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4e8d0-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4e8d0-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4e8d0-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4e8d0-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4e8d0-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4e8d0-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4e8d0-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4e8d0-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4e8d0-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e8d0-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e8d0-141">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4e8d0-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4e8d0-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e8d0-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e8d0-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e8d0-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e8d0-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4e8d0-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4e8d0-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e8d0-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4e8d0-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4e8d0-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4e8d0-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4e8d0-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4e8d0-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e8d0-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e8d0-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e8d0-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e8d0-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e8d0-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e8d0-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4e8d0-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4e8d0-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e8d0-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e8d0-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e8d0-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4e8d0-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4e8d0-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4e8d0-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4e8d0-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4e8d0-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4e8d0-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4e8d0-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4e8d0-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4e8d0-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4e8d0-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4e8d0-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e8d0-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
