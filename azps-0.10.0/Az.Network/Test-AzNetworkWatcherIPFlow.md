---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936477"
---
# <span data-ttu-id="d3c63-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d3c63-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="d3c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3c63-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c63-103">Paketin belirli bir hedefte veya belirli bir hedefle kabul edilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3c63-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="d3c63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3c63-104">SYNTAX</span></span>

### <span data-ttu-id="d3c63-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3c63-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3c63-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d3c63-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3c63-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3c63-107">DESCRIPTION</span></span>
<span data-ttu-id="d3c63-108">Belirli bir VM kaynağı ve yerel ve uzak, IP adresleri ve bağlantı noktaları kullanılarak belirtilen yöne sahip bir paket için Test-AzNetworkWatcherIPFlow cmdlet, pakete izin verilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3c63-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="d3c63-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3c63-109">EXAMPLES</span></span>

### <span data-ttu-id="d3c63-110">Örnek 1:---Test-AzNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="d3c63-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="d3c63-111">Bu abonelik için Batı merkezi ABD 'deki ağ Izleyicisi 'ni edinin, ardından VM ve ilişkili ağ arabirimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d3c63-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="d3c63-112">Ardından ilk ağ arabiriminde, internet 'teki bir IP 'ye giden bağlantı için ilk ağ arabiriminden ilk IP 'yi kullanarak Test-AzNetworkWatcherIPFlow çalışır.</span><span class="sxs-lookup"><span data-stu-id="d3c63-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="d3c63-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3c63-113">PARAMETERS</span></span>

### <span data-ttu-id="d3c63-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d3c63-114">-AsJob</span></span>
<span data-ttu-id="d3c63-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d3c63-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3c63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c63-116">-DefaultProfile</span></span>
<span data-ttu-id="d3c63-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3c63-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3c63-118">-Yön</span><span class="sxs-lookup"><span data-stu-id="d3c63-118">-Direction</span></span>
<span data-ttu-id="d3c63-119">Yönüyle.</span><span class="sxs-lookup"><span data-stu-id="d3c63-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c63-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="d3c63-120">-LocalIPAddress</span></span>
<span data-ttu-id="d3c63-121">Yerel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="d3c63-121">Local IP Address.</span></span>

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

### <span data-ttu-id="d3c63-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="d3c63-122">-LocalPort</span></span>
<span data-ttu-id="d3c63-123">Yerel bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="d3c63-123">Local Port.</span></span>

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

### <span data-ttu-id="d3c63-124">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d3c63-124">-NetworkWatcher</span></span>
<span data-ttu-id="d3c63-125">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="d3c63-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="d3c63-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d3c63-126">-NetworkWatcherName</span></span>
<span data-ttu-id="d3c63-127">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="d3c63-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="d3c63-128">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d3c63-128">-Protocol</span></span>
<span data-ttu-id="d3c63-129">Kurallarının.</span><span class="sxs-lookup"><span data-stu-id="d3c63-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3c63-130">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="d3c63-130">-RemoteIPAddress</span></span>
<span data-ttu-id="d3c63-131">Uzak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="d3c63-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="d3c63-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="d3c63-132">-RemotePort</span></span>
<span data-ttu-id="d3c63-133">Uzak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="d3c63-133">Remote port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c63-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c63-134">-ResourceGroupName</span></span>
<span data-ttu-id="d3c63-135">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d3c63-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d3c63-136">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="d3c63-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="d3c63-137">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="d3c63-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="d3c63-138">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="d3c63-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d3c63-139">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d3c63-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="d3c63-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c63-140">CommonParameters</span></span>
<span data-ttu-id="d3c63-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3c63-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c63-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c63-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c63-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3c63-143">INPUTS</span></span>

### <span data-ttu-id="d3c63-144">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d3c63-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d3c63-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d3c63-145">System.String</span></span>

## <span data-ttu-id="d3c63-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3c63-146">OUTPUTS</span></span>

### <span data-ttu-id="d3c63-147">Microsoft. Azure. Commands. Network. model. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="d3c63-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="d3c63-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3c63-148">NOTES</span></span>
<span data-ttu-id="d3c63-149">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="d3c63-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="d3c63-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3c63-150">RELATED LINKS</span></span>

[<span data-ttu-id="d3c63-151">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="d3c63-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d3c63-152">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d3c63-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d3c63-153">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d3c63-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d3c63-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d3c63-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d3c63-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d3c63-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d3c63-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d3c63-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d3c63-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d3c63-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d3c63-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d3c63-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d3c63-159">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d3c63-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d3c63-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d3c63-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d3c63-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d3c63-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d3c63-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d3c63-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
