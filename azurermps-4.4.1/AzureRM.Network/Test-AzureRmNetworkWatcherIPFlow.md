---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6e9700f91a9d6f8db5983604a0146f9d864dafd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594653"
---
# <span data-ttu-id="89396-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="89396-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="89396-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89396-102">SYNOPSIS</span></span>
<span data-ttu-id="89396-103">Paketin belirli bir hedefte veya belirli bir hedefle kabul edilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="89396-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89396-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89396-104">SYNTAX</span></span>

### <span data-ttu-id="89396-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89396-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89396-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="89396-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89396-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="89396-107">DESCRIPTION</span></span>
<span data-ttu-id="89396-108">Belirli bir VM kaynağı ve yerel ve uzak, IP adresleri ve bağlantı noktaları kullanılarak belirtilen yöne sahip bir paket için Test-AzureRmNetworkWatcherIPFlow cmdlet, pakete izin verilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="89396-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="89396-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89396-109">EXAMPLES</span></span>

### <span data-ttu-id="89396-110">Örnek 1:---Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="89396-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="89396-111">Bu abonelik için Batı merkezi ABD 'deki ağ Izleyicisi 'ni edinin, ardından VM ve ilişkili ağ arabirimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="89396-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="89396-112">Ardından ilk ağ arabiriminde, internet 'teki bir IP 'ye giden bağlantı için ilk ağ arabiriminden ilk IP 'yi kullanarak Test-AzureRmNetworkWatcherIPFlow çalışır.</span><span class="sxs-lookup"><span data-stu-id="89396-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="89396-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89396-113">PARAMETERS</span></span>

### <span data-ttu-id="89396-114">-Yön</span><span class="sxs-lookup"><span data-stu-id="89396-114">-Direction</span></span>
<span data-ttu-id="89396-115">Yönüyle.</span><span class="sxs-lookup"><span data-stu-id="89396-115">Direction.</span></span>

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

### <span data-ttu-id="89396-116">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="89396-116">-LocalIPAddress</span></span>
<span data-ttu-id="89396-117">Yerel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="89396-117">Local IP Address.</span></span>

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

### <span data-ttu-id="89396-118">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="89396-118">-LocalPort</span></span>
<span data-ttu-id="89396-119">Yerel bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="89396-119">Local Port.</span></span>

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

### <span data-ttu-id="89396-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="89396-120">-NetworkWatcher</span></span>
<span data-ttu-id="89396-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="89396-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="89396-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="89396-122">-NetworkWatcherName</span></span>
<span data-ttu-id="89396-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="89396-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="89396-124">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="89396-124">-Protocol</span></span>
<span data-ttu-id="89396-125">Kurallarının.</span><span class="sxs-lookup"><span data-stu-id="89396-125">Protocol.</span></span>

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

### <span data-ttu-id="89396-126">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="89396-126">-RemoteIPAddress</span></span>
<span data-ttu-id="89396-127">Uzak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="89396-127">Remote IP Address.</span></span>

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

### <span data-ttu-id="89396-128">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="89396-128">-RemotePort</span></span>
<span data-ttu-id="89396-129">Uzak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="89396-129">Remote port.</span></span>

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

### <span data-ttu-id="89396-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89396-130">-ResourceGroupName</span></span>
<span data-ttu-id="89396-131">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="89396-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="89396-132">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="89396-132">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="89396-133">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="89396-133">Target network interface Id.</span></span>

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

### <span data-ttu-id="89396-134">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="89396-134">-TargetVirtualMachineId</span></span>
<span data-ttu-id="89396-135">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="89396-135">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="89396-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89396-136">-DefaultProfile</span></span>
<span data-ttu-id="89396-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89396-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89396-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89396-138">CommonParameters</span></span>
<span data-ttu-id="89396-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89396-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89396-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89396-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89396-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89396-141">INPUTS</span></span>

### <span data-ttu-id="89396-142">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="89396-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="89396-143">System. String</span><span class="sxs-lookup"><span data-stu-id="89396-143">System.String</span></span>

## <span data-ttu-id="89396-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89396-144">OUTPUTS</span></span>

### <span data-ttu-id="89396-145">Microsoft. Azure. Commands. Network. model. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="89396-145">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="89396-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89396-146">NOTES</span></span>
<span data-ttu-id="89396-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="89396-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="89396-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89396-148">RELATED LINKS</span></span>

[<span data-ttu-id="89396-149">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="89396-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="89396-150">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="89396-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="89396-151">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="89396-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="89396-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="89396-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="89396-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="89396-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="89396-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="89396-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="89396-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="89396-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="89396-156">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89396-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89396-157">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="89396-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="89396-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89396-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89396-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89396-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89396-160">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89396-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
