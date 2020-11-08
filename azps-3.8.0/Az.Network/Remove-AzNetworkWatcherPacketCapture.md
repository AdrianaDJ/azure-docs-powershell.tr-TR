---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 6002f420e0e4d1c3a0a61c8524ec6b2022075b52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104066"
---
# <span data-ttu-id="92c71-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="92c71-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="92c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92c71-102">SYNOPSIS</span></span>
<span data-ttu-id="92c71-103">Paket yakalama kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="92c71-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="92c71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92c71-104">SYNTAX</span></span>

### <span data-ttu-id="92c71-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="92c71-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92c71-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="92c71-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92c71-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="92c71-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92c71-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="92c71-108">DESCRIPTION</span></span>
<span data-ttu-id="92c71-109">Remove-AzNetworkWatcherPacketCapture paket yakalama kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="92c71-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="92c71-110">Remove-AzNetworkWatcherPacketCapture ' i çağırmadan önce Stop-AzNetworkWatcherPacketCapture çağrı yapmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="92c71-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="92c71-111">Remove-AzNetworkWatcherPacketCapture çağrıldığında paket yakalama oturumu çalışıyorsa, paket yakalama kaydedilmez.</span><span class="sxs-lookup"><span data-stu-id="92c71-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="92c71-112">Oturum kaldırılmadan önce durdurulmuşsa, yakalama verilerini içeren. cap dosyası kaldırılmaz.</span><span class="sxs-lookup"><span data-stu-id="92c71-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="92c71-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92c71-113">EXAMPLES</span></span>

### <span data-ttu-id="92c71-114">Örnek 1: paket yakalama oturumunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="92c71-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="92c71-115">Bu örnekte, "PacketCaptureTest" adlı bir paket yakalama oturumu kaldırdık.</span><span class="sxs-lookup"><span data-stu-id="92c71-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="92c71-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92c71-116">PARAMETERS</span></span>

### <span data-ttu-id="92c71-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="92c71-117">-AsJob</span></span>
<span data-ttu-id="92c71-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="92c71-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92c71-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92c71-119">-DefaultProfile</span></span>
<span data-ttu-id="92c71-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92c71-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92c71-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="92c71-121">-Location</span></span>
<span data-ttu-id="92c71-122">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="92c71-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="92c71-123">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="92c71-123">-NetworkWatcher</span></span>
<span data-ttu-id="92c71-124">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="92c71-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="92c71-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="92c71-125">-NetworkWatcherName</span></span>
<span data-ttu-id="92c71-126">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="92c71-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="92c71-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="92c71-127">-PacketCaptureName</span></span>
<span data-ttu-id="92c71-128">Paket yakalama adı.</span><span class="sxs-lookup"><span data-stu-id="92c71-128">The packet capture name.</span></span>

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

### <span data-ttu-id="92c71-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="92c71-129">-PassThru</span></span>
<span data-ttu-id="92c71-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="92c71-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="92c71-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92c71-131">-ResourceGroupName</span></span>
<span data-ttu-id="92c71-132">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="92c71-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="92c71-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="92c71-133">-Confirm</span></span>
<span data-ttu-id="92c71-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92c71-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92c71-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92c71-135">-WhatIf</span></span>
<span data-ttu-id="92c71-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92c71-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92c71-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92c71-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92c71-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c71-138">CommonParameters</span></span>
<span data-ttu-id="92c71-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92c71-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c71-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92c71-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c71-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92c71-141">INPUTS</span></span>

### <span data-ttu-id="92c71-142">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="92c71-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="92c71-143">System. String</span><span class="sxs-lookup"><span data-stu-id="92c71-143">System.String</span></span>

## <span data-ttu-id="92c71-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92c71-144">OUTPUTS</span></span>

### <span data-ttu-id="92c71-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92c71-145">System.Boolean</span></span>

## <span data-ttu-id="92c71-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92c71-146">NOTES</span></span>
<span data-ttu-id="92c71-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik, kaldır</span><span class="sxs-lookup"><span data-stu-id="92c71-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="92c71-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92c71-148">RELATED LINKS</span></span>

[<span data-ttu-id="92c71-149">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="92c71-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="92c71-150">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="92c71-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="92c71-151">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="92c71-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="92c71-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="92c71-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="92c71-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="92c71-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="92c71-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="92c71-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="92c71-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="92c71-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="92c71-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="92c71-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="92c71-157">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="92c71-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="92c71-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="92c71-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="92c71-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="92c71-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="92c71-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="92c71-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="92c71-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="92c71-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="92c71-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="92c71-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="92c71-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="92c71-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="92c71-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92c71-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92c71-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92c71-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92c71-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92c71-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92c71-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="92c71-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="92c71-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92c71-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92c71-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92c71-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="92c71-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="92c71-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="92c71-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="92c71-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="92c71-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="92c71-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="92c71-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="92c71-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="92c71-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="92c71-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="92c71-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="92c71-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
