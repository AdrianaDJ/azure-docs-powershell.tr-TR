---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 577f883affc772c01343a57a533c5ae06eccf31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764415"
---
# <span data-ttu-id="866e6-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="866e6-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="866e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="866e6-102">SYNOPSIS</span></span>
<span data-ttu-id="866e6-103">Paketin belirli bir hedefte veya belirli bir hedefle kabul edilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="866e6-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="866e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="866e6-104">SYNTAX</span></span>

### <span data-ttu-id="866e6-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="866e6-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="866e6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="866e6-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="866e6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="866e6-107">DESCRIPTION</span></span>
<span data-ttu-id="866e6-108">Belirli bir VM kaynağı ve yerel ve uzak, IP adresleri ve bağlantı noktaları kullanılarak belirtilen yöne sahip bir paket için Test-AzureRmNetworkWatcherIPFlow cmdlet, pakete izin verilip verilmediğini döndürür.</span><span class="sxs-lookup"><span data-stu-id="866e6-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="866e6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="866e6-109">EXAMPLES</span></span>

### <span data-ttu-id="866e6-110">Örnek 1:---Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="866e6-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="866e6-111">Bu abonelik için Batı merkezi ABD 'deki ağ Izleyicisi 'ni edinin, ardından VM ve ilişkili ağ arabirimlerini alır.</span><span class="sxs-lookup"><span data-stu-id="866e6-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="866e6-112">Ardından ilk ağ arabiriminde, internet 'teki bir IP 'ye giden bağlantı için ilk ağ arabiriminden ilk IP 'yi kullanarak Test-AzureRmNetworkWatcherIPFlow çalışır.</span><span class="sxs-lookup"><span data-stu-id="866e6-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="866e6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="866e6-113">PARAMETERS</span></span>

### <span data-ttu-id="866e6-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="866e6-114">-AsJob</span></span>
<span data-ttu-id="866e6-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="866e6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="866e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866e6-116">-DefaultProfile</span></span>
<span data-ttu-id="866e6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="866e6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="866e6-118">-Yön</span><span class="sxs-lookup"><span data-stu-id="866e6-118">-Direction</span></span>
<span data-ttu-id="866e6-119">Yönüyle.</span><span class="sxs-lookup"><span data-stu-id="866e6-119">Direction.</span></span>

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

### <span data-ttu-id="866e6-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="866e6-120">-LocalIPAddress</span></span>
<span data-ttu-id="866e6-121">Yerel IP adresi.</span><span class="sxs-lookup"><span data-stu-id="866e6-121">Local IP Address.</span></span>

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

### <span data-ttu-id="866e6-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="866e6-122">-LocalPort</span></span>
<span data-ttu-id="866e6-123">Yerel bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="866e6-123">Local Port.</span></span>

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

### <span data-ttu-id="866e6-124">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="866e6-124">-NetworkWatcher</span></span>
<span data-ttu-id="866e6-125">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="866e6-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="866e6-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="866e6-126">-NetworkWatcherName</span></span>
<span data-ttu-id="866e6-127">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="866e6-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="866e6-128">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="866e6-128">-Protocol</span></span>
<span data-ttu-id="866e6-129">Kurallarının.</span><span class="sxs-lookup"><span data-stu-id="866e6-129">Protocol.</span></span>

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

### <span data-ttu-id="866e6-130">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="866e6-130">-RemoteIPAddress</span></span>
<span data-ttu-id="866e6-131">Uzak IP adresi.</span><span class="sxs-lookup"><span data-stu-id="866e6-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="866e6-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="866e6-132">-RemotePort</span></span>
<span data-ttu-id="866e6-133">Uzak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="866e6-133">Remote port.</span></span>

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

### <span data-ttu-id="866e6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866e6-134">-ResourceGroupName</span></span>
<span data-ttu-id="866e6-135">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="866e6-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="866e6-136">-Targetnetworkınterfaceıd</span><span class="sxs-lookup"><span data-stu-id="866e6-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="866e6-137">Hedef ağ arabirim kimliği.</span><span class="sxs-lookup"><span data-stu-id="866e6-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="866e6-138">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="866e6-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="866e6-139">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="866e6-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="866e6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866e6-140">CommonParameters</span></span>
<span data-ttu-id="866e6-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="866e6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866e6-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866e6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866e6-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="866e6-143">INPUTS</span></span>

### <span data-ttu-id="866e6-144">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="866e6-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="866e6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="866e6-145">System.String</span></span>

## <span data-ttu-id="866e6-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="866e6-146">OUTPUTS</span></span>

### <span data-ttu-id="866e6-147">Microsoft. Azure. Commands. Network. model. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="866e6-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="866e6-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="866e6-148">NOTES</span></span>
<span data-ttu-id="866e6-149">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="866e6-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="866e6-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="866e6-150">RELATED LINKS</span></span>

[<span data-ttu-id="866e6-151">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="866e6-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="866e6-152">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="866e6-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="866e6-153">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="866e6-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="866e6-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="866e6-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="866e6-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="866e6-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="866e6-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="866e6-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="866e6-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="866e6-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="866e6-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="866e6-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="866e6-159">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="866e6-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="866e6-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="866e6-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="866e6-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="866e6-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="866e6-162">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="866e6-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
