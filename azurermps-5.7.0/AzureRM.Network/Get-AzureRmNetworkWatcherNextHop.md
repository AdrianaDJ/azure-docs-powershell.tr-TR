---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 641678db33e8e7436bda103f95863aefbf31eb96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587533"
---
# <span data-ttu-id="f1c7b-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f1c7b-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="f1c7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c7b-103">Bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1c7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1c7b-104">SYNTAX</span></span>

### <span data-ttu-id="f1c7b-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1c7b-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1c7b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f1c7b-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1c7b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1c7b-107">DESCRIPTION</span></span>
<span data-ttu-id="f1c7b-108">Get-AzureRmNetworkWatcherNextHop cmdlet, bir VM 'den sonraki atlamayı alır.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="f1c7b-109">Sonraki atlama, Azure kaynağının türünü, bu kaynağın ilişkili IP adresini ve rotadaki sorumlu yönlendirme tablosu kuralını görüntülemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="f1c7b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1c7b-110">EXAMPLES</span></span>

### <span data-ttu-id="f1c7b-111">--Örnek 1: Internet ile iletişim kurarken sonraki atlama</span><span class="sxs-lookup"><span data-stu-id="f1c7b-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="f1c7b-112">Belirtilen sanal bir ana ağ arabiriminden 204.79.197.200 'e giden iletişimin sonraki atlaması</span><span class="sxs-lookup"><span data-stu-id="f1c7b-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="f1c7b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1c7b-113">PARAMETERS</span></span>

### <span data-ttu-id="f1c7b-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="f1c7b-114">-AsJob</span></span>
<span data-ttu-id="f1c7b-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f1c7b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1c7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c7b-116">-DefaultProfile</span></span>
<span data-ttu-id="f1c7b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1c7b-118">-Destinationıpaddress</span><span class="sxs-lookup"><span data-stu-id="f1c7b-118">-DestinationIPAddress</span></span>
<span data-ttu-id="f1c7b-119">Hedef IP adresi.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-119">Destination IP address.</span></span>

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

### <span data-ttu-id="f1c7b-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f1c7b-120">-NetworkWatcher</span></span>
<span data-ttu-id="f1c7b-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="f1c7b-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f1c7b-122">-NetworkWatcherName</span></span>
<span data-ttu-id="f1c7b-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="f1c7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1c7b-125">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f1c7b-126">-Sourceıpaddress</span><span class="sxs-lookup"><span data-stu-id="f1c7b-126">-SourceIPAddress</span></span>
<span data-ttu-id="f1c7b-127">Kaynak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-127">Source IP address.</span></span>

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

### <span data-ttu-id="f1c7b-128">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="f1c7b-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="f1c7b-129">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="f1c7b-130">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="f1c7b-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f1c7b-131">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f1c7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c7b-132">CommonParameters</span></span>
<span data-ttu-id="f1c7b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1c7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c7b-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c7b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c7b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1c7b-135">INPUTS</span></span>

### <span data-ttu-id="f1c7b-136">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f1c7b-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f1c7b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f1c7b-137">System.String</span></span>

## <span data-ttu-id="f1c7b-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1c7b-138">OUTPUTS</span></span>

### <span data-ttu-id="f1c7b-139">Microsoft. Azure. Commands. Network. model. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="f1c7b-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="f1c7b-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1c7b-140">NOTES</span></span>
<span data-ttu-id="f1c7b-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sonraki, atlama</span><span class="sxs-lookup"><span data-stu-id="f1c7b-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="f1c7b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1c7b-142">RELATED LINKS</span></span>

[<span data-ttu-id="f1c7b-143">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f1c7b-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f1c7b-144">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f1c7b-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f1c7b-145">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f1c7b-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f1c7b-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f1c7b-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f1c7b-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f1c7b-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f1c7b-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f1c7b-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f1c7b-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f1c7b-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f1c7b-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1c7b-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1c7b-151">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f1c7b-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f1c7b-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1c7b-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1c7b-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1c7b-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f1c7b-154">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f1c7b-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

