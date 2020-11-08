---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: f91dc3942241237ddf3841d276ea442361d89987
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939509"
---
# <span data-ttu-id="ea4e2-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea4e2-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="ea4e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ea4e2-103">Yeni bir paket yakalama kaynağı oluşturur ve bir VM 'de paket yakalama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea4e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea4e2-104">SYNTAX</span></span>

### <span data-ttu-id="ea4e2-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ea4e2-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea4e2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ea4e2-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea4e2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea4e2-107">DESCRIPTION</span></span>
<span data-ttu-id="ea4e2-108">New-AzureRmNetworkWatcherPacketCapture cmdlet 'i yeni bir paket yakalama kaynağı oluşturur ve bir VM 'de paket yakalama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="ea4e2-109">Paket yakalama oturumlarının uzunluğu, bir zaman kısıtlaması veya boyut kısıtlaması aracılığıyla yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="ea4e2-110">Her paket için yakalanan verilerin miktarı da yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="ea4e2-111">Filtreler belirli bir paket yakalama oturumuna uygulanabilir ve bu da yakalanan paketlerin türünü özelleştirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="ea4e2-112">Süzgeçler, yerel ve uzak IP adresleri & adres aralıkları, yerel ve uzak bağlantı noktaları & bağlantı noktası aralıklarını ve oturum düzeyi iletişim kuralını da kısıtlayabilir.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="ea4e2-113">Filtreler birleştirilebilir ve size birden çok filtre uygulamak için çok sayıda filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="ea4e2-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea4e2-114">EXAMPLES</span></span>

### <span data-ttu-id="ea4e2-115">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma------</span><span class="sxs-lookup"><span data-stu-id="ea4e2-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="ea4e2-116">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="ea4e2-117">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="ea4e2-118">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="ea4e2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea4e2-119">PARAMETERS</span></span>

### <span data-ttu-id="ea4e2-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="ea4e2-120">-AsJob</span></span>
<span data-ttu-id="ea4e2-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ea4e2-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea4e2-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="ea4e2-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="ea4e2-123">Paket başına yakalanacak baytlar.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4e2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea4e2-124">-DefaultProfile</span></span>
<span data-ttu-id="ea4e2-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea4e2-126">-Filtre</span><span class="sxs-lookup"><span data-stu-id="ea4e2-126">-Filter</span></span>
<span data-ttu-id="ea4e2-127">Paket yakalama oturumu için filtreler.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-127">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4e2-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="ea4e2-128">-LocalFilePath</span></span>
<span data-ttu-id="ea4e2-129">Yerel dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-129">Local file path.</span></span>

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

### <span data-ttu-id="ea4e2-130">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ea4e2-130">-NetworkWatcher</span></span>
<span data-ttu-id="ea4e2-131">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="ea4e2-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ea4e2-132">-NetworkWatcherName</span></span>
<span data-ttu-id="ea4e2-133">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="ea4e2-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="ea4e2-134">-PacketCaptureName</span></span>
<span data-ttu-id="ea4e2-135">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-135">The packet capture name.</span></span>

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

### <span data-ttu-id="ea4e2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea4e2-136">-ResourceGroupName</span></span>
<span data-ttu-id="ea4e2-137">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ea4e2-138">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="ea4e2-138">-StorageAccountId</span></span>
<span data-ttu-id="ea4e2-139">Depolama hesabı kimliği.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-139">Storage account Id.</span></span>

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

### <span data-ttu-id="ea4e2-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="ea4e2-140">-StoragePath</span></span>
<span data-ttu-id="ea4e2-141">Depolama yolu.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-141">Storage path.</span></span>

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

### <span data-ttu-id="ea4e2-142">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="ea4e2-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="ea4e2-143">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="ea4e2-144">-Timelimitınseconds</span><span class="sxs-lookup"><span data-stu-id="ea4e2-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="ea4e2-145">Saniye cinsinden zaman sınırı.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4e2-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="ea4e2-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="ea4e2-147">Oturum başına toplam bayt sayısı.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea4e2-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea4e2-148">-Confirm</span></span>
<span data-ttu-id="ea4e2-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4e2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea4e2-150">-WhatIf</span></span>
<span data-ttu-id="ea4e2-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea4e2-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea4e2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea4e2-153">CommonParameters</span></span>
<span data-ttu-id="ea4e2-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea4e2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea4e2-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea4e2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea4e2-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea4e2-156">INPUTS</span></span>

### <span data-ttu-id="ea4e2-157">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ea4e2-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ea4e2-158">System. String System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="ea4e2-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="ea4e2-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea4e2-159">OUTPUTS</span></span>

### <span data-ttu-id="ea4e2-160">Microsoft. Azure. Commands. Network. model. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea4e2-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="ea4e2-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea4e2-161">NOTES</span></span>
<span data-ttu-id="ea4e2-162">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="ea4e2-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="ea4e2-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea4e2-163">RELATED LINKS</span></span>

[<span data-ttu-id="ea4e2-164">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ea4e2-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ea4e2-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea4e2-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea4e2-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea4e2-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea4e2-167">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea4e2-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ea4e2-168">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ea4e2-168">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ea4e2-169">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ea4e2-169">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ea4e2-170">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ea4e2-170">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ea4e2-171">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ea4e2-171">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ea4e2-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ea4e2-172">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ea4e2-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ea4e2-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ea4e2-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ea4e2-174">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ea4e2-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ea4e2-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

