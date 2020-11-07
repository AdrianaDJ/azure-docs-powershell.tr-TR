---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 61946fcf8023fa46e6296bb976fd474f5021a195
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932695"
---
# <span data-ttu-id="3ab64-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3ab64-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="3ab64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ab64-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab64-103">Paketin belirli bir hedefte veya belirli bir hedefle kabul edilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3ab64-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="3ab64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ab64-104">SYNTAX</span></span>

### <span data-ttu-id="3ab64-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ab64-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ab64-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3ab64-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ab64-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3ab64-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ab64-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ab64-108">DESCRIPTION</span></span>
<span data-ttu-id="3ab64-109">Belirli bir VM kaynağı ve yerel ve uzak, IP adresleri ve bağlantı noktaları kullanılarak belirtilen yöne sahip bir paket için Test-AzNetworkWatcherIPFlow cmdlet, pakete izin verilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3ab64-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="3ab64-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ab64-110">EXAMPLES</span></span>

### <span data-ttu-id="3ab64-111">Örnek 1: Test-AzNetworkWatcherIPFlow çalışma</span><span class="sxs-lookup"><span data-stu-id="3ab64-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="3ab64-112">Bu abonelik için Batı merkezi 'ndeki ağ Izleyicisi 'ni alır, ardından VM 'yi ve ilişkili ağ arabirimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ab64-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="3ab64-113">Ardından ilk ağ arabiriminde, internet 'teki bir IP 'ye giden bağlantı için ilk ağ arabiriminden ilk IP 'yi kullanarak Test-AzNetworkWatcherIPFlow çalışır.</span><span class="sxs-lookup"><span data-stu-id="3ab64-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="3ab64-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ab64-114">PARAMETERS</span></span>

### <span data-ttu-id="3ab64-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="3ab64-115">-AsJob</span></span>
<span data-ttu-id="3ab64-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3ab64-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ab64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab64-117">-DefaultProfile</span></span>
<span data-ttu-id="3ab64-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ab64-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ab64-119">-Yön</span><span class="sxs-lookup"><span data-stu-id="3ab64-119">-Direction</span></span>
<span data-ttu-id="3ab64-120">Yönüyle.</span><span class="sxs-lookup"><span data-stu-id="3ab64-120">Direction.</span></span>

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

### <span data-ttu-id="3ab64-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="3ab64-121">-LocalIPAddress</span></span>
<span data-ttu-id="3ab64-122">Yerel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="3ab64-122">Local IP Address.</span></span>

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

### <span data-ttu-id="3ab64-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="3ab64-123">-LocalPort</span></span>
<span data-ttu-id="3ab64-124">Yerel bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="3ab64-124">Local Port.</span></span>

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

### <span data-ttu-id="3ab64-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="3ab64-125">-Location</span></span>
<span data-ttu-id="3ab64-126">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="3ab64-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3ab64-127">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3ab64-127">-NetworkWatcher</span></span>
<span data-ttu-id="3ab64-128">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="3ab64-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="3ab64-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3ab64-129">-NetworkWatcherName</span></span>
<span data-ttu-id="3ab64-130">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="3ab64-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="3ab64-131">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="3ab64-131">-Protocol</span></span>
<span data-ttu-id="3ab64-132">Kurallarının.</span><span class="sxs-lookup"><span data-stu-id="3ab64-132">Protocol.</span></span>

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

### <span data-ttu-id="3ab64-133">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="3ab64-133">-RemoteIPAddress</span></span>
<span data-ttu-id="3ab64-134">Uzak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="3ab64-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="3ab64-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="3ab64-135">-RemotePort</span></span>
<span data-ttu-id="3ab64-136">Uzak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="3ab64-136">Remote port.</span></span>

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

### <span data-ttu-id="3ab64-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab64-137">-ResourceGroupName</span></span>
<span data-ttu-id="3ab64-138">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3ab64-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3ab64-139">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="3ab64-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="3ab64-140">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="3ab64-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="3ab64-141">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="3ab64-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="3ab64-142">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3ab64-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="3ab64-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab64-143">CommonParameters</span></span>
<span data-ttu-id="3ab64-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ab64-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab64-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ab64-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab64-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ab64-146">INPUTS</span></span>

### <span data-ttu-id="3ab64-147">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3ab64-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3ab64-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3ab64-148">System.String</span></span>

## <span data-ttu-id="3ab64-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ab64-149">OUTPUTS</span></span>

### <span data-ttu-id="3ab64-150">Microsoft. Azure. Commands. Network. model. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="3ab64-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="3ab64-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ab64-151">NOTES</span></span>
<span data-ttu-id="3ab64-152">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="3ab64-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="3ab64-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ab64-153">RELATED LINKS</span></span>

[<span data-ttu-id="3ab64-154">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="3ab64-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3ab64-155">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3ab64-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3ab64-156">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3ab64-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3ab64-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3ab64-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3ab64-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3ab64-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3ab64-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3ab64-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3ab64-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3ab64-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3ab64-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ab64-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ab64-162">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3ab64-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3ab64-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ab64-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ab64-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ab64-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ab64-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3ab64-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3ab64-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ab64-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3ab64-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3ab64-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3ab64-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3ab64-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3ab64-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ab64-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3ab64-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ab64-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3ab64-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ab64-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3ab64-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3ab64-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3ab64-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ab64-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3ab64-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ab64-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3ab64-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3ab64-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3ab64-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3ab64-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3ab64-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3ab64-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3ab64-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3ab64-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3ab64-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3ab64-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="3ab64-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3ab64-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
