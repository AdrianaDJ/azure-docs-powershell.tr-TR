---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936619"
---
# <span data-ttu-id="09ec5-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09ec5-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="09ec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="09ec5-103">Paket yakalama kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="09ec5-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="09ec5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09ec5-104">SYNTAX</span></span>

### <span data-ttu-id="09ec5-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="09ec5-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09ec5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="09ec5-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09ec5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="09ec5-107">DESCRIPTION</span></span>
<span data-ttu-id="09ec5-108">Remove-AzNetworkWatcherPacketCapture paket yakalama kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="09ec5-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="09ec5-109">Remove-AzNetworkWatcherPacketCapture ' i çağırmadan önce Stop-AzNetworkWatcherPacketCapture çağrı yapmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="09ec5-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="09ec5-110">Remove-AzNetworkWatcherPacketCapture çağrıldığında paket yakalama oturumu çalışıyorsa, paket yakalama kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="09ec5-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="09ec5-111">Oturum kaldırılmadan önce durdurulmuşsa, yakalama verilerini içeren. cap dosyası kaldırılmaz.</span><span class="sxs-lookup"><span data-stu-id="09ec5-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="09ec5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09ec5-112">EXAMPLES</span></span>

### <span data-ttu-id="09ec5-113">Örnek 1: paket yakalama oturumunu kaldırma-----</span><span class="sxs-lookup"><span data-stu-id="09ec5-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="09ec5-114">Bu örnekte, "PacketCaptureTest" adlı bir paket yakalama oturumu kaldırdık.</span><span class="sxs-lookup"><span data-stu-id="09ec5-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="09ec5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09ec5-115">PARAMETERS</span></span>

### <span data-ttu-id="09ec5-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="09ec5-116">-AsJob</span></span>
<span data-ttu-id="09ec5-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="09ec5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09ec5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09ec5-118">-DefaultProfile</span></span>
<span data-ttu-id="09ec5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09ec5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09ec5-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="09ec5-120">-NetworkWatcher</span></span>
<span data-ttu-id="09ec5-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="09ec5-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="09ec5-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="09ec5-122">-NetworkWatcherName</span></span>
<span data-ttu-id="09ec5-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="09ec5-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="09ec5-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="09ec5-124">-PacketCaptureName</span></span>
<span data-ttu-id="09ec5-125">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="09ec5-125">The packet capture name.</span></span>

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

### <span data-ttu-id="09ec5-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="09ec5-126">-PassThru</span></span>
<span data-ttu-id="09ec5-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="09ec5-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09ec5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09ec5-128">-ResourceGroupName</span></span>
<span data-ttu-id="09ec5-129">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="09ec5-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="09ec5-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="09ec5-130">-Confirm</span></span>
<span data-ttu-id="09ec5-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="09ec5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09ec5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09ec5-132">-WhatIf</span></span>
<span data-ttu-id="09ec5-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="09ec5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09ec5-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="09ec5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09ec5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09ec5-135">CommonParameters</span></span>
<span data-ttu-id="09ec5-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09ec5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09ec5-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09ec5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09ec5-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09ec5-138">INPUTS</span></span>

### <span data-ttu-id="09ec5-139">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="09ec5-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="09ec5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="09ec5-140">System.String</span></span>

## <span data-ttu-id="09ec5-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09ec5-141">OUTPUTS</span></span>

### <span data-ttu-id="09ec5-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="09ec5-142">System.Object</span></span>

## <span data-ttu-id="09ec5-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09ec5-143">NOTES</span></span>
<span data-ttu-id="09ec5-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik, kaldır</span><span class="sxs-lookup"><span data-stu-id="09ec5-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="09ec5-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09ec5-145">RELATED LINKS</span></span>

[<span data-ttu-id="09ec5-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09ec5-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="09ec5-147">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="09ec5-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="09ec5-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09ec5-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="09ec5-149">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="09ec5-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="09ec5-150">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="09ec5-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="09ec5-151">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="09ec5-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="09ec5-152">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="09ec5-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="09ec5-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="09ec5-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="09ec5-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="09ec5-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="09ec5-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="09ec5-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="09ec5-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="09ec5-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="09ec5-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="09ec5-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
