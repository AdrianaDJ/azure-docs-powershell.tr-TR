---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: 3c69884e988b10f41da4d41d98318ee96c019112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594859"
---
# <span data-ttu-id="6d67a-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6d67a-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="6d67a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d67a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d67a-103">Yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d67a-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d67a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d67a-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d67a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d67a-105">DESCRIPTION</span></span>
<span data-ttu-id="6d67a-106">New-AzureRmPacketCaptureFilterConfig cmdlet 'i yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d67a-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="6d67a-107">Bu nesne, belirtilen ölçütleri kullanarak paket yakalama oturumu sırasında yakalanan paketlerin türünü sınırlandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6d67a-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="6d67a-108">New-AzureRmNetworkWatcherPacketCapture cmdlet, birleştirilebilir yakalama oturumlarını etkinleştirmek için birden çok filtre nesnesi kabul edebilir.</span><span class="sxs-lookup"><span data-stu-id="6d67a-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="6d67a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d67a-109">EXAMPLES</span></span>

### <span data-ttu-id="6d67a-110">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma</span><span class="sxs-lookup"><span data-stu-id="6d67a-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="6d67a-111">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="6d67a-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="6d67a-112">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6d67a-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="6d67a-113">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6d67a-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="6d67a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d67a-114">PARAMETERS</span></span>

### <span data-ttu-id="6d67a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d67a-115">-DefaultProfile</span></span>
<span data-ttu-id="6d67a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d67a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d67a-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="6d67a-117">-LocalIPAddress</span></span>
<span data-ttu-id="6d67a-118">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d67a-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="6d67a-119">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="6d67a-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="6d67a-120">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="6d67a-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="6d67a-121">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="6d67a-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d67a-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="6d67a-122">-LocalPort</span></span>
<span data-ttu-id="6d67a-123">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d67a-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="6d67a-124">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="6d67a-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="6d67a-125">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="6d67a-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="6d67a-126">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="6d67a-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d67a-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="6d67a-127">-Protocol</span></span>
<span data-ttu-id="6d67a-128">Filtre uygulanacak procotol belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d67a-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="6d67a-129">Kabul edilebilir değerler "TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="6d67a-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d67a-130">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="6d67a-130">-RemoteIPAddress</span></span>
<span data-ttu-id="6d67a-131">Filtre uygulanacak uzak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d67a-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="6d67a-132">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="6d67a-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="6d67a-133">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="6d67a-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="6d67a-134">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="6d67a-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d67a-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="6d67a-135">-RemotePort</span></span>
<span data-ttu-id="6d67a-136">Filtre uygulanacak uzak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d67a-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="6d67a-137">Uzak bağlantı noktası örnek girişleri: tek çıkışlı girdi için "80".</span><span class="sxs-lookup"><span data-stu-id="6d67a-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="6d67a-138">Aralık için "80-85".</span><span class="sxs-lookup"><span data-stu-id="6d67a-138">"80-85" for range.</span></span>
<span data-ttu-id="6d67a-139">birden çok girdi için "80; 443;".</span><span class="sxs-lookup"><span data-stu-id="6d67a-139">"80;443;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d67a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d67a-140">CommonParameters</span></span>
<span data-ttu-id="6d67a-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d67a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d67a-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d67a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d67a-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d67a-143">INPUTS</span></span>

### <span data-ttu-id="6d67a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="6d67a-144">System.String</span></span>
<span data-ttu-id="6d67a-145">Parametreler: Protocol (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d67a-145">Parameters: Protocol (ByValue)</span></span>

## <span data-ttu-id="6d67a-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d67a-146">OUTPUTS</span></span>

### <span data-ttu-id="6d67a-147">Microsoft. Azure. Commands. Network. model. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="6d67a-147">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="6d67a-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d67a-148">NOTES</span></span>
<span data-ttu-id="6d67a-149">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, paket, yakalama, trafik, filtre</span><span class="sxs-lookup"><span data-stu-id="6d67a-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="6d67a-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d67a-150">RELATED LINKS</span></span>

[<span data-ttu-id="6d67a-151">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6d67a-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6d67a-152">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6d67a-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6d67a-153">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6d67a-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6d67a-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6d67a-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6d67a-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6d67a-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6d67a-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6d67a-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6d67a-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6d67a-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6d67a-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d67a-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d67a-159">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6d67a-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6d67a-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d67a-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d67a-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d67a-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d67a-162">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d67a-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d67a-163">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d67a-163">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6d67a-164">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6d67a-164">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6d67a-165">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6d67a-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="6d67a-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d67a-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d67a-167">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d67a-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d67a-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d67a-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d67a-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6d67a-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6d67a-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d67a-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d67a-171">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d67a-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d67a-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6d67a-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6d67a-173">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6d67a-173">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6d67a-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6d67a-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6d67a-175">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6d67a-175">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6d67a-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6d67a-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="6d67a-177">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d67a-177">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
