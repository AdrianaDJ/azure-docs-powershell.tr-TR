---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: d26f50768c561e05b4dc27ad829c063b73c5a336
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594621"
---
# <span data-ttu-id="0b388-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0b388-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="0b388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b388-102">SYNOPSIS</span></span>
<span data-ttu-id="0b388-103">Bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="0b388-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b388-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b388-104">SYNTAX</span></span>

### <span data-ttu-id="0b388-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b388-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b388-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0b388-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b388-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b388-107">DESCRIPTION</span></span>
<span data-ttu-id="0b388-108">Get-AzureRmNetworkWatcherNextHop cmdlet, bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="0b388-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="0b388-109">Sonraki atlama, Azure kaynağının türünü, bu kaynağın ilişkili IP adresini ve rotadaki sorumlu yönlendirme tablosu kuralını görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0b388-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="0b388-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b388-110">EXAMPLES</span></span>

### <span data-ttu-id="0b388-111">--Örnek 1: Internet ile iletişim kurarken sonraki atlama</span><span class="sxs-lookup"><span data-stu-id="0b388-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="0b388-112">Belirtilen sanal bir ana ağ arabiriminden 204.79.197.200 'e giden iletişimin sonraki atlaması</span><span class="sxs-lookup"><span data-stu-id="0b388-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="0b388-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b388-113">PARAMETERS</span></span>

### <span data-ttu-id="0b388-114">-Destinationıpaddress</span><span class="sxs-lookup"><span data-stu-id="0b388-114">-DestinationIPAddress</span></span>
<span data-ttu-id="0b388-115">Hedef IP adresi.</span><span class="sxs-lookup"><span data-stu-id="0b388-115">Destination IP address.</span></span>

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

### <span data-ttu-id="0b388-116">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0b388-116">-NetworkWatcher</span></span>
<span data-ttu-id="0b388-117">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="0b388-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="0b388-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0b388-118">-NetworkWatcherName</span></span>
<span data-ttu-id="0b388-119">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="0b388-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="0b388-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b388-120">-ResourceGroupName</span></span>
<span data-ttu-id="0b388-121">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0b388-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0b388-122">-Sourceıpaddress</span><span class="sxs-lookup"><span data-stu-id="0b388-122">-SourceIPAddress</span></span>
<span data-ttu-id="0b388-123">Kaynak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="0b388-123">Source IP address.</span></span>

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

### <span data-ttu-id="0b388-124">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="0b388-124">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="0b388-125">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="0b388-125">Target network interface Id.</span></span>

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

### <span data-ttu-id="0b388-126">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="0b388-126">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0b388-127">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0b388-127">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="0b388-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b388-128">-DefaultProfile</span></span>
<span data-ttu-id="0b388-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b388-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b388-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b388-130">CommonParameters</span></span>
<span data-ttu-id="0b388-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b388-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b388-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b388-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b388-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b388-133">INPUTS</span></span>

### <span data-ttu-id="0b388-134">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0b388-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0b388-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0b388-135">System.String</span></span>

## <span data-ttu-id="0b388-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b388-136">OUTPUTS</span></span>

### <span data-ttu-id="0b388-137">Microsoft. Azure. Commands. Network. model. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="0b388-137">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="0b388-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b388-138">NOTES</span></span>
<span data-ttu-id="0b388-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sonraki, atlama</span><span class="sxs-lookup"><span data-stu-id="0b388-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="0b388-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b388-140">RELATED LINKS</span></span>

[<span data-ttu-id="0b388-141">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0b388-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0b388-142">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0b388-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0b388-143">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0b388-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0b388-144">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0b388-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0b388-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0b388-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0b388-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0b388-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0b388-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0b388-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0b388-148">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0b388-148">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0b388-149">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0b388-149">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0b388-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0b388-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0b388-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0b388-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0b388-152">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0b388-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

