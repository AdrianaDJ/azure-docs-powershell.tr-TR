---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935506"
---
# <span data-ttu-id="d1852-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d1852-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="d1852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1852-102">SYNOPSIS</span></span>
<span data-ttu-id="d1852-103">Bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="d1852-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="d1852-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1852-104">SYNTAX</span></span>

### <span data-ttu-id="d1852-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d1852-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1852-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d1852-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1852-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1852-107">DESCRIPTION</span></span>
<span data-ttu-id="d1852-108">Get-AzNetworkWatcherNextHop cmdlet, bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="d1852-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="d1852-109">Sonraki atlama, Azure kaynağının türünü, bu kaynağın ilişkili IP adresini ve rotadaki sorumlu yönlendirme tablosu kuralını görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d1852-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="d1852-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1852-110">EXAMPLES</span></span>

### <span data-ttu-id="d1852-111">--Örnek 1: Internet ile iletişim kurarken sonraki atlama</span><span class="sxs-lookup"><span data-stu-id="d1852-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="d1852-112">Belirtilen sanal bir ana ağ arabiriminden 204.79.197.200 'e giden iletişimin sonraki atlaması</span><span class="sxs-lookup"><span data-stu-id="d1852-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="d1852-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1852-113">PARAMETERS</span></span>

### <span data-ttu-id="d1852-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d1852-114">-AsJob</span></span>
<span data-ttu-id="d1852-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d1852-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1852-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1852-116">-DefaultProfile</span></span>
<span data-ttu-id="d1852-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1852-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1852-118">-Destinationıpaddress</span><span class="sxs-lookup"><span data-stu-id="d1852-118">-DestinationIPAddress</span></span>
<span data-ttu-id="d1852-119">Hedef IP adresi.</span><span class="sxs-lookup"><span data-stu-id="d1852-119">Destination IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1852-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d1852-120">-NetworkWatcher</span></span>
<span data-ttu-id="d1852-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="d1852-121">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1852-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d1852-122">-NetworkWatcherName</span></span>
<span data-ttu-id="d1852-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="d1852-123">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1852-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1852-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1852-125">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d1852-125">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1852-126">-Sourceıpaddress</span><span class="sxs-lookup"><span data-stu-id="d1852-126">-SourceIPAddress</span></span>
<span data-ttu-id="d1852-127">Kaynak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="d1852-127">Source IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1852-128">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="d1852-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="d1852-129">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="d1852-129">Target network interface Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1852-130">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="d1852-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d1852-131">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d1852-131">The target virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1852-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1852-132">CommonParameters</span></span>
<span data-ttu-id="d1852-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1852-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1852-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1852-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1852-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1852-135">INPUTS</span></span>

### <span data-ttu-id="d1852-136">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d1852-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d1852-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d1852-137">System.String</span></span>

## <span data-ttu-id="d1852-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1852-138">OUTPUTS</span></span>

### <span data-ttu-id="d1852-139">Microsoft. Azure. Commands. Network. model. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="d1852-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="d1852-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1852-140">NOTES</span></span>
<span data-ttu-id="d1852-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sonraki, atlama</span><span class="sxs-lookup"><span data-stu-id="d1852-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="d1852-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1852-142">RELATED LINKS</span></span>

[<span data-ttu-id="d1852-143">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="d1852-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d1852-144">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d1852-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d1852-145">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d1852-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d1852-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d1852-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d1852-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d1852-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d1852-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d1852-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d1852-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d1852-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d1852-150">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d1852-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d1852-151">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d1852-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d1852-152">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d1852-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d1852-153">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d1852-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d1852-154">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d1852-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

