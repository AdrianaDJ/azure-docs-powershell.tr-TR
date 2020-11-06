---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: ad6d2baaccdc17ec6ca414ae4b0cee84db20c94b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589255"
---
# <span data-ttu-id="b03a9-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b03a9-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="b03a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b03a9-102">SYNOPSIS</span></span>
<span data-ttu-id="b03a9-103">Yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b03a9-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b03a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b03a9-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b03a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b03a9-105">DESCRIPTION</span></span>
<span data-ttu-id="b03a9-106">New-AzureRmPacketCaptureFilterConfig cmdlet 'i yeni bir paket yakalama filtresi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b03a9-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="b03a9-107">Bu nesne, belirtilen ölçütleri kullanarak paket yakalama oturumu sırasında yakalanan paketlerin türünü sınırlandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b03a9-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="b03a9-108">New-AzureRmNetworkWatcherPacketCapture cmdlet, birleştirilebilir yakalama oturumlarını etkinleştirmek için birden çok filtre nesnesi kabul edebilir.</span><span class="sxs-lookup"><span data-stu-id="b03a9-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="b03a9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b03a9-109">EXAMPLES</span></span>

### <span data-ttu-id="b03a9-110">Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma------</span><span class="sxs-lookup"><span data-stu-id="b03a9-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="b03a9-111">Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="b03a9-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="b03a9-112">Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="b03a9-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="b03a9-113">Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b03a9-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="b03a9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b03a9-114">PARAMETERS</span></span>

### <span data-ttu-id="b03a9-115">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="b03a9-115">-LocalIPAddress</span></span>
<span data-ttu-id="b03a9-116">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b03a9-116">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="b03a9-117">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="b03a9-117">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="b03a9-118">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="b03a9-118">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="b03a9-119">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="b03a9-119">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="b03a9-120">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="b03a9-120">-LocalPort</span></span>
<span data-ttu-id="b03a9-121">Filtre uygulanacak yerel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b03a9-121">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="b03a9-122">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="b03a9-122">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="b03a9-123">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="b03a9-123">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="b03a9-124">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="b03a9-124">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="b03a9-125">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="b03a9-125">-Protocol</span></span>
<span data-ttu-id="b03a9-126">Filtre uygulanacak procotol belirtir.</span><span class="sxs-lookup"><span data-stu-id="b03a9-126">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="b03a9-127">Kabul edilebilir değerler "TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="b03a9-127">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b03a9-128">-Remoteıpaddress</span><span class="sxs-lookup"><span data-stu-id="b03a9-128">-RemoteIPAddress</span></span>
<span data-ttu-id="b03a9-129">Filtre uygulanacak uzak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b03a9-129">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="b03a9-130">Örnek girişler: tek bir adres girişi için "127.0.0.1".</span><span class="sxs-lookup"><span data-stu-id="b03a9-130">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="b03a9-131">Aralık için "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="b03a9-131">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="b03a9-132">birden çok girdi için "127.0.0.1; 127.0.0.5;".</span><span class="sxs-lookup"><span data-stu-id="b03a9-132">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="b03a9-133">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="b03a9-133">-RemotePort</span></span>
<span data-ttu-id="b03a9-134">Filtre uygulanacak uzak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b03a9-134">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="b03a9-135">Uzak bağlantı noktası örnek girişleri: tek çıkışlı girdi için "80".</span><span class="sxs-lookup"><span data-stu-id="b03a9-135">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="b03a9-136">Aralık için "80-85".</span><span class="sxs-lookup"><span data-stu-id="b03a9-136">"80-85" for range.</span></span>
<span data-ttu-id="b03a9-137">birden çok girdi için "80; 443;".</span><span class="sxs-lookup"><span data-stu-id="b03a9-137">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="b03a9-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b03a9-138">-DefaultProfile</span></span>
<span data-ttu-id="b03a9-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b03a9-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b03a9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b03a9-140">CommonParameters</span></span>
<span data-ttu-id="b03a9-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b03a9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b03a9-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b03a9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b03a9-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b03a9-143">INPUTS</span></span>

### <span data-ttu-id="b03a9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b03a9-144">System.String</span></span>

## <span data-ttu-id="b03a9-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b03a9-145">OUTPUTS</span></span>

### <span data-ttu-id="b03a9-146">Microsoft. Azure. Commands. Network. model. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="b03a9-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="b03a9-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b03a9-147">NOTES</span></span>
<span data-ttu-id="b03a9-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, paket, yakalama, trafik, filtre</span><span class="sxs-lookup"><span data-stu-id="b03a9-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="b03a9-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b03a9-149">RELATED LINKS</span></span>

[<span data-ttu-id="b03a9-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b03a9-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b03a9-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b03a9-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b03a9-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b03a9-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b03a9-153">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b03a9-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b03a9-154">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b03a9-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b03a9-155">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b03a9-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b03a9-156">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b03a9-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b03a9-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b03a9-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b03a9-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b03a9-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b03a9-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b03a9-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b03a9-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b03a9-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b03a9-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b03a9-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
