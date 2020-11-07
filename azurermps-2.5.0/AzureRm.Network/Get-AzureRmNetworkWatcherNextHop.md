---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
ms.openlocfilehash: 41c76d78ad27ff889f2dc3e7be254bcc88668023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939926"
---
# <span data-ttu-id="7ec9d-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7ec9d-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="7ec9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ec9d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec9d-103">Bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ec9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ec9d-104">SYNTAX</span></span>

### <span data-ttu-id="7ec9d-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ec9d-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ec9d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7ec9d-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ec9d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ec9d-107">DESCRIPTION</span></span>
<span data-ttu-id="7ec9d-108">Get-AzureRmNetworkWatcherNextHop cmdlet, bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="7ec9d-109">Sonraki atlama, Azure kaynağının türünü, bu kaynağın ilişkili IP adresini ve rotadaki sorumlu yönlendirme tablosu kuralını görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="7ec9d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ec9d-110">EXAMPLES</span></span>

### <span data-ttu-id="7ec9d-111">--Örnek 1: Internet ile iletişim kurarken sonraki atlama</span><span class="sxs-lookup"><span data-stu-id="7ec9d-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="7ec9d-112">Belirtilen sanal bir ana ağ arabiriminden 204.79.197.200 'e giden iletişimin sonraki atlaması</span><span class="sxs-lookup"><span data-stu-id="7ec9d-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="7ec9d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ec9d-113">PARAMETERS</span></span>

### <span data-ttu-id="7ec9d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="7ec9d-114">-AsJob</span></span>
<span data-ttu-id="7ec9d-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7ec9d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ec9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec9d-116">-DefaultProfile</span></span>
<span data-ttu-id="7ec9d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ec9d-118">-Destinationıpaddress</span><span class="sxs-lookup"><span data-stu-id="7ec9d-118">-DestinationIPAddress</span></span>
<span data-ttu-id="7ec9d-119">Hedef IP adresi.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-119">Destination IP address.</span></span>

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

### <span data-ttu-id="7ec9d-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="7ec9d-120">-NetworkWatcher</span></span>
<span data-ttu-id="7ec9d-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="7ec9d-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7ec9d-122">-NetworkWatcherName</span></span>
<span data-ttu-id="7ec9d-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="7ec9d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ec9d-124">-ResourceGroupName</span></span>
<span data-ttu-id="7ec9d-125">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7ec9d-126">-Sourceıpaddress</span><span class="sxs-lookup"><span data-stu-id="7ec9d-126">-SourceIPAddress</span></span>
<span data-ttu-id="7ec9d-127">Kaynak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-127">Source IP address.</span></span>

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

### <span data-ttu-id="7ec9d-128">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="7ec9d-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="7ec9d-129">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="7ec9d-130">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="7ec9d-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="7ec9d-131">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="7ec9d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec9d-132">CommonParameters</span></span>
<span data-ttu-id="7ec9d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ec9d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec9d-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ec9d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec9d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ec9d-135">INPUTS</span></span>

### <span data-ttu-id="7ec9d-136">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="7ec9d-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7ec9d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec9d-137">System.String</span></span>

## <span data-ttu-id="7ec9d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ec9d-138">OUTPUTS</span></span>

### <span data-ttu-id="7ec9d-139">Microsoft. Azure. Commands. Network. model. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="7ec9d-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="7ec9d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ec9d-140">NOTES</span></span>
<span data-ttu-id="7ec9d-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sonraki, atlama</span><span class="sxs-lookup"><span data-stu-id="7ec9d-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="7ec9d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ec9d-142">RELATED LINKS</span></span>

[<span data-ttu-id="7ec9d-143">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="7ec9d-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7ec9d-144">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="7ec9d-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7ec9d-145">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="7ec9d-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7ec9d-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7ec9d-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7ec9d-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7ec9d-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7ec9d-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7ec9d-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7ec9d-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7ec9d-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7ec9d-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ec9d-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ec9d-151">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7ec9d-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7ec9d-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ec9d-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ec9d-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ec9d-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ec9d-154">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ec9d-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

