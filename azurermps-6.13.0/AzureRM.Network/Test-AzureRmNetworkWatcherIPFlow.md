---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6fc406d0af3ed451fbbf2f14c9ca8943256df744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594844"
---
# <span data-ttu-id="0d0f4-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0d0f4-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="0d0f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="0d0f4-103">Paketin belirli bir hedefte veya belirli bir hedefle kabul edilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d0f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d0f4-104">SYNTAX</span></span>

### <span data-ttu-id="0d0f4-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d0f4-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d0f4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0d0f4-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d0f4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0d0f4-107">SetByLocation</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d0f4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d0f4-108">DESCRIPTION</span></span>
<span data-ttu-id="0d0f4-109">Belirli bir VM kaynağı ve yerel ve uzak, IP adresleri ve bağlantı noktaları kullanılarak belirtilen yöne sahip bir paket için Test-AzureRmNetworkWatcherIPFlow cmdlet, pakete izin verilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-109">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="0d0f4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d0f4-110">EXAMPLES</span></span>

### <span data-ttu-id="0d0f4-111">Örnek 1: Test-AzureRmNetworkWatcherIPFlow çalışma</span><span class="sxs-lookup"><span data-stu-id="0d0f4-111">Example 1: Run Test-AzureRmNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="0d0f4-112">Bu abonelik için Batı merkezi ABD 'deki ağ Izleyicisi 'ni edinin, ardından VM ve ilişkili ağ arabirimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-112">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="0d0f4-113">Ardından ilk ağ arabiriminde, internet 'teki bir IP 'ye giden bağlantı için ilk ağ arabiriminden ilk IP 'yi kullanarak Test-AzureRmNetworkWatcherIPFlow çalışır.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-113">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="0d0f4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d0f4-114">PARAMETERS</span></span>

### <span data-ttu-id="0d0f4-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="0d0f4-115">-AsJob</span></span>
<span data-ttu-id="0d0f4-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0d0f4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d0f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d0f4-117">-DefaultProfile</span></span>
<span data-ttu-id="0d0f4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d0f4-119">-Yön</span><span class="sxs-lookup"><span data-stu-id="0d0f4-119">-Direction</span></span>
<span data-ttu-id="0d0f4-120">Yönüyle.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-120">Direction.</span></span>

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

### <span data-ttu-id="0d0f4-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="0d0f4-121">-LocalIPAddress</span></span>
<span data-ttu-id="0d0f4-122">Yerel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-122">Local IP Address.</span></span>

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

### <span data-ttu-id="0d0f4-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="0d0f4-123">-LocalPort</span></span>
<span data-ttu-id="0d0f4-124">Yerel bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-124">Local Port.</span></span>

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

### <span data-ttu-id="0d0f4-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="0d0f4-125">-Location</span></span>
<span data-ttu-id="0d0f4-126">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0d0f4-127">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d0f4-127">-NetworkWatcher</span></span>
<span data-ttu-id="0d0f4-128">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="0d0f4-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0d0f4-129">-NetworkWatcherName</span></span>
<span data-ttu-id="0d0f4-130">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="0d0f4-131">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="0d0f4-131">-Protocol</span></span>
<span data-ttu-id="0d0f4-132">Kurallarının.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-132">Protocol.</span></span>

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

### <span data-ttu-id="0d0f4-133">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="0d0f4-133">-RemoteIPAddress</span></span>
<span data-ttu-id="0d0f4-134">Uzak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="0d0f4-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="0d0f4-135">-RemotePort</span></span>
<span data-ttu-id="0d0f4-136">Uzak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-136">Remote port.</span></span>

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

### <span data-ttu-id="0d0f4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d0f4-137">-ResourceGroupName</span></span>
<span data-ttu-id="0d0f4-138">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0d0f4-139">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="0d0f4-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="0d0f4-140">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="0d0f4-141">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="0d0f4-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0d0f4-142">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="0d0f4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d0f4-143">CommonParameters</span></span>
<span data-ttu-id="0d0f4-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d0f4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d0f4-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d0f4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d0f4-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d0f4-146">INPUTS</span></span>

### <span data-ttu-id="0d0f4-147">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d0f4-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0d0f4-148">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d0f4-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="0d0f4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0d0f4-149">System.String</span></span>
<span data-ttu-id="0d0f4-150">Parametreler: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d0f4-150">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="0d0f4-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d0f4-151">OUTPUTS</span></span>

### <span data-ttu-id="0d0f4-152">Microsoft. Azure. Commands. Network. model. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="0d0f4-152">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="0d0f4-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d0f4-153">NOTES</span></span>
<span data-ttu-id="0d0f4-154">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="0d0f4-154">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="0d0f4-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d0f4-155">RELATED LINKS</span></span>

[<span data-ttu-id="0d0f4-156">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d0f4-156">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d0f4-157">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d0f4-157">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d0f4-158">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d0f4-158">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d0f4-159">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0d0f4-159">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="0d0f4-160">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0d0f4-160">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0d0f4-161">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0d0f4-161">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0d0f4-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0d0f4-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0d0f4-163">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d0f4-163">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d0f4-164">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0d0f4-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0d0f4-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d0f4-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d0f4-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d0f4-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d0f4-167">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d0f4-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d0f4-168">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d0f4-168">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0d0f4-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0d0f4-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0d0f4-170">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0d0f4-170">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="0d0f4-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d0f4-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d0f4-172">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d0f4-172">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d0f4-173">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d0f4-173">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d0f4-174">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0d0f4-174">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0d0f4-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d0f4-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d0f4-176">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d0f4-176">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0d0f4-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0d0f4-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0d0f4-178">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0d0f4-178">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0d0f4-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0d0f4-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0d0f4-180">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0d0f4-180">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0d0f4-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0d0f4-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="0d0f4-182">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0d0f4-182">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
