---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 7fe316bda1cc6385babad2b5a7cb03d44a6fc128
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937688"
---
# <span data-ttu-id="b44aa-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b44aa-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="b44aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b44aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b44aa-103">Bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="b44aa-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="b44aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b44aa-104">SYNTAX</span></span>

### <span data-ttu-id="b44aa-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b44aa-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b44aa-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b44aa-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b44aa-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b44aa-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b44aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b44aa-108">DESCRIPTION</span></span>
<span data-ttu-id="b44aa-109">Get-AzNetworkWatcherNextHop cmdlet, bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="b44aa-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="b44aa-110">Sonraki atlama, Azure kaynağının türünü, bu kaynağın ilişkili IP adresini ve rotadaki sorumlu yönlendirme tablosu kuralını görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b44aa-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="b44aa-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b44aa-111">EXAMPLES</span></span>

### <span data-ttu-id="b44aa-112">Örnek 1: Internet IP 'si ile iletişim kurarken sonraki atlama</span><span class="sxs-lookup"><span data-stu-id="b44aa-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="b44aa-113">Belirtilen sanal makinedeki birincil ağ arabiriminden giden iletişimin sonraki 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="b44aa-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="b44aa-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b44aa-114">PARAMETERS</span></span>

### <span data-ttu-id="b44aa-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="b44aa-115">-AsJob</span></span>
<span data-ttu-id="b44aa-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b44aa-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b44aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44aa-117">-DefaultProfile</span></span>
<span data-ttu-id="b44aa-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b44aa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b44aa-119">-Destinationıpaddress</span><span class="sxs-lookup"><span data-stu-id="b44aa-119">-DestinationIPAddress</span></span>
<span data-ttu-id="b44aa-120">Hedef IP adresi.</span><span class="sxs-lookup"><span data-stu-id="b44aa-120">Destination IP address.</span></span>

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

### <span data-ttu-id="b44aa-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="b44aa-121">-Location</span></span>
<span data-ttu-id="b44aa-122">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="b44aa-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b44aa-123">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b44aa-123">-NetworkWatcher</span></span>
<span data-ttu-id="b44aa-124">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="b44aa-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="b44aa-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b44aa-125">-NetworkWatcherName</span></span>
<span data-ttu-id="b44aa-126">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="b44aa-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="b44aa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b44aa-127">-ResourceGroupName</span></span>
<span data-ttu-id="b44aa-128">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b44aa-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b44aa-129">-Sourceıpaddress</span><span class="sxs-lookup"><span data-stu-id="b44aa-129">-SourceIPAddress</span></span>
<span data-ttu-id="b44aa-130">Kaynak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="b44aa-130">Source IP address.</span></span>

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

### <span data-ttu-id="b44aa-131">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="b44aa-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="b44aa-132">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="b44aa-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="b44aa-133">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="b44aa-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="b44aa-134">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b44aa-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="b44aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44aa-135">CommonParameters</span></span>
<span data-ttu-id="b44aa-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b44aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44aa-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b44aa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44aa-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b44aa-138">INPUTS</span></span>

### <span data-ttu-id="b44aa-139">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b44aa-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b44aa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b44aa-140">System.String</span></span>

## <span data-ttu-id="b44aa-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b44aa-141">OUTPUTS</span></span>

### <span data-ttu-id="b44aa-142">Microsoft. Azure. Commands. Network. model. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="b44aa-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="b44aa-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b44aa-143">NOTES</span></span>
<span data-ttu-id="b44aa-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sonraki, atlama</span><span class="sxs-lookup"><span data-stu-id="b44aa-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="b44aa-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b44aa-145">RELATED LINKS</span></span>

[<span data-ttu-id="b44aa-146">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="b44aa-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b44aa-147">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b44aa-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b44aa-148">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b44aa-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b44aa-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b44aa-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b44aa-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b44aa-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b44aa-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b44aa-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b44aa-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b44aa-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b44aa-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b44aa-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b44aa-154">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b44aa-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b44aa-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b44aa-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b44aa-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b44aa-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b44aa-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b44aa-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b44aa-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b44aa-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b44aa-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b44aa-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b44aa-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b44aa-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b44aa-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b44aa-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b44aa-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b44aa-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b44aa-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b44aa-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b44aa-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b44aa-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b44aa-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b44aa-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b44aa-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b44aa-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b44aa-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b44aa-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b44aa-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b44aa-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b44aa-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b44aa-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b44aa-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b44aa-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b44aa-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b44aa-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="b44aa-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b44aa-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
