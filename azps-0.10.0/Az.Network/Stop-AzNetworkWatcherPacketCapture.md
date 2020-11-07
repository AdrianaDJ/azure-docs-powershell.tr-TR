---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936480"
---
# <span data-ttu-id="5a060-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5a060-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="5a060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a060-102">SYNOPSIS</span></span>
<span data-ttu-id="5a060-103">Çalışan bir paket yakalama oturumunu durdurur</span><span class="sxs-lookup"><span data-stu-id="5a060-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="5a060-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a060-104">SYNTAX</span></span>

### <span data-ttu-id="5a060-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a060-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a060-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5a060-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a060-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a060-107">DESCRIPTION</span></span>
<span data-ttu-id="5a060-108">Stop-AzNetworkWatcherPacketCapture çalışan paket yakalama oturumu durdurulur.</span><span class="sxs-lookup"><span data-stu-id="5a060-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="5a060-109">Oturum durdurulduktan sonra, paket yakalama dosyası, yapılandırmasına bağlı olarak yerel olarak depoya yüklenir ve/veya yerel olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="5a060-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="5a060-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a060-110">EXAMPLES</span></span>

### <span data-ttu-id="5a060-111">---Örnek 1: paket yakalama oturumunu durdurma---</span><span class="sxs-lookup"><span data-stu-id="5a060-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="5a060-112">Bu örnekte, "PacketCaptureTest" adlı çalışan bir paket yakalama oturumu dururız.</span><span class="sxs-lookup"><span data-stu-id="5a060-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="5a060-113">Oturum durdurulduktan sonra, paket yakalama dosyası, yapılandırmasına bağlı olarak yerel olarak depoya yüklenir ve/veya yerel olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="5a060-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="5a060-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a060-114">PARAMETERS</span></span>

### <span data-ttu-id="5a060-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="5a060-115">-AsJob</span></span>
<span data-ttu-id="5a060-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5a060-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a060-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a060-117">-DefaultProfile</span></span>
<span data-ttu-id="5a060-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a060-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a060-119">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="5a060-119">-NetworkWatcher</span></span>
<span data-ttu-id="5a060-120">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="5a060-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="5a060-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5a060-121">-NetworkWatcherName</span></span>
<span data-ttu-id="5a060-122">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="5a060-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="5a060-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="5a060-123">-PacketCaptureName</span></span>
<span data-ttu-id="5a060-124">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="5a060-124">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a060-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5a060-125">-PassThru</span></span>
<span data-ttu-id="5a060-126">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="5a060-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5a060-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a060-127">-ResourceGroupName</span></span>
<span data-ttu-id="5a060-128">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5a060-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5a060-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a060-129">-Confirm</span></span>
<span data-ttu-id="5a060-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a060-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a060-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a060-131">-WhatIf</span></span>
<span data-ttu-id="5a060-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a060-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a060-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a060-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a060-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a060-134">CommonParameters</span></span>
<span data-ttu-id="5a060-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a060-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a060-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a060-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a060-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a060-137">INPUTS</span></span>

### <span data-ttu-id="5a060-138">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="5a060-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5a060-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5a060-139">System.String</span></span>

## <span data-ttu-id="5a060-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a060-140">OUTPUTS</span></span>

### <span data-ttu-id="5a060-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a060-141">System.Boolean</span></span>

## <span data-ttu-id="5a060-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a060-142">NOTES</span></span>
<span data-ttu-id="5a060-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="5a060-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="5a060-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a060-144">RELATED LINKS</span></span>

[<span data-ttu-id="5a060-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5a060-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5a060-146">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5a060-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5a060-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5a060-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5a060-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5a060-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5a060-149">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="5a060-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5a060-150">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="5a060-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5a060-151">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="5a060-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5a060-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5a060-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5a060-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5a060-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5a060-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5a060-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5a060-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5a060-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5a060-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5a060-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
