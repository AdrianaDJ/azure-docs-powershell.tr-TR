---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: f8e51258a56051edf99aa1ec0cfa5e252e0ac0d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918220"
---
# <span data-ttu-id="467a5-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="467a5-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="467a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="467a5-102">SYNOPSIS</span></span>
<span data-ttu-id="467a5-103">Yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="467a5-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="467a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="467a5-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="467a5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="467a5-105">DESCRIPTION</span></span>
<span data-ttu-id="467a5-106">New-AzPacketCaptureFilterConfig cmdlet 'i yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="467a5-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="467a5-107">Bu nesne, belirtilen ölçütleri kullanarak paket yakalama oturumu sırasında yakalanan paketlerin türünü sınırlandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="467a5-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="467a5-108">New-AzNetworkWatcherPacketCapture cmdlet, birleştirilebilir yakalama oturumlarını etkinleştirmek için birden çok filtre nesnesi kabul edebilir.</span><span class="sxs-lookup"><span data-stu-id="467a5-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="467a5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="467a5-109">EXAMPLES</span></span>

### <span data-ttu-id="467a5-110">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma</span><span class="sxs-lookup"><span data-stu-id="467a5-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="467a5-111">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="467a5-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="467a5-112">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="467a5-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="467a5-113">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="467a5-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="467a5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="467a5-114">PARAMETERS</span></span>

### <span data-ttu-id="467a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467a5-115">-DefaultProfile</span></span>
<span data-ttu-id="467a5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="467a5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="467a5-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="467a5-117">-LocalIPAddress</span></span>
<span data-ttu-id="467a5-118">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="467a5-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="467a5-119">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="467a5-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="467a5-120">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="467a5-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="467a5-121">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="467a5-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="467a5-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="467a5-122">-LocalPort</span></span>
<span data-ttu-id="467a5-123">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="467a5-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="467a5-124">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="467a5-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="467a5-125">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="467a5-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="467a5-126">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="467a5-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="467a5-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="467a5-127">-Protocol</span></span>
<span data-ttu-id="467a5-128">Süzülecek protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="467a5-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="467a5-129">Kabul edilebilir değerler "TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="467a5-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="467a5-130">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="467a5-130">-RemoteIPAddress</span></span>
<span data-ttu-id="467a5-131">Filtre uygulanacak uzak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="467a5-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="467a5-132">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="467a5-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="467a5-133">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="467a5-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="467a5-134">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="467a5-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="467a5-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="467a5-135">-RemotePort</span></span>
<span data-ttu-id="467a5-136">Filtre uygulanacak uzak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="467a5-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="467a5-137">Uzak bağlantı noktası örnek girişleri: tek çıkışlı girdi için "80".</span><span class="sxs-lookup"><span data-stu-id="467a5-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="467a5-138">Aralık için "80-85".</span><span class="sxs-lookup"><span data-stu-id="467a5-138">"80-85" for range.</span></span>
<span data-ttu-id="467a5-139">birden çok girdi için "80; 443;".</span><span class="sxs-lookup"><span data-stu-id="467a5-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="467a5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467a5-140">CommonParameters</span></span>
<span data-ttu-id="467a5-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="467a5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467a5-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="467a5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467a5-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="467a5-143">INPUTS</span></span>

### <span data-ttu-id="467a5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="467a5-144">System.String</span></span>

## <span data-ttu-id="467a5-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="467a5-145">OUTPUTS</span></span>

### <span data-ttu-id="467a5-146">Microsoft. Azure. Commands. Network. model. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="467a5-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="467a5-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="467a5-147">NOTES</span></span>
<span data-ttu-id="467a5-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, paket, yakalama, trafik, filtre</span><span class="sxs-lookup"><span data-stu-id="467a5-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="467a5-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="467a5-149">RELATED LINKS</span></span>

[<span data-ttu-id="467a5-150">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="467a5-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="467a5-151">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="467a5-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="467a5-152">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="467a5-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="467a5-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="467a5-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="467a5-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="467a5-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="467a5-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="467a5-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="467a5-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="467a5-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="467a5-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="467a5-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="467a5-158">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="467a5-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="467a5-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="467a5-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="467a5-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="467a5-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="467a5-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="467a5-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="467a5-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="467a5-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="467a5-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="467a5-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="467a5-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="467a5-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="467a5-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="467a5-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="467a5-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="467a5-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="467a5-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="467a5-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="467a5-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="467a5-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="467a5-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="467a5-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="467a5-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="467a5-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="467a5-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="467a5-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="467a5-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="467a5-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="467a5-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="467a5-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="467a5-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="467a5-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="467a5-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="467a5-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="467a5-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="467a5-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)