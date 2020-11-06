---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 034cca094bf6dd7d3911e3e705e03888f0ea10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593732"
---
# <span data-ttu-id="0d511-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d511-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="0d511-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d511-102">SYNOPSIS</span></span>
<span data-ttu-id="0d511-103">Paket yakalama kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d511-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d511-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d511-104">SYNTAX</span></span>

### <span data-ttu-id="0d511-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d511-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d511-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0d511-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d511-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d511-107">DESCRIPTION</span></span>
<span data-ttu-id="0d511-108">Remove-AzureRmNetworkWatcherPacketCapture paket yakalama kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d511-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="0d511-109">Remove-AzureRmNetworkWatcherPacketCapture ' i çağırmadan önce Stop-AzureRmNetworkWatcherPacketCapture çağrı yapmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="0d511-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="0d511-110">Remove-AzureRmNetworkWatcherPacketCapture çağrıldığında paket yakalama oturumu çalışıyorsa, paket yakalama kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="0d511-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="0d511-111">Oturum kaldırılmadan önce durdurulmuşsa, yakalama verilerini içeren. cap dosyası kaldırılmaz.</span><span class="sxs-lookup"><span data-stu-id="0d511-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="0d511-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d511-112">EXAMPLES</span></span>

### <span data-ttu-id="0d511-113">Örnek 1: paket yakalama oturumunu kaldırma-----</span><span class="sxs-lookup"><span data-stu-id="0d511-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="0d511-114">Bu örnekte, "PacketCaptureTest" adlı bir paket yakalama oturumu kaldırdık.</span><span class="sxs-lookup"><span data-stu-id="0d511-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="0d511-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d511-115">PARAMETERS</span></span>

### <span data-ttu-id="0d511-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="0d511-116">-AsJob</span></span>
<span data-ttu-id="0d511-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0d511-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d511-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d511-118">-DefaultProfile</span></span>
<span data-ttu-id="0d511-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d511-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d511-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d511-120">-NetworkWatcher</span></span>
<span data-ttu-id="0d511-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="0d511-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="0d511-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0d511-122">-NetworkWatcherName</span></span>
<span data-ttu-id="0d511-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="0d511-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="0d511-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="0d511-124">-PacketCaptureName</span></span>
<span data-ttu-id="0d511-125">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="0d511-125">The packet capture name.</span></span>

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

### <span data-ttu-id="0d511-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0d511-126">-PassThru</span></span>
<span data-ttu-id="0d511-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="0d511-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0d511-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d511-128">-ResourceGroupName</span></span>
<span data-ttu-id="0d511-129">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0d511-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0d511-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d511-130">-Confirm</span></span>
<span data-ttu-id="0d511-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d511-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d511-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d511-132">-WhatIf</span></span>
<span data-ttu-id="0d511-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d511-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d511-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d511-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d511-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d511-135">CommonParameters</span></span>
<span data-ttu-id="0d511-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d511-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d511-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d511-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d511-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d511-138">INPUTS</span></span>

### <span data-ttu-id="0d511-139">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d511-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0d511-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0d511-140">System.String</span></span>

## <span data-ttu-id="0d511-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d511-141">OUTPUTS</span></span>

### <span data-ttu-id="0d511-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="0d511-142">System.Object</span></span>

## <span data-ttu-id="0d511-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d511-143">NOTES</span></span>
<span data-ttu-id="0d511-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik, kaldır</span><span class="sxs-lookup"><span data-stu-id="0d511-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="0d511-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d511-145">RELATED LINKS</span></span>

[<span data-ttu-id="0d511-146">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d511-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d511-147">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0d511-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0d511-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d511-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d511-149">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d511-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d511-150">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d511-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d511-151">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d511-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d511-152">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="0d511-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d511-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0d511-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0d511-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0d511-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="0d511-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0d511-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0d511-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0d511-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0d511-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0d511-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
