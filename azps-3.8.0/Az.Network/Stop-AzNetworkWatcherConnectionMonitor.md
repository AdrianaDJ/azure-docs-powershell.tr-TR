---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 8840fc454601880fd2d4ed8bf7b816f7f3d83e5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098265"
---
# <span data-ttu-id="1cb47-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1cb47-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="1cb47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb47-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb47-103">Bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="1cb47-103">Stop a connection monitor</span></span>

## <span data-ttu-id="1cb47-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1cb47-104">SYNTAX</span></span>

### <span data-ttu-id="1cb47-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1cb47-105">SetByName (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb47-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1cb47-106">SetByResource</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb47-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1cb47-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb47-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="1cb47-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cb47-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1cb47-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb47-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cb47-110">DESCRIPTION</span></span>
<span data-ttu-id="1cb47-111">Stop-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini durdurur.</span><span class="sxs-lookup"><span data-stu-id="1cb47-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="1cb47-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1cb47-112">EXAMPLES</span></span>

### <span data-ttu-id="1cb47-113">Örnek 1: bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="1cb47-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="1cb47-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini durdurmamız</span><span class="sxs-lookup"><span data-stu-id="1cb47-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="1cb47-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1cb47-115">PARAMETERS</span></span>

### <span data-ttu-id="1cb47-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="1cb47-116">-AsJob</span></span>
<span data-ttu-id="1cb47-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1cb47-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cb47-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb47-118">-DefaultProfile</span></span>
<span data-ttu-id="1cb47-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1cb47-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cb47-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cb47-120">-InputObject</span></span>
<span data-ttu-id="1cb47-121">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1cb47-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb47-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="1cb47-122">-Location</span></span>
<span data-ttu-id="1cb47-123">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="1cb47-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1cb47-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1cb47-124">-Name</span></span>
<span data-ttu-id="1cb47-125">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="1cb47-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb47-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1cb47-126">-NetworkWatcher</span></span>
<span data-ttu-id="1cb47-127">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="1cb47-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="1cb47-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1cb47-128">-NetworkWatcherName</span></span>
<span data-ttu-id="1cb47-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="1cb47-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb47-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1cb47-130">-PassThru</span></span>
<span data-ttu-id="1cb47-131">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="1cb47-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="1cb47-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb47-132">-ResourceGroupName</span></span>
<span data-ttu-id="1cb47-133">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1cb47-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb47-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1cb47-134">-ResourceId</span></span>
<span data-ttu-id="1cb47-135">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1cb47-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb47-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="1cb47-136">-Confirm</span></span>
<span data-ttu-id="1cb47-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1cb47-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb47-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb47-138">-WhatIf</span></span>
<span data-ttu-id="1cb47-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1cb47-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb47-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1cb47-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb47-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb47-141">CommonParameters</span></span>
<span data-ttu-id="1cb47-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1cb47-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb47-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cb47-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb47-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1cb47-144">INPUTS</span></span>

### <span data-ttu-id="1cb47-145">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1cb47-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1cb47-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1cb47-146">System.String</span></span>

### <span data-ttu-id="1cb47-147">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="1cb47-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="1cb47-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1cb47-148">OUTPUTS</span></span>

### <span data-ttu-id="1cb47-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1cb47-149">System.Boolean</span></span>

## <span data-ttu-id="1cb47-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1cb47-150">NOTES</span></span>
<span data-ttu-id="1cb47-151">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="1cb47-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="1cb47-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1cb47-152">RELATED LINKS</span></span>

[<span data-ttu-id="1cb47-153">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="1cb47-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1cb47-154">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1cb47-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1cb47-155">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1cb47-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1cb47-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1cb47-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1cb47-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1cb47-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1cb47-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1cb47-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1cb47-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1cb47-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1cb47-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1cb47-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1cb47-161">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1cb47-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1cb47-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1cb47-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1cb47-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1cb47-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1cb47-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1cb47-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1cb47-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1cb47-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1cb47-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1cb47-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1cb47-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1cb47-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1cb47-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1cb47-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1cb47-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1cb47-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1cb47-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1cb47-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1cb47-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1cb47-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1cb47-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1cb47-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1cb47-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1cb47-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1cb47-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1cb47-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1cb47-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1cb47-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1cb47-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1cb47-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1cb47-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1cb47-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1cb47-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1cb47-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1cb47-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1cb47-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
