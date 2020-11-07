---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 43dc48aaa58f086e6d05f45a81096612d3177a17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764417"
---
# <span data-ttu-id="efb39-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efb39-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="efb39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efb39-102">SYNOPSIS</span></span>
<span data-ttu-id="efb39-103">Çalışan bir paket yakalama oturumunu durdurur</span><span class="sxs-lookup"><span data-stu-id="efb39-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efb39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efb39-104">SYNTAX</span></span>

### <span data-ttu-id="efb39-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="efb39-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efb39-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="efb39-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efb39-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="efb39-107">DESCRIPTION</span></span>
<span data-ttu-id="efb39-108">Stop-AzureRmNetworkWatcherPacketCapture çalışan paket yakalama oturumu durdurulur.</span><span class="sxs-lookup"><span data-stu-id="efb39-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="efb39-109">Oturum durdurulduktan sonra, paket yakalama dosyası, yapılandırmasına bağlı olarak yerel olarak depoya yüklenir ve/veya yerel olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="efb39-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="efb39-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efb39-110">EXAMPLES</span></span>

### <span data-ttu-id="efb39-111">---Örnek 1: paket yakalama oturumunu durdurma---</span><span class="sxs-lookup"><span data-stu-id="efb39-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="efb39-112">Bu örnekte, "PacketCaptureTest" adlı çalışan bir paket yakalama oturumu dururız.</span><span class="sxs-lookup"><span data-stu-id="efb39-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="efb39-113">Oturum durdurulduktan sonra, paket yakalama dosyası, yapılandırmasına bağlı olarak yerel olarak depoya yüklenir ve/veya yerel olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="efb39-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="efb39-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efb39-114">PARAMETERS</span></span>

### <span data-ttu-id="efb39-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="efb39-115">-AsJob</span></span>
<span data-ttu-id="efb39-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="efb39-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="efb39-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb39-117">-DefaultProfile</span></span>
<span data-ttu-id="efb39-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="efb39-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efb39-119">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="efb39-119">-NetworkWatcher</span></span>
<span data-ttu-id="efb39-120">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="efb39-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="efb39-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="efb39-121">-NetworkWatcherName</span></span>
<span data-ttu-id="efb39-122">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="efb39-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="efb39-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="efb39-123">-PacketCaptureName</span></span>
<span data-ttu-id="efb39-124">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="efb39-124">The packet capture name.</span></span>

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

### <span data-ttu-id="efb39-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="efb39-125">-PassThru</span></span>
<span data-ttu-id="efb39-126">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="efb39-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="efb39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb39-127">-ResourceGroupName</span></span>
<span data-ttu-id="efb39-128">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="efb39-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="efb39-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="efb39-129">-Confirm</span></span>
<span data-ttu-id="efb39-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="efb39-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb39-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb39-131">-WhatIf</span></span>
<span data-ttu-id="efb39-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="efb39-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efb39-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="efb39-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb39-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb39-134">CommonParameters</span></span>
<span data-ttu-id="efb39-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efb39-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb39-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efb39-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb39-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efb39-137">INPUTS</span></span>

### <span data-ttu-id="efb39-138">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="efb39-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="efb39-139">System. String</span><span class="sxs-lookup"><span data-stu-id="efb39-139">System.String</span></span>

## <span data-ttu-id="efb39-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efb39-140">OUTPUTS</span></span>

### <span data-ttu-id="efb39-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="efb39-141">System.Boolean</span></span>

## <span data-ttu-id="efb39-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efb39-142">NOTES</span></span>
<span data-ttu-id="efb39-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="efb39-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="efb39-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efb39-144">RELATED LINKS</span></span>

[<span data-ttu-id="efb39-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efb39-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efb39-146">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="efb39-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="efb39-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efb39-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efb39-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="efb39-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="efb39-149">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="efb39-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="efb39-150">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="efb39-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="efb39-151">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="efb39-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="efb39-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="efb39-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="efb39-153">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="efb39-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="efb39-154">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="efb39-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="efb39-155">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="efb39-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="efb39-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="efb39-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
