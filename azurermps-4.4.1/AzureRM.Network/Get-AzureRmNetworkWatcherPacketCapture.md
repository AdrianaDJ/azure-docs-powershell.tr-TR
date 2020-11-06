---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 4cf1cb9149c0f821ad0e6164cd7c817b12ccc147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589256"
---
# <span data-ttu-id="e0888-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0888-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="e0888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0888-102">SYNOPSIS</span></span>
<span data-ttu-id="e0888-103">Bir paket yakalama kaynağının bilgilerini ve özelliklerini ve durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="e0888-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0888-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0888-104">SYNTAX</span></span>

### <span data-ttu-id="e0888-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0888-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0888-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e0888-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0888-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0888-107">DESCRIPTION</span></span>
<span data-ttu-id="e0888-108">Get-AzureRmNetworkWatcherPacketCapture, paket yakalama kaynağının özelliklerini ve durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="e0888-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="e0888-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0888-109">EXAMPLES</span></span>

### <span data-ttu-id="e0888-110">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma ve durumunu geri alma------</span><span class="sxs-lookup"><span data-stu-id="e0888-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="e0888-111">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="e0888-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="e0888-112">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="e0888-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="e0888-113">Ardından, yakalama oturumunun durumunu almak için Get-AzureRmNetworkWatcherPacketCapture çağrı yaptık.</span><span class="sxs-lookup"><span data-stu-id="e0888-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="e0888-114">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e0888-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="e0888-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0888-115">PARAMETERS</span></span>

### <span data-ttu-id="e0888-116">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="e0888-116">-NetworkWatcher</span></span>
<span data-ttu-id="e0888-117">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="e0888-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="e0888-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e0888-118">-NetworkWatcherName</span></span>
<span data-ttu-id="e0888-119">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="e0888-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="e0888-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="e0888-120">-PacketCaptureName</span></span>
<span data-ttu-id="e0888-121">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="e0888-121">The packet capture name.</span></span>

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

### <span data-ttu-id="e0888-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0888-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0888-123">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e0888-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e0888-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0888-124">-DefaultProfile</span></span>
<span data-ttu-id="e0888-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0888-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0888-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0888-126">CommonParameters</span></span>
<span data-ttu-id="e0888-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0888-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0888-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0888-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0888-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0888-129">INPUTS</span></span>

### <span data-ttu-id="e0888-130">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="e0888-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e0888-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e0888-131">System.String</span></span>

## <span data-ttu-id="e0888-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0888-132">OUTPUTS</span></span>

### <span data-ttu-id="e0888-133">Microsoft. Azure. Commands. Network. modeller. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="e0888-133">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="e0888-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0888-134">NOTES</span></span>
<span data-ttu-id="e0888-135">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="e0888-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="e0888-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0888-136">RELATED LINKS</span></span>

[<span data-ttu-id="e0888-137">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0888-137">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0888-138">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e0888-138">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="e0888-139">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0888-139">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0888-140">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0888-140">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0888-141">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="e0888-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e0888-142">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="e0888-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e0888-143">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="e0888-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e0888-144">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e0888-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e0888-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e0888-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="e0888-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e0888-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e0888-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e0888-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e0888-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e0888-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

