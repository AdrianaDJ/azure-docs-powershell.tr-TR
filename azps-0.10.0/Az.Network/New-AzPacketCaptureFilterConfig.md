---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 77a760fd78b06d4f04d5a805b689139977433f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935367"
---
# <span data-ttu-id="d6913-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d6913-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="d6913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6913-102">SYNOPSIS</span></span>
<span data-ttu-id="d6913-103">Yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6913-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="d6913-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6913-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6913-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6913-105">DESCRIPTION</span></span>
<span data-ttu-id="d6913-106">New-AzPacketCaptureFilterConfig cmdlet 'i yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d6913-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="d6913-107">Bu nesne, belirtilen ölçütleri kullanarak paket yakalama oturumu sırasında yakalanan paketlerin türünü sınırlandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d6913-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="d6913-108">New-AzNetworkWatcherPacketCapture cmdlet, birleştirilebilir yakalama oturumlarını etkinleştirmek için birden çok filtre nesnesi kabul edebilir.</span><span class="sxs-lookup"><span data-stu-id="d6913-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="d6913-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6913-109">EXAMPLES</span></span>

### <span data-ttu-id="d6913-110">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma------</span><span class="sxs-lookup"><span data-stu-id="d6913-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="d6913-111">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="d6913-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="d6913-112">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="d6913-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="d6913-113">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d6913-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="d6913-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6913-114">PARAMETERS</span></span>

### <span data-ttu-id="d6913-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6913-115">-DefaultProfile</span></span>
<span data-ttu-id="d6913-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d6913-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6913-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="d6913-117">-LocalIPAddress</span></span>
<span data-ttu-id="d6913-118">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6913-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="d6913-119">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="d6913-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d6913-120">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="d6913-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d6913-121">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="d6913-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="d6913-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="d6913-122">-LocalPort</span></span>
<span data-ttu-id="d6913-123">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6913-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="d6913-124">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="d6913-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d6913-125">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="d6913-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d6913-126">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="d6913-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="d6913-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d6913-127">-Protocol</span></span>
<span data-ttu-id="d6913-128">Filtre uygulanacak procotol belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6913-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="d6913-129">Kabul edilebilir değerler "TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="d6913-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="d6913-130">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="d6913-130">-RemoteIPAddress</span></span>
<span data-ttu-id="d6913-131">Filtre uygulanacak uzak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6913-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="d6913-132">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="d6913-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="d6913-133">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="d6913-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="d6913-134">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="d6913-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="d6913-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="d6913-135">-RemotePort</span></span>
<span data-ttu-id="d6913-136">Filtre uygulanacak uzak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d6913-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="d6913-137">Uzak bağlantı noktası örnek girişleri: tek çıkışlı girdi için "80".</span><span class="sxs-lookup"><span data-stu-id="d6913-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="d6913-138">Aralık için "80-85".</span><span class="sxs-lookup"><span data-stu-id="d6913-138">"80-85" for range.</span></span>
<span data-ttu-id="d6913-139">birden çok girdi için "80; 443;".</span><span class="sxs-lookup"><span data-stu-id="d6913-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="d6913-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6913-140">CommonParameters</span></span>
<span data-ttu-id="d6913-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6913-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6913-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6913-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6913-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6913-143">INPUTS</span></span>

### <span data-ttu-id="d6913-144">System. String</span><span class="sxs-lookup"><span data-stu-id="d6913-144">System.String</span></span>

## <span data-ttu-id="d6913-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6913-145">OUTPUTS</span></span>

### <span data-ttu-id="d6913-146">Microsoft. Azure. Commands. Network. model. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="d6913-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="d6913-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6913-147">NOTES</span></span>
<span data-ttu-id="d6913-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, paket, yakalama, trafik, filtre</span><span class="sxs-lookup"><span data-stu-id="d6913-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="d6913-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6913-149">RELATED LINKS</span></span>

[<span data-ttu-id="d6913-150">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6913-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6913-151">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6913-151">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6913-152">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6913-152">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6913-153">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6913-153">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6913-154">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="d6913-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d6913-155">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d6913-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d6913-156">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d6913-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d6913-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d6913-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d6913-158">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d6913-158">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d6913-159">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d6913-159">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d6913-160">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d6913-160">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d6913-161">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d6913-161">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
