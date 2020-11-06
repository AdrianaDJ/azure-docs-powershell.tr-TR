---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 7f9417fe4ad6e115e73502e953dfcab965ccd17b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587837"
---
# <span data-ttu-id="f17fe-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f17fe-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="f17fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f17fe-102">SYNOPSIS</span></span>
<span data-ttu-id="f17fe-103">Paket yakalama kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f17fe-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f17fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f17fe-104">SYNTAX</span></span>

### <span data-ttu-id="f17fe-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f17fe-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17fe-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f17fe-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f17fe-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f17fe-107">DESCRIPTION</span></span>
<span data-ttu-id="f17fe-108">Remove-AzureRmNetworkWatcherPacketCapture paket yakalama kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f17fe-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="f17fe-109">Remove-AzureRmNetworkWatcherPacketCapture ' i çağırmadan önce Stop-AzureRmNetworkWatcherPacketCapture çağrı yapmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="f17fe-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="f17fe-110">Remove-AzureRmNetworkWatcherPacketCapture çağrıldığında paket yakalama oturumu çalışıyorsa, paket yakalama kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="f17fe-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="f17fe-111">Oturum kaldırılmadan önce durdurulmuşsa, yakalama verilerini içeren. cap dosyası kaldırılmaz.</span><span class="sxs-lookup"><span data-stu-id="f17fe-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="f17fe-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f17fe-112">EXAMPLES</span></span>

### <span data-ttu-id="f17fe-113">Örnek 1: paket yakalama oturumunu kaldırma-----</span><span class="sxs-lookup"><span data-stu-id="f17fe-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="f17fe-114">Bu örnekte, "PacketCaptureTest" adlı bir paket yakalama oturumu kaldırdık.</span><span class="sxs-lookup"><span data-stu-id="f17fe-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="f17fe-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f17fe-115">PARAMETERS</span></span>

### <span data-ttu-id="f17fe-116">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f17fe-116">-NetworkWatcher</span></span>
<span data-ttu-id="f17fe-117">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="f17fe-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="f17fe-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f17fe-118">-NetworkWatcherName</span></span>
<span data-ttu-id="f17fe-119">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="f17fe-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="f17fe-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="f17fe-120">-PacketCaptureName</span></span>
<span data-ttu-id="f17fe-121">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="f17fe-121">The packet capture name.</span></span>

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

### <span data-ttu-id="f17fe-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f17fe-122">-PassThru</span></span>
<span data-ttu-id="f17fe-123">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f17fe-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f17fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f17fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="f17fe-125">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f17fe-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f17fe-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="f17fe-126">-Confirm</span></span>
<span data-ttu-id="f17fe-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f17fe-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f17fe-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f17fe-128">-WhatIf</span></span>
<span data-ttu-id="f17fe-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f17fe-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f17fe-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f17fe-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f17fe-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17fe-131">-DefaultProfile</span></span>
<span data-ttu-id="f17fe-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f17fe-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f17fe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17fe-133">CommonParameters</span></span>
<span data-ttu-id="f17fe-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f17fe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17fe-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f17fe-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17fe-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f17fe-136">INPUTS</span></span>

### <span data-ttu-id="f17fe-137">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f17fe-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f17fe-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f17fe-138">System.String</span></span>

## <span data-ttu-id="f17fe-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f17fe-139">OUTPUTS</span></span>

### <span data-ttu-id="f17fe-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="f17fe-140">System.Object</span></span>

## <span data-ttu-id="f17fe-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f17fe-141">NOTES</span></span>
<span data-ttu-id="f17fe-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik, kaldır</span><span class="sxs-lookup"><span data-stu-id="f17fe-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="f17fe-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f17fe-143">RELATED LINKS</span></span>

[<span data-ttu-id="f17fe-144">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f17fe-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f17fe-145">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f17fe-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f17fe-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f17fe-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f17fe-147">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f17fe-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f17fe-148">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f17fe-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f17fe-149">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f17fe-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f17fe-150">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="f17fe-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f17fe-151">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f17fe-151">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f17fe-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f17fe-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="f17fe-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f17fe-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f17fe-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f17fe-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f17fe-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f17fe-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
