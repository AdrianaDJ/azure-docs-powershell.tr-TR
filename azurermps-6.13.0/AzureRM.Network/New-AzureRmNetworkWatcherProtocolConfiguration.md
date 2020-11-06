---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 4929612cd2bb3788bd171f4bb6386c622c4fbbee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594860"
---
# <span data-ttu-id="36956-101">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="36956-101">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="36956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36956-102">SYNOPSIS</span></span>
<span data-ttu-id="36956-103">Yeni bir iletişim kuralı yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36956-103">Creates a new protocol configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36956-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36956-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36956-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="36956-105">DESCRIPTION</span></span>
<span data-ttu-id="36956-106">New-AzureRmNetworkWatcherProtocolConfiguration cmdlet 'i yeni bir iletişim kuralı yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="36956-106">The New-AzureRmNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="36956-107">Bu nesne, belirtilen ölçütleri kullanarak connecitivity denetleme oturumu sırasında protokol yapılandırması 'nı kısıtlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="36956-107">This object is used to restrict the protocol confiuration during a connecitivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="36956-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36956-108">EXAMPLES</span></span>

### <span data-ttu-id="36956-109">Örnek 1: protokol yapılandırmasına sahip bir VM 'den bir Web sitesine ağ Izleyicisi bağlantısını sınama</span><span class="sxs-lookup"><span data-stu-id="36956-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzureRmNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


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

<span data-ttu-id="36956-110">Bu örnekte, Azure 'daki bir VM 'den www.bing.com 'e bağlantıyı test ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="36956-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="36956-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36956-111">PARAMETERS</span></span>

### <span data-ttu-id="36956-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36956-112">-DefaultProfile</span></span>
<span data-ttu-id="36956-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36956-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36956-114">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="36956-114">-Header</span></span>
<span data-ttu-id="36956-115">HTTP üstbilgilerinin listesi</span><span class="sxs-lookup"><span data-stu-id="36956-115">list of HTTP headers</span></span>

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

### <span data-ttu-id="36956-116">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="36956-116">-Method</span></span>
<span data-ttu-id="36956-117">HTTP yöntemi</span><span class="sxs-lookup"><span data-stu-id="36956-117">HTTP method</span></span>

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

### <span data-ttu-id="36956-118">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="36956-118">-Protocol</span></span>
<span data-ttu-id="36956-119">Cotol türü</span><span class="sxs-lookup"><span data-stu-id="36956-119">Procotol type</span></span>

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

### <span data-ttu-id="36956-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="36956-120">-ValidStatusCode</span></span>
<span data-ttu-id="36956-121">geçerli durum kodları</span><span class="sxs-lookup"><span data-stu-id="36956-121">valid status codes</span></span>

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

### <span data-ttu-id="36956-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36956-122">CommonParameters</span></span>
<span data-ttu-id="36956-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36956-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36956-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36956-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36956-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36956-125">INPUTS</span></span>

### <span data-ttu-id="36956-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="36956-126">None</span></span>

## <span data-ttu-id="36956-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36956-127">OUTPUTS</span></span>

### <span data-ttu-id="36956-128">Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="36956-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="36956-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36956-129">NOTES</span></span>
<span data-ttu-id="36956-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, paket, yakalama, trafik, filtre</span><span class="sxs-lookup"><span data-stu-id="36956-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="36956-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36956-131">RELATED LINKS</span></span>

[<span data-ttu-id="36956-132">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="36956-132">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="36956-133">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="36956-133">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="36956-134">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="36956-134">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="36956-135">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="36956-135">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="36956-136">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="36956-136">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="36956-137">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="36956-137">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="36956-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="36956-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="36956-139">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="36956-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="36956-140">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="36956-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="36956-141">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="36956-141">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="36956-142">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="36956-142">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="36956-143">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="36956-143">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="36956-144">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="36956-144">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="36956-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="36956-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="36956-146">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="36956-146">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="36956-147">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="36956-147">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="36956-148">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="36956-148">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="36956-149">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="36956-149">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="36956-150">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="36956-150">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="36956-151">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="36956-151">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="36956-152">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="36956-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="36956-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="36956-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="36956-154">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="36956-154">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="36956-155">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="36956-155">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="36956-156">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="36956-156">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="36956-157">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="36956-157">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="36956-158">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="36956-158">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
