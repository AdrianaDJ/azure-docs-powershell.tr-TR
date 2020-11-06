---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 4c6a1e179cf0c6086035488d092232e85c570637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589508"
---
# <span data-ttu-id="78cf1-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="78cf1-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="78cf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="78cf1-103">Bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="78cf1-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78cf1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78cf1-104">SYNTAX</span></span>

### <span data-ttu-id="78cf1-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="78cf1-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78cf1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="78cf1-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78cf1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="78cf1-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78cf1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="78cf1-108">DESCRIPTION</span></span>
<span data-ttu-id="78cf1-109">Get-AzureRmNetworkWatcherNextHop cmdlet, bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="78cf1-109">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="78cf1-110">Sonraki atlama, Azure kaynağının türünü, bu kaynağın ilişkili IP adresini ve rotadaki sorumlu yönlendirme tablosu kuralını görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="78cf1-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="78cf1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78cf1-111">EXAMPLES</span></span>

### <span data-ttu-id="78cf1-112">Örnek 1: Internet IP 'si ile iletişim kurarken sonraki atlama</span><span class="sxs-lookup"><span data-stu-id="78cf1-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="78cf1-113">Belirtilen sanal bir ana ağ arabiriminden 204.79.197.200 'e giden iletişimin sonraki atlaması</span><span class="sxs-lookup"><span data-stu-id="78cf1-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="78cf1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78cf1-114">PARAMETERS</span></span>

### <span data-ttu-id="78cf1-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="78cf1-115">-AsJob</span></span>
<span data-ttu-id="78cf1-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="78cf1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78cf1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78cf1-117">-DefaultProfile</span></span>
<span data-ttu-id="78cf1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78cf1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78cf1-119">-Destinationıpaddress</span><span class="sxs-lookup"><span data-stu-id="78cf1-119">-DestinationIPAddress</span></span>
<span data-ttu-id="78cf1-120">Hedef IP adresi.</span><span class="sxs-lookup"><span data-stu-id="78cf1-120">Destination IP address.</span></span>

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

### <span data-ttu-id="78cf1-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="78cf1-121">-Location</span></span>
<span data-ttu-id="78cf1-122">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="78cf1-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="78cf1-123">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="78cf1-123">-NetworkWatcher</span></span>
<span data-ttu-id="78cf1-124">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="78cf1-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="78cf1-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="78cf1-125">-NetworkWatcherName</span></span>
<span data-ttu-id="78cf1-126">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="78cf1-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="78cf1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78cf1-127">-ResourceGroupName</span></span>
<span data-ttu-id="78cf1-128">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="78cf1-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="78cf1-129">-Sourceıpaddress</span><span class="sxs-lookup"><span data-stu-id="78cf1-129">-SourceIPAddress</span></span>
<span data-ttu-id="78cf1-130">Kaynak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="78cf1-130">Source IP address.</span></span>

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

### <span data-ttu-id="78cf1-131">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="78cf1-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="78cf1-132">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="78cf1-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="78cf1-133">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="78cf1-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="78cf1-134">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="78cf1-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="78cf1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78cf1-135">CommonParameters</span></span>
<span data-ttu-id="78cf1-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78cf1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78cf1-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78cf1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78cf1-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78cf1-138">INPUTS</span></span>

### <span data-ttu-id="78cf1-139">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="78cf1-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="78cf1-140">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="78cf1-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="78cf1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="78cf1-141">System.String</span></span>
<span data-ttu-id="78cf1-142">Parametreler: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="78cf1-142">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="78cf1-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78cf1-143">OUTPUTS</span></span>

### <span data-ttu-id="78cf1-144">Microsoft. Azure. Commands. Network. model. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="78cf1-144">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="78cf1-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78cf1-145">NOTES</span></span>
<span data-ttu-id="78cf1-146">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sonraki, atlama</span><span class="sxs-lookup"><span data-stu-id="78cf1-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="78cf1-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78cf1-147">RELATED LINKS</span></span>

[<span data-ttu-id="78cf1-148">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="78cf1-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="78cf1-149">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="78cf1-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="78cf1-150">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="78cf1-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="78cf1-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="78cf1-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="78cf1-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="78cf1-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="78cf1-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="78cf1-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="78cf1-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="78cf1-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="78cf1-155">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78cf1-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78cf1-156">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="78cf1-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="78cf1-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78cf1-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78cf1-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78cf1-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78cf1-159">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78cf1-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78cf1-160">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="78cf1-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="78cf1-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="78cf1-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="78cf1-162">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="78cf1-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="78cf1-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78cf1-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78cf1-164">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78cf1-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78cf1-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78cf1-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78cf1-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="78cf1-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="78cf1-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78cf1-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78cf1-168">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78cf1-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78cf1-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="78cf1-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="78cf1-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="78cf1-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="78cf1-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="78cf1-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="78cf1-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="78cf1-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="78cf1-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="78cf1-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="78cf1-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78cf1-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
