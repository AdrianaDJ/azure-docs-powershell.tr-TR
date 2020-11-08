---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: e20c0087c44ee7dbf29d65733712eb28022da1b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098135"
---
# <span data-ttu-id="06d0d-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="06d0d-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="06d0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d0d-102">SYNOPSIS</span></span>
<span data-ttu-id="06d0d-103">Paketin belirli bir hedefte veya belirli bir hedefle kabul edilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="06d0d-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="06d0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06d0d-104">SYNTAX</span></span>

### <span data-ttu-id="06d0d-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06d0d-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d0d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="06d0d-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06d0d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="06d0d-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06d0d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="06d0d-108">DESCRIPTION</span></span>
<span data-ttu-id="06d0d-109">Belirli bir VM kaynağı ve yerel ve uzak, IP adresleri ve bağlantı noktaları kullanılarak belirtilen yöne sahip bir paket için Test-AzNetworkWatcherIPFlow cmdlet, pakete izin verilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="06d0d-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="06d0d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06d0d-110">EXAMPLES</span></span>

### <span data-ttu-id="06d0d-111">Örnek 1: Test-AzNetworkWatcherIPFlow çalışma</span><span class="sxs-lookup"><span data-stu-id="06d0d-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="06d0d-112">Bu abonelik için Batı merkezi 'ndeki ağ Izleyicisi 'ni alır, ardından VM 'yi ve ilişkili ağ arabirimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="06d0d-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="06d0d-113">Ardından ilk ağ arabiriminde, internet 'teki bir IP 'ye giden bağlantı için ilk ağ arabiriminden ilk IP 'yi kullanarak Test-AzNetworkWatcherIPFlow çalışır.</span><span class="sxs-lookup"><span data-stu-id="06d0d-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="06d0d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06d0d-114">PARAMETERS</span></span>

### <span data-ttu-id="06d0d-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="06d0d-115">-AsJob</span></span>
<span data-ttu-id="06d0d-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="06d0d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06d0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d0d-117">-DefaultProfile</span></span>
<span data-ttu-id="06d0d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06d0d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06d0d-119">-Yön</span><span class="sxs-lookup"><span data-stu-id="06d0d-119">-Direction</span></span>
<span data-ttu-id="06d0d-120">Yönüyle.</span><span class="sxs-lookup"><span data-stu-id="06d0d-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d0d-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="06d0d-121">-LocalIPAddress</span></span>
<span data-ttu-id="06d0d-122">Yerel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="06d0d-122">Local IP Address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d0d-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="06d0d-123">-LocalPort</span></span>
<span data-ttu-id="06d0d-124">Yerel bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="06d0d-124">Local Port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d0d-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="06d0d-125">-Location</span></span>
<span data-ttu-id="06d0d-126">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="06d0d-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="06d0d-127">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="06d0d-127">-NetworkWatcher</span></span>
<span data-ttu-id="06d0d-128">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="06d0d-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="06d0d-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="06d0d-129">-NetworkWatcherName</span></span>
<span data-ttu-id="06d0d-130">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="06d0d-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="06d0d-131">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="06d0d-131">-Protocol</span></span>
<span data-ttu-id="06d0d-132">Kurallarının.</span><span class="sxs-lookup"><span data-stu-id="06d0d-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06d0d-133">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="06d0d-133">-RemoteIPAddress</span></span>
<span data-ttu-id="06d0d-134">Uzak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="06d0d-134">Remote IP Address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d0d-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="06d0d-135">-RemotePort</span></span>
<span data-ttu-id="06d0d-136">Uzak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="06d0d-136">Remote port.</span></span>

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

### <span data-ttu-id="06d0d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d0d-137">-ResourceGroupName</span></span>
<span data-ttu-id="06d0d-138">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="06d0d-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="06d0d-139">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="06d0d-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="06d0d-140">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="06d0d-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="06d0d-141">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="06d0d-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="06d0d-142">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="06d0d-142">The target virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06d0d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d0d-143">CommonParameters</span></span>
<span data-ttu-id="06d0d-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06d0d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d0d-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06d0d-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d0d-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06d0d-146">INPUTS</span></span>

### <span data-ttu-id="06d0d-147">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="06d0d-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="06d0d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="06d0d-148">System.String</span></span>

## <span data-ttu-id="06d0d-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06d0d-149">OUTPUTS</span></span>

### <span data-ttu-id="06d0d-150">Microsoft. Azure. Commands. Network. model. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="06d0d-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="06d0d-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06d0d-151">NOTES</span></span>
<span data-ttu-id="06d0d-152">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="06d0d-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="06d0d-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06d0d-153">RELATED LINKS</span></span>

[<span data-ttu-id="06d0d-154">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="06d0d-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="06d0d-155">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="06d0d-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="06d0d-156">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="06d0d-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="06d0d-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="06d0d-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="06d0d-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="06d0d-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="06d0d-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="06d0d-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="06d0d-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="06d0d-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="06d0d-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06d0d-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06d0d-162">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="06d0d-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="06d0d-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06d0d-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06d0d-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06d0d-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06d0d-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06d0d-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06d0d-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="06d0d-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="06d0d-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="06d0d-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="06d0d-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="06d0d-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="06d0d-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="06d0d-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="06d0d-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="06d0d-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="06d0d-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="06d0d-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="06d0d-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="06d0d-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="06d0d-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="06d0d-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="06d0d-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="06d0d-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="06d0d-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="06d0d-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="06d0d-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="06d0d-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="06d0d-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="06d0d-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="06d0d-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="06d0d-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="06d0d-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="06d0d-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="06d0d-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="06d0d-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
