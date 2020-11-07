---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
ms.openlocfilehash: 1d6054307ad1e499fbb36342f6c81e7e32227f37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939288"
---
# <span data-ttu-id="332b6-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="332b6-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="332b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="332b6-102">SYNOPSIS</span></span>
<span data-ttu-id="332b6-103">Yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="332b6-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="332b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="332b6-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="332b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="332b6-105">DESCRIPTION</span></span>
<span data-ttu-id="332b6-106">New-AzureRmPacketCaptureFilterConfig cmdlet 'i yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="332b6-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="332b6-107">Bu nesne, belirtilen ölçütleri kullanarak paket yakalama oturumu sırasında yakalanan paketlerin türünü sınırlandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="332b6-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="332b6-108">New-AzureRmNetworkWatcherPacketCapture cmdlet, birleştirilebilir yakalama oturumlarını etkinleştirmek için birden çok filtre nesnesi kabul edebilir.</span><span class="sxs-lookup"><span data-stu-id="332b6-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="332b6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="332b6-109">EXAMPLES</span></span>

### <span data-ttu-id="332b6-110">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma------</span><span class="sxs-lookup"><span data-stu-id="332b6-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="332b6-111">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="332b6-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="332b6-112">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="332b6-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="332b6-113">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="332b6-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="332b6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="332b6-114">PARAMETERS</span></span>

### <span data-ttu-id="332b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="332b6-115">-DefaultProfile</span></span>
<span data-ttu-id="332b6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="332b6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="332b6-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="332b6-117">-LocalIPAddress</span></span>
<span data-ttu-id="332b6-118">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="332b6-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="332b6-119">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="332b6-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="332b6-120">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="332b6-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="332b6-121">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="332b6-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="332b6-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="332b6-122">-LocalPort</span></span>
<span data-ttu-id="332b6-123">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="332b6-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="332b6-124">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="332b6-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="332b6-125">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="332b6-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="332b6-126">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="332b6-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="332b6-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="332b6-127">-Protocol</span></span>
<span data-ttu-id="332b6-128">Filtre uygulanacak procotol belirtir.</span><span class="sxs-lookup"><span data-stu-id="332b6-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="332b6-129">Kabul edilebilir değerler "TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="332b6-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="332b6-130">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="332b6-130">-RemoteIPAddress</span></span>
<span data-ttu-id="332b6-131">Filtre uygulanacak uzak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="332b6-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="332b6-132">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="332b6-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="332b6-133">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="332b6-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="332b6-134">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="332b6-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="332b6-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="332b6-135">-RemotePort</span></span>
<span data-ttu-id="332b6-136">Filtre uygulanacak uzak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="332b6-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="332b6-137">Uzak bağlantı noktası örnek girişleri: tek çıkışlı girdi için "80".</span><span class="sxs-lookup"><span data-stu-id="332b6-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="332b6-138">Aralık için "80-85".</span><span class="sxs-lookup"><span data-stu-id="332b6-138">"80-85" for range.</span></span>
<span data-ttu-id="332b6-139">birden çok girdi için "80; 443;".</span><span class="sxs-lookup"><span data-stu-id="332b6-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="332b6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="332b6-140">CommonParameters</span></span>
<span data-ttu-id="332b6-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="332b6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="332b6-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="332b6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="332b6-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="332b6-143">INPUTS</span></span>

### <span data-ttu-id="332b6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="332b6-144">System.String</span></span>

## <span data-ttu-id="332b6-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="332b6-145">OUTPUTS</span></span>

### <span data-ttu-id="332b6-146">Microsoft. Azure. Commands. Network. model. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="332b6-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="332b6-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="332b6-147">NOTES</span></span>
<span data-ttu-id="332b6-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, paket, yakalama, trafik, filtre</span><span class="sxs-lookup"><span data-stu-id="332b6-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="332b6-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="332b6-149">RELATED LINKS</span></span>

[<span data-ttu-id="332b6-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="332b6-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="332b6-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="332b6-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="332b6-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="332b6-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="332b6-153">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="332b6-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="332b6-154">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="332b6-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="332b6-155">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="332b6-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="332b6-156">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="332b6-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="332b6-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="332b6-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="332b6-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="332b6-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="332b6-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="332b6-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="332b6-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="332b6-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="332b6-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="332b6-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
