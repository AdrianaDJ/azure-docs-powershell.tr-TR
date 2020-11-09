---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 922026b14531cc1c65f60901914383b402d06889
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325690"
---
# <span data-ttu-id="86573-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86573-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="86573-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86573-102">SYNOPSIS</span></span>
<span data-ttu-id="86573-103">Çalışan bir paket yakalama oturumunu durdurur</span><span class="sxs-lookup"><span data-stu-id="86573-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="86573-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86573-104">SYNTAX</span></span>

### <span data-ttu-id="86573-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="86573-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86573-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="86573-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86573-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="86573-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86573-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="86573-108">DESCRIPTION</span></span>
<span data-ttu-id="86573-109">Stop-AzNetworkWatcherPacketCapture çalışan paket yakalama oturumu durdurulur.</span><span class="sxs-lookup"><span data-stu-id="86573-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="86573-110">Oturum durdurulduktan sonra, paket yakalama dosyası, yapılandırmasına bağlı olarak yerel olarak depoya yüklenir ve/veya yerel olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="86573-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="86573-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86573-111">EXAMPLES</span></span>

### <span data-ttu-id="86573-112">Örnek 1: paket yakalama oturumunu durdurma</span><span class="sxs-lookup"><span data-stu-id="86573-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="86573-113">Bu örnekte, "PacketCaptureTest" adlı çalışan bir paket yakalama oturumu dururız.</span><span class="sxs-lookup"><span data-stu-id="86573-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="86573-114">Oturum durdurulduktan sonra, paket yakalama dosyası, yapılandırmasına bağlı olarak yerel olarak depoya yüklenir ve/veya yerel olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="86573-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="86573-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86573-115">PARAMETERS</span></span>

### <span data-ttu-id="86573-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="86573-116">-AsJob</span></span>
<span data-ttu-id="86573-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="86573-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86573-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86573-118">-DefaultProfile</span></span>
<span data-ttu-id="86573-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="86573-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86573-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="86573-120">-Location</span></span>
<span data-ttu-id="86573-121">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="86573-121">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86573-122">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="86573-122">-NetworkWatcher</span></span>
<span data-ttu-id="86573-123">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="86573-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="86573-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="86573-124">-NetworkWatcherName</span></span>
<span data-ttu-id="86573-125">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="86573-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="86573-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="86573-126">-PacketCaptureName</span></span>
<span data-ttu-id="86573-127">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="86573-127">The packet capture name.</span></span>

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

### <span data-ttu-id="86573-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="86573-128">-PassThru</span></span>
<span data-ttu-id="86573-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="86573-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="86573-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86573-130">-ResourceGroupName</span></span>
<span data-ttu-id="86573-131">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="86573-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="86573-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="86573-132">-Confirm</span></span>
<span data-ttu-id="86573-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="86573-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86573-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86573-134">-WhatIf</span></span>
<span data-ttu-id="86573-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86573-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86573-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="86573-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86573-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86573-137">CommonParameters</span></span>
<span data-ttu-id="86573-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86573-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86573-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86573-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86573-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86573-140">INPUTS</span></span>

### <span data-ttu-id="86573-141">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="86573-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="86573-142">System. String</span><span class="sxs-lookup"><span data-stu-id="86573-142">System.String</span></span>

## <span data-ttu-id="86573-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86573-143">OUTPUTS</span></span>

### <span data-ttu-id="86573-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86573-144">System.Boolean</span></span>

## <span data-ttu-id="86573-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86573-145">NOTES</span></span>
<span data-ttu-id="86573-146">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik</span><span class="sxs-lookup"><span data-stu-id="86573-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="86573-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86573-147">RELATED LINKS</span></span>

[<span data-ttu-id="86573-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86573-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86573-149">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="86573-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="86573-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86573-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86573-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86573-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86573-152">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="86573-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="86573-153">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="86573-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="86573-154">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="86573-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="86573-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="86573-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="86573-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="86573-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="86573-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86573-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="86573-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="86573-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="86573-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="86573-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="86573-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="86573-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="86573-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86573-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86573-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="86573-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="86573-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="86573-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="86573-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86573-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86573-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86573-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86573-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86573-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86573-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="86573-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="86573-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86573-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86573-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86573-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86573-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="86573-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="86573-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="86573-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="86573-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="86573-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="86573-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="86573-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="86573-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86573-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
