---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b67d393f0ab24fff15da14b9ce6f6fb1b567d0b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918223"
---
# <span data-ttu-id="57d9c-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57d9c-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="57d9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="57d9c-103">Yeni bir paket yakalama kaynağı oluşturur ve bir VM 'de paket yakalama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="57d9c-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="57d9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57d9c-104">SYNTAX</span></span>

### <span data-ttu-id="57d9c-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57d9c-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57d9c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="57d9c-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57d9c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="57d9c-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57d9c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="57d9c-108">DESCRIPTION</span></span>
<span data-ttu-id="57d9c-109">New-AzNetworkWatcherPacketCapture cmdlet 'i yeni bir paket yakalama kaynağı oluşturur ve bir VM 'de paket yakalama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="57d9c-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="57d9c-110">Paket yakalama oturumlarının uzunluğu, bir zaman kısıtlaması veya boyut kısıtlaması aracılığıyla yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="57d9c-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="57d9c-111">Her paket için yakalanan verilerin miktarı da yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="57d9c-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="57d9c-112">Filtreler belirli bir paket yakalama oturumuna uygulanabilir ve bu da yakalanan paketlerin türünü özelleştirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="57d9c-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="57d9c-113">Süzgeçler, yerel ve uzak IP adresleri & adres aralıkları, yerel ve uzak bağlantı noktaları & bağlantı noktası aralıklarını ve oturum düzeyi iletişim kuralını da kısıtlayabilir.</span><span class="sxs-lookup"><span data-stu-id="57d9c-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="57d9c-114">Filtreler birleştirilebilir ve size birden çok filtre uygulamak için çok sayıda filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57d9c-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="57d9c-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57d9c-115">EXAMPLES</span></span>

### <span data-ttu-id="57d9c-116">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma</span><span class="sxs-lookup"><span data-stu-id="57d9c-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="57d9c-117">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="57d9c-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="57d9c-118">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="57d9c-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="57d9c-119">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="57d9c-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="57d9c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57d9c-120">PARAMETERS</span></span>

### <span data-ttu-id="57d9c-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="57d9c-121">-AsJob</span></span>
<span data-ttu-id="57d9c-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="57d9c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57d9c-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="57d9c-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="57d9c-124">Paket başına yakalanacak baytlar.</span><span class="sxs-lookup"><span data-stu-id="57d9c-124">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d9c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57d9c-125">-DefaultProfile</span></span>
<span data-ttu-id="57d9c-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57d9c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d9c-127">-Filtre</span><span class="sxs-lookup"><span data-stu-id="57d9c-127">-Filter</span></span>
<span data-ttu-id="57d9c-128">Paket yakalama oturumu için filtreler.</span><span class="sxs-lookup"><span data-stu-id="57d9c-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d9c-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="57d9c-129">-LocalFilePath</span></span>
<span data-ttu-id="57d9c-130">Yerel dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="57d9c-130">Local file path.</span></span>

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

### <span data-ttu-id="57d9c-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="57d9c-131">-Location</span></span>
<span data-ttu-id="57d9c-132">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="57d9c-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="57d9c-133">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="57d9c-133">-NetworkWatcher</span></span>
<span data-ttu-id="57d9c-134">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="57d9c-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="57d9c-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="57d9c-135">-NetworkWatcherName</span></span>
<span data-ttu-id="57d9c-136">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="57d9c-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="57d9c-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="57d9c-137">-PacketCaptureName</span></span>
<span data-ttu-id="57d9c-138">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="57d9c-138">The packet capture name.</span></span>

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

### <span data-ttu-id="57d9c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57d9c-139">-ResourceGroupName</span></span>
<span data-ttu-id="57d9c-140">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="57d9c-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="57d9c-141">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="57d9c-141">-StorageAccountId</span></span>
<span data-ttu-id="57d9c-142">Depolama hesabı kimliği.</span><span class="sxs-lookup"><span data-stu-id="57d9c-142">Storage account Id.</span></span>

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

### <span data-ttu-id="57d9c-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="57d9c-143">-StoragePath</span></span>
<span data-ttu-id="57d9c-144">Depolama yolu.</span><span class="sxs-lookup"><span data-stu-id="57d9c-144">Storage path.</span></span>

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

### <span data-ttu-id="57d9c-145">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="57d9c-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="57d9c-146">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="57d9c-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="57d9c-147">-Timelimitınseconds</span><span class="sxs-lookup"><span data-stu-id="57d9c-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="57d9c-148">Saniye cinsinden zaman sınırı.</span><span class="sxs-lookup"><span data-stu-id="57d9c-148">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d9c-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="57d9c-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="57d9c-150">Oturum başına toplam bayt sayısı.</span><span class="sxs-lookup"><span data-stu-id="57d9c-150">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57d9c-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="57d9c-151">-Confirm</span></span>
<span data-ttu-id="57d9c-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57d9c-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d9c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57d9c-153">-WhatIf</span></span>
<span data-ttu-id="57d9c-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57d9c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57d9c-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57d9c-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57d9c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57d9c-156">CommonParameters</span></span>
<span data-ttu-id="57d9c-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57d9c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57d9c-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57d9c-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57d9c-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57d9c-159">INPUTS</span></span>

### <span data-ttu-id="57d9c-160">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="57d9c-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="57d9c-161">System. String</span><span class="sxs-lookup"><span data-stu-id="57d9c-161">System.String</span></span>

### <span data-ttu-id="57d9c-162">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="57d9c-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="57d9c-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57d9c-163">OUTPUTS</span></span>

### <span data-ttu-id="57d9c-164">Microsoft. Azure. Commands. Network. modeller. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="57d9c-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="57d9c-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57d9c-165">NOTES</span></span>
<span data-ttu-id="57d9c-166">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="57d9c-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="57d9c-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57d9c-167">RELATED LINKS</span></span>

[<span data-ttu-id="57d9c-168">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="57d9c-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="57d9c-169">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="57d9c-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="57d9c-170">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="57d9c-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="57d9c-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="57d9c-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="57d9c-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="57d9c-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="57d9c-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="57d9c-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="57d9c-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="57d9c-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="57d9c-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57d9c-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="57d9c-176">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="57d9c-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="57d9c-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57d9c-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="57d9c-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57d9c-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="57d9c-179">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57d9c-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="57d9c-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="57d9c-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="57d9c-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="57d9c-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="57d9c-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="57d9c-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="57d9c-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57d9c-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57d9c-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57d9c-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57d9c-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57d9c-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57d9c-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="57d9c-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="57d9c-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57d9c-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57d9c-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57d9c-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="57d9c-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="57d9c-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="57d9c-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="57d9c-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="57d9c-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="57d9c-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="57d9c-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="57d9c-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="57d9c-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="57d9c-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="57d9c-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="57d9c-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


