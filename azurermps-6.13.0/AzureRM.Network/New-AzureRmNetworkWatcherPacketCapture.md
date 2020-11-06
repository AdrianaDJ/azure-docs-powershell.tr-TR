---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: ab7b6176f8453d1a3e5e0001e6b6c1e47c4de1cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594864"
---
# <span data-ttu-id="865c5-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="865c5-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="865c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="865c5-102">SYNOPSIS</span></span>
<span data-ttu-id="865c5-103">Yeni bir paket yakalama kaynağı oluşturur ve bir VM 'de paket yakalama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="865c5-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="865c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="865c5-104">SYNTAX</span></span>

### <span data-ttu-id="865c5-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="865c5-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="865c5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="865c5-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="865c5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="865c5-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="865c5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="865c5-108">DESCRIPTION</span></span>
<span data-ttu-id="865c5-109">New-AzureRmNetworkWatcherPacketCapture cmdlet 'i yeni bir paket yakalama kaynağı oluşturur ve bir VM 'de paket yakalama oturumu başlatır.</span><span class="sxs-lookup"><span data-stu-id="865c5-109">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="865c5-110">Paket yakalama oturumlarının uzunluğu, bir zaman kısıtlaması veya boyut kısıtlaması aracılığıyla yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="865c5-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="865c5-111">Her paket için yakalanan verilerin miktarı da yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="865c5-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="865c5-112">Filtreler belirli bir paket yakalama oturumuna uygulanabilir ve bu da yakalanan paketlerin türünü özelleştirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="865c5-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="865c5-113">Süzgeçler, yerel ve uzak IP adresleri & adres aralıkları, yerel ve uzak bağlantı noktaları & bağlantı noktası aralıklarını ve oturum düzeyi iletişim kuralını da kısıtlayabilir.</span><span class="sxs-lookup"><span data-stu-id="865c5-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="865c5-114">Filtreler birleştirilebilir ve size birden çok filtre uygulamak için çok sayıda filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="865c5-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="865c5-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="865c5-115">EXAMPLES</span></span>

### <span data-ttu-id="865c5-116">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma</span><span class="sxs-lookup"><span data-stu-id="865c5-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="865c5-117">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="865c5-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="865c5-118">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="865c5-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="865c5-119">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="865c5-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="865c5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="865c5-120">PARAMETERS</span></span>

### <span data-ttu-id="865c5-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="865c5-121">-AsJob</span></span>
<span data-ttu-id="865c5-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="865c5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="865c5-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="865c5-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="865c5-124">Paket başına yakalanacak baytlar.</span><span class="sxs-lookup"><span data-stu-id="865c5-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="865c5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865c5-125">-DefaultProfile</span></span>
<span data-ttu-id="865c5-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="865c5-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="865c5-127">-Filtre</span><span class="sxs-lookup"><span data-stu-id="865c5-127">-Filter</span></span>
<span data-ttu-id="865c5-128">Paket yakalama oturumu için filtreler.</span><span class="sxs-lookup"><span data-stu-id="865c5-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="865c5-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="865c5-129">-LocalFilePath</span></span>
<span data-ttu-id="865c5-130">Yerel dosya yolu.</span><span class="sxs-lookup"><span data-stu-id="865c5-130">Local file path.</span></span>

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

### <span data-ttu-id="865c5-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="865c5-131">-Location</span></span>
<span data-ttu-id="865c5-132">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="865c5-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="865c5-133">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="865c5-133">-NetworkWatcher</span></span>
<span data-ttu-id="865c5-134">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="865c5-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="865c5-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="865c5-135">-NetworkWatcherName</span></span>
<span data-ttu-id="865c5-136">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="865c5-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="865c5-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="865c5-137">-PacketCaptureName</span></span>
<span data-ttu-id="865c5-138">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="865c5-138">The packet capture name.</span></span>

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

### <span data-ttu-id="865c5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="865c5-139">-ResourceGroupName</span></span>
<span data-ttu-id="865c5-140">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="865c5-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="865c5-141">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="865c5-141">-StorageAccountId</span></span>
<span data-ttu-id="865c5-142">Depolama hesabı kimliği.</span><span class="sxs-lookup"><span data-stu-id="865c5-142">Storage account Id.</span></span>

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

### <span data-ttu-id="865c5-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="865c5-143">-StoragePath</span></span>
<span data-ttu-id="865c5-144">Depolama yolu.</span><span class="sxs-lookup"><span data-stu-id="865c5-144">Storage path.</span></span>

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

### <span data-ttu-id="865c5-145">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="865c5-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="865c5-146">Hedef sanal makine KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="865c5-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="865c5-147">-Timelimitınseconds</span><span class="sxs-lookup"><span data-stu-id="865c5-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="865c5-148">Saniye cinsinden zaman sınırı.</span><span class="sxs-lookup"><span data-stu-id="865c5-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="865c5-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="865c5-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="865c5-150">Oturum başına toplam bayt sayısı.</span><span class="sxs-lookup"><span data-stu-id="865c5-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="865c5-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="865c5-151">-Confirm</span></span>
<span data-ttu-id="865c5-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="865c5-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="865c5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="865c5-153">-WhatIf</span></span>
<span data-ttu-id="865c5-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="865c5-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="865c5-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="865c5-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="865c5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865c5-156">CommonParameters</span></span>
<span data-ttu-id="865c5-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="865c5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865c5-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="865c5-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865c5-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="865c5-159">INPUTS</span></span>

### <span data-ttu-id="865c5-160">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="865c5-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="865c5-161">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="865c5-161">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="865c5-162">System. String</span><span class="sxs-lookup"><span data-stu-id="865c5-162">System.String</span></span>
<span data-ttu-id="865c5-163">Parametreler: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="865c5-163">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="865c5-164">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="865c5-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="865c5-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="865c5-165">OUTPUTS</span></span>

### <span data-ttu-id="865c5-166">Microsoft. Azure. Commands. Network. modeller. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="865c5-166">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="865c5-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="865c5-167">NOTES</span></span>
<span data-ttu-id="865c5-168">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="865c5-168">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="865c5-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="865c5-169">RELATED LINKS</span></span>

[<span data-ttu-id="865c5-170">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="865c5-170">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="865c5-171">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="865c5-171">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="865c5-172">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="865c5-172">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="865c5-173">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="865c5-173">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="865c5-174">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="865c5-174">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="865c5-175">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="865c5-175">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="865c5-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="865c5-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="865c5-177">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="865c5-177">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="865c5-178">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="865c5-178">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="865c5-179">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="865c5-179">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="865c5-180">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="865c5-180">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="865c5-181">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="865c5-181">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="865c5-182">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="865c5-182">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="865c5-183">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="865c5-183">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="865c5-184">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="865c5-184">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="865c5-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="865c5-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="865c5-186">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="865c5-186">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="865c5-187">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="865c5-187">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="865c5-188">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="865c5-188">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="865c5-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="865c5-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="865c5-190">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="865c5-190">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="865c5-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="865c5-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="865c5-192">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="865c5-192">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="865c5-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="865c5-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="865c5-194">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="865c5-194">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="865c5-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="865c5-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="865c5-196">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="865c5-196">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)


