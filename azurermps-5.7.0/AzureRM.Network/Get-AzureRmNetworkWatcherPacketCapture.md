---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 912c2a424cda533dd5d576ab6744476b689d2ae1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765203"
---
# <span data-ttu-id="863f7-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="863f7-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="863f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="863f7-102">SYNOPSIS</span></span>
<span data-ttu-id="863f7-103">Bir paket yakalama kaynağının bilgilerini ve özelliklerini ve durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="863f7-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="863f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="863f7-104">SYNTAX</span></span>

### <span data-ttu-id="863f7-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="863f7-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="863f7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="863f7-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="863f7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="863f7-107">DESCRIPTION</span></span>
<span data-ttu-id="863f7-108">Get-AzureRmNetworkWatcherPacketCapture, paket yakalama kaynağının özelliklerini ve durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="863f7-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="863f7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="863f7-109">EXAMPLES</span></span>

### <span data-ttu-id="863f7-110">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma ve durumunu geri alma------</span><span class="sxs-lookup"><span data-stu-id="863f7-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="863f7-111">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="863f7-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="863f7-112">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="863f7-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="863f7-113">Ardından, yakalama oturumunun durumunu almak için Get-AzureRmNetworkWatcherPacketCapture çağrı yaptık.</span><span class="sxs-lookup"><span data-stu-id="863f7-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="863f7-114">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="863f7-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="863f7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="863f7-115">PARAMETERS</span></span>

### <span data-ttu-id="863f7-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="863f7-116">-AsJob</span></span>
<span data-ttu-id="863f7-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="863f7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="863f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="863f7-118">-DefaultProfile</span></span>
<span data-ttu-id="863f7-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="863f7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="863f7-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="863f7-120">-NetworkWatcher</span></span>
<span data-ttu-id="863f7-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="863f7-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="863f7-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="863f7-122">-NetworkWatcherName</span></span>
<span data-ttu-id="863f7-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="863f7-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="863f7-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="863f7-124">-PacketCaptureName</span></span>
<span data-ttu-id="863f7-125">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="863f7-125">The packet capture name.</span></span>

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

### <span data-ttu-id="863f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="863f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="863f7-127">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="863f7-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="863f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="863f7-128">CommonParameters</span></span>
<span data-ttu-id="863f7-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="863f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="863f7-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="863f7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="863f7-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="863f7-131">INPUTS</span></span>

### <span data-ttu-id="863f7-132">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="863f7-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="863f7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="863f7-133">System.String</span></span>

## <span data-ttu-id="863f7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="863f7-134">OUTPUTS</span></span>

### <span data-ttu-id="863f7-135">Microsoft. Azure. Commands. Network. modeller. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="863f7-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="863f7-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="863f7-136">NOTES</span></span>
<span data-ttu-id="863f7-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="863f7-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="863f7-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="863f7-138">RELATED LINKS</span></span>

[<span data-ttu-id="863f7-139">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="863f7-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="863f7-140">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="863f7-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="863f7-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="863f7-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="863f7-142">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="863f7-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="863f7-143">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="863f7-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="863f7-144">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="863f7-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="863f7-145">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="863f7-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="863f7-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="863f7-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="863f7-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="863f7-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="863f7-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="863f7-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="863f7-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="863f7-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="863f7-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="863f7-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

