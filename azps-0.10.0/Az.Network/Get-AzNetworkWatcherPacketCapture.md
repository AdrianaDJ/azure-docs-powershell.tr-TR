---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935504"
---
# <span data-ttu-id="45cf9-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45cf9-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="45cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="45cf9-103">Bir paket yakalama kaynağının bilgilerini ve özelliklerini ve durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="45cf9-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="45cf9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45cf9-104">SYNTAX</span></span>

### <span data-ttu-id="45cf9-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="45cf9-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45cf9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="45cf9-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45cf9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="45cf9-107">DESCRIPTION</span></span>
<span data-ttu-id="45cf9-108">Get-AzNetworkWatcherPacketCapture, paket yakalama kaynağının özelliklerini ve durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="45cf9-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="45cf9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45cf9-109">EXAMPLES</span></span>

### <span data-ttu-id="45cf9-110">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma ve durumunu geri alma------</span><span class="sxs-lookup"><span data-stu-id="45cf9-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="45cf9-111">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="45cf9-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="45cf9-112">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="45cf9-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="45cf9-113">Ardından, yakalama oturumunun durumunu almak için Get-AzNetworkWatcherPacketCapture çağrı yaptık.</span><span class="sxs-lookup"><span data-stu-id="45cf9-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="45cf9-114">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="45cf9-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="45cf9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45cf9-115">PARAMETERS</span></span>

### <span data-ttu-id="45cf9-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="45cf9-116">-AsJob</span></span>
<span data-ttu-id="45cf9-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="45cf9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45cf9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45cf9-118">-DefaultProfile</span></span>
<span data-ttu-id="45cf9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45cf9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45cf9-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="45cf9-120">-NetworkWatcher</span></span>
<span data-ttu-id="45cf9-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="45cf9-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="45cf9-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="45cf9-122">-NetworkWatcherName</span></span>
<span data-ttu-id="45cf9-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="45cf9-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="45cf9-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="45cf9-124">-PacketCaptureName</span></span>
<span data-ttu-id="45cf9-125">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="45cf9-125">The packet capture name.</span></span>

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

### <span data-ttu-id="45cf9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45cf9-126">-ResourceGroupName</span></span>
<span data-ttu-id="45cf9-127">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="45cf9-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="45cf9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45cf9-128">CommonParameters</span></span>
<span data-ttu-id="45cf9-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45cf9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45cf9-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45cf9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45cf9-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45cf9-131">INPUTS</span></span>

### <span data-ttu-id="45cf9-132">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="45cf9-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="45cf9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="45cf9-133">System.String</span></span>

## <span data-ttu-id="45cf9-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45cf9-134">OUTPUTS</span></span>

### <span data-ttu-id="45cf9-135">Microsoft. Azure. Commands. Network. modeller. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="45cf9-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="45cf9-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45cf9-136">NOTES</span></span>
<span data-ttu-id="45cf9-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="45cf9-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="45cf9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45cf9-138">RELATED LINKS</span></span>

[<span data-ttu-id="45cf9-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45cf9-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45cf9-140">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="45cf9-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="45cf9-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45cf9-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45cf9-142">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="45cf9-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="45cf9-143">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="45cf9-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="45cf9-144">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="45cf9-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="45cf9-145">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="45cf9-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="45cf9-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="45cf9-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="45cf9-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="45cf9-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="45cf9-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="45cf9-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="45cf9-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="45cf9-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="45cf9-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="45cf9-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

