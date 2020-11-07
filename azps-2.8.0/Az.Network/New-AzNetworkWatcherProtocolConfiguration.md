---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 7db73595c4a7f6f4f843df4d77096549ace82a4d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932352"
---
# <span data-ttu-id="12e4a-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="12e4a-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="12e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="12e4a-103">Yeni bir iletişim kuralı yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12e4a-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="12e4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12e4a-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12e4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="12e4a-106">New-AzNetworkWatcherProtocolConfiguration cmdlet 'i yeni bir iletişim kuralı yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12e4a-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="12e4a-107">Bu nesne, bir bağlantı denetleme oturumu sırasında belirtilen ölçütleri kullanarak protokol yapılandırmasını kısıtlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12e4a-107">This object is used to restrict the protocol configuration during a connectivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="12e4a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12e4a-108">EXAMPLES</span></span>

### <span data-ttu-id="12e4a-109">Örnek 1: protokol yapılandırmasına sahip bir VM 'den bir Web sitesine ağ Izleyicisi bağlantısını sınama</span><span class="sxs-lookup"><span data-stu-id="12e4a-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="12e4a-110">Bu örnekte, Azure 'daki bir VM 'den www.bing.com 'e bağlantıyı test ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="12e4a-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="12e4a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12e4a-111">PARAMETERS</span></span>

### <span data-ttu-id="12e4a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e4a-112">-DefaultProfile</span></span>
<span data-ttu-id="12e4a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12e4a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e4a-114">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="12e4a-114">-Header</span></span>
<span data-ttu-id="12e4a-115">HTTP üstbilgilerinin listesi</span><span class="sxs-lookup"><span data-stu-id="12e4a-115">list of HTTP headers</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e4a-116">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="12e4a-116">-Method</span></span>
<span data-ttu-id="12e4a-117">HTTP yöntemi</span><span class="sxs-lookup"><span data-stu-id="12e4a-117">HTTP method</span></span>

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

### <span data-ttu-id="12e4a-118">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="12e4a-118">-Protocol</span></span>
<span data-ttu-id="12e4a-119">Protokol türü</span><span class="sxs-lookup"><span data-stu-id="12e4a-119">Protocol type</span></span>

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

### <span data-ttu-id="12e4a-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="12e4a-120">-ValidStatusCode</span></span>
<span data-ttu-id="12e4a-121">geçerli durum kodları</span><span class="sxs-lookup"><span data-stu-id="12e4a-121">valid status codes</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12e4a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e4a-122">CommonParameters</span></span>
<span data-ttu-id="12e4a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12e4a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e4a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12e4a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e4a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12e4a-125">INPUTS</span></span>

### <span data-ttu-id="12e4a-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="12e4a-126">None</span></span>

## <span data-ttu-id="12e4a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12e4a-127">OUTPUTS</span></span>

### <span data-ttu-id="12e4a-128">Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="12e4a-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="12e4a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12e4a-129">NOTES</span></span>
<span data-ttu-id="12e4a-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, paket, yakalama, trafik, filtre</span><span class="sxs-lookup"><span data-stu-id="12e4a-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="12e4a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12e4a-131">RELATED LINKS</span></span>

[<span data-ttu-id="12e4a-132">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="12e4a-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="12e4a-133">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="12e4a-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="12e4a-134">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="12e4a-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="12e4a-135">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="12e4a-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="12e4a-136">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="12e4a-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="12e4a-137">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="12e4a-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="12e4a-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="12e4a-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="12e4a-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="12e4a-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="12e4a-140">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="12e4a-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="12e4a-141">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="12e4a-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="12e4a-142">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="12e4a-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="12e4a-143">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="12e4a-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="12e4a-144">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="12e4a-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="12e4a-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="12e4a-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="12e4a-146">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="12e4a-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="12e4a-147">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="12e4a-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="12e4a-148">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="12e4a-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="12e4a-149">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="12e4a-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="12e4a-150">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="12e4a-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="12e4a-151">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="12e4a-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="12e4a-152">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="12e4a-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="12e4a-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="12e4a-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="12e4a-154">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="12e4a-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="12e4a-155">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="12e4a-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="12e4a-156">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="12e4a-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="12e4a-157">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="12e4a-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="12e4a-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="12e4a-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
