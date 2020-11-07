---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 35222774bf5b18cfb18ecfc5479f0d6e11636b99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937677"
---
# <span data-ttu-id="c3df8-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3df8-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="c3df8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3df8-102">SYNOPSIS</span></span>
<span data-ttu-id="c3df8-103">Bir paket yakalama kaynağının bilgilerini ve özelliklerini ve durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c3df8-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="c3df8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3df8-104">SYNTAX</span></span>

### <span data-ttu-id="c3df8-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3df8-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3df8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c3df8-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3df8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c3df8-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3df8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3df8-108">DESCRIPTION</span></span>
<span data-ttu-id="c3df8-109">Get-AzNetworkWatcherPacketCapture, paket yakalama kaynağının özelliklerini ve durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c3df8-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="c3df8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3df8-110">EXAMPLES</span></span>

### <span data-ttu-id="c3df8-111">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma ve durumunu alma</span><span class="sxs-lookup"><span data-stu-id="c3df8-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="c3df8-112">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="c3df8-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="c3df8-113">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="c3df8-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="c3df8-114">Ardından, yakalama oturumunun durumunu almak için Get-AzNetworkWatcherPacketCapture çağrı yaptık.</span><span class="sxs-lookup"><span data-stu-id="c3df8-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="c3df8-115">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c3df8-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="c3df8-116">Doğrudan New-AzNetworkWatcherPacketCapture komutundan paket yakalamaya başvuru oluşturursanız, tüm özellikler olmaz.</span><span class="sxs-lookup"><span data-stu-id="c3df8-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="c3df8-117">Get-AzNetworkWatcherPacketCapture komutuna çağrı yaparak paket yakalamanın tüm özelliklerini alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c3df8-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="c3df8-118">Örnek 2: birden çok filtre içeren bir paket yakalama oluşturma ve durumunu alma</span><span class="sxs-lookup"><span data-stu-id="c3df8-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="c3df8-119">Bu cmdlet, NW1 ağ Izleyicisi 'nde "PacketCapture" ile başlayan tüm Packetcapture öğesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c3df8-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="c3df8-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3df8-120">PARAMETERS</span></span>

### <span data-ttu-id="c3df8-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="c3df8-121">-AsJob</span></span>
<span data-ttu-id="c3df8-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c3df8-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3df8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3df8-123">-DefaultProfile</span></span>
<span data-ttu-id="c3df8-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3df8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3df8-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="c3df8-125">-Location</span></span>
<span data-ttu-id="c3df8-126">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="c3df8-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c3df8-127">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c3df8-127">-NetworkWatcher</span></span>
<span data-ttu-id="c3df8-128">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="c3df8-128">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3df8-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c3df8-129">-NetworkWatcherName</span></span>
<span data-ttu-id="c3df8-130">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="c3df8-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3df8-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="c3df8-131">-PacketCaptureName</span></span>
<span data-ttu-id="c3df8-132">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="c3df8-132">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c3df8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3df8-133">-ResourceGroupName</span></span>
<span data-ttu-id="c3df8-134">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c3df8-134">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3df8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3df8-135">CommonParameters</span></span>
<span data-ttu-id="c3df8-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3df8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3df8-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c3df8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3df8-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3df8-138">INPUTS</span></span>

### <span data-ttu-id="c3df8-139">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c3df8-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c3df8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c3df8-140">System.String</span></span>

## <span data-ttu-id="c3df8-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3df8-141">OUTPUTS</span></span>

### <span data-ttu-id="c3df8-142">Microsoft. Azure. Commands. Network. modeller. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="c3df8-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="c3df8-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3df8-143">NOTES</span></span>
<span data-ttu-id="c3df8-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="c3df8-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="c3df8-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3df8-145">RELATED LINKS</span></span>

[<span data-ttu-id="c3df8-146">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="c3df8-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c3df8-147">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c3df8-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c3df8-148">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c3df8-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c3df8-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c3df8-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c3df8-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c3df8-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c3df8-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c3df8-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c3df8-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c3df8-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c3df8-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3df8-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c3df8-154">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c3df8-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c3df8-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3df8-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c3df8-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3df8-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c3df8-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c3df8-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c3df8-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3df8-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c3df8-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c3df8-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c3df8-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c3df8-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c3df8-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3df8-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3df8-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3df8-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3df8-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3df8-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3df8-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c3df8-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c3df8-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3df8-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3df8-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3df8-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c3df8-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c3df8-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c3df8-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c3df8-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c3df8-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c3df8-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c3df8-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c3df8-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c3df8-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c3df8-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c3df8-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c3df8-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

