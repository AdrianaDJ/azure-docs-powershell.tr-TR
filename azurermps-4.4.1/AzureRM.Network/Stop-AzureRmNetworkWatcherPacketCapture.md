---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 3f1206b79f8e80793106b1e294b591e21b9fb77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587826"
---
# <span data-ttu-id="c2c57-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2c57-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="c2c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2c57-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c57-103">Çalışan bir paket yakalama oturumunu durdurur</span><span class="sxs-lookup"><span data-stu-id="c2c57-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2c57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2c57-104">SYNTAX</span></span>

### <span data-ttu-id="c2c57-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2c57-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2c57-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c2c57-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2c57-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2c57-107">DESCRIPTION</span></span>
<span data-ttu-id="c2c57-108">Stop-AzureRmNetworkWatcherPacketCapture çalışan paket yakalama oturumu durdurulur.</span><span class="sxs-lookup"><span data-stu-id="c2c57-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="c2c57-109">Oturum durdurulduktan sonra, paket yakalama dosyası, yapılandırmasına bağlı olarak yerel olarak depoya yüklenir ve/veya yerel olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="c2c57-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="c2c57-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2c57-110">EXAMPLES</span></span>

### <span data-ttu-id="c2c57-111">---Örnek 1: paket yakalama oturumunu durdurma---</span><span class="sxs-lookup"><span data-stu-id="c2c57-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="c2c57-112">Bu örnekte, "PacketCaptureTest" adlı çalışan bir paket yakalama oturumu dururız.</span><span class="sxs-lookup"><span data-stu-id="c2c57-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="c2c57-113">Oturum durdurulduktan sonra, paket yakalama dosyası, yapılandırmasına bağlı olarak yerel olarak depoya yüklenir ve/veya yerel olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="c2c57-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="c2c57-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2c57-114">PARAMETERS</span></span>

### <span data-ttu-id="c2c57-115">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2c57-115">-NetworkWatcher</span></span>
<span data-ttu-id="c2c57-116">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="c2c57-116">The network watcher resource.</span></span>

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

### <span data-ttu-id="c2c57-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c2c57-117">-NetworkWatcherName</span></span>
<span data-ttu-id="c2c57-118">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="c2c57-118">The name of network watcher.</span></span>

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

### <span data-ttu-id="c2c57-119">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="c2c57-119">-PacketCaptureName</span></span>
<span data-ttu-id="c2c57-120">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="c2c57-120">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c57-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c2c57-121">-PassThru</span></span>
<span data-ttu-id="c2c57-122">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c2c57-122">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2c57-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c57-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2c57-124">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c2c57-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c2c57-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2c57-125">-Confirm</span></span>
<span data-ttu-id="c2c57-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2c57-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2c57-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2c57-127">-WhatIf</span></span>
<span data-ttu-id="c2c57-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2c57-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2c57-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2c57-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2c57-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c57-130">-DefaultProfile</span></span>
<span data-ttu-id="c2c57-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2c57-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2c57-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c57-132">CommonParameters</span></span>
<span data-ttu-id="c2c57-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2c57-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c57-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c57-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c57-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2c57-135">INPUTS</span></span>

### <span data-ttu-id="c2c57-136">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2c57-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c2c57-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c2c57-137">System.String</span></span>

## <span data-ttu-id="c2c57-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2c57-138">OUTPUTS</span></span>

### <span data-ttu-id="c2c57-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2c57-139">System.Boolean</span></span>

## <span data-ttu-id="c2c57-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2c57-140">NOTES</span></span>
<span data-ttu-id="c2c57-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="c2c57-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="c2c57-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2c57-142">RELATED LINKS</span></span>

[<span data-ttu-id="c2c57-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2c57-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2c57-144">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c2c57-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c2c57-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2c57-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2c57-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2c57-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2c57-147">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2c57-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c2c57-148">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2c57-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c2c57-149">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c2c57-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c2c57-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c2c57-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c2c57-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c2c57-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c2c57-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c2c57-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c2c57-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c2c57-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c2c57-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c2c57-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
