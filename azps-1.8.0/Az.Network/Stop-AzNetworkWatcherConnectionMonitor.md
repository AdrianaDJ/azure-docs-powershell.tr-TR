---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: ceb03c58c7f7c3983f89073b5bad2428a32b7934
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759939"
---
# <span data-ttu-id="8ec4d-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ec4d-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="8ec4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec4d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec4d-103">Bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="8ec4d-103">Stop a connection monitor</span></span>

## <span data-ttu-id="8ec4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ec4d-104">SYNTAX</span></span>

### <span data-ttu-id="8ec4d-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ec4d-105">SetByName (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ec4d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8ec4d-106">SetByResource</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ec4d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8ec4d-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ec4d-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="8ec4d-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ec4d-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ec4d-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec4d-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ec4d-110">DESCRIPTION</span></span>
<span data-ttu-id="8ec4d-111">Stop-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini durdurur.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="8ec4d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ec4d-112">EXAMPLES</span></span>

### <span data-ttu-id="8ec4d-113">Örnek 1: bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="8ec4d-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="8ec4d-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini durdurmamız</span><span class="sxs-lookup"><span data-stu-id="8ec4d-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="8ec4d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ec4d-115">PARAMETERS</span></span>

### <span data-ttu-id="8ec4d-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="8ec4d-116">-AsJob</span></span>
<span data-ttu-id="8ec4d-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8ec4d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ec4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec4d-118">-DefaultProfile</span></span>
<span data-ttu-id="8ec4d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ec4d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ec4d-120">-InputObject</span></span>
<span data-ttu-id="8ec4d-121">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="8ec4d-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="8ec4d-122">-Location</span></span>
<span data-ttu-id="8ec4d-123">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8ec4d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ec4d-124">-Name</span></span>
<span data-ttu-id="8ec4d-125">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="8ec4d-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8ec4d-126">-NetworkWatcher</span></span>
<span data-ttu-id="8ec4d-127">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="8ec4d-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8ec4d-128">-NetworkWatcherName</span></span>
<span data-ttu-id="8ec4d-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="8ec4d-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8ec4d-130">-PassThru</span></span>
<span data-ttu-id="8ec4d-131">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="8ec4d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec4d-132">-ResourceGroupName</span></span>
<span data-ttu-id="8ec4d-133">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8ec4d-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8ec4d-134">-ResourceId</span></span>
<span data-ttu-id="8ec4d-135">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-135">Resource ID.</span></span>

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

### <span data-ttu-id="8ec4d-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ec4d-136">-Confirm</span></span>
<span data-ttu-id="8ec4d-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec4d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec4d-138">-WhatIf</span></span>
<span data-ttu-id="8ec4d-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ec4d-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec4d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec4d-141">CommonParameters</span></span>
<span data-ttu-id="8ec4d-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ec4d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec4d-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec4d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec4d-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ec4d-144">INPUTS</span></span>

### <span data-ttu-id="8ec4d-145">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8ec4d-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8ec4d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8ec4d-146">System.String</span></span>

### <span data-ttu-id="8ec4d-147">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="8ec4d-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="8ec4d-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ec4d-148">OUTPUTS</span></span>

### <span data-ttu-id="8ec4d-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec4d-149">System.Boolean</span></span>

## <span data-ttu-id="8ec4d-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ec4d-150">NOTES</span></span>
<span data-ttu-id="8ec4d-151">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="8ec4d-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="8ec4d-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ec4d-152">RELATED LINKS</span></span>

[<span data-ttu-id="8ec4d-153">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="8ec4d-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8ec4d-154">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8ec4d-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8ec4d-155">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8ec4d-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8ec4d-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8ec4d-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8ec4d-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8ec4d-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8ec4d-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8ec4d-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8ec4d-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8ec4d-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8ec4d-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ec4d-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ec4d-161">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8ec4d-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8ec4d-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ec4d-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ec4d-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ec4d-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ec4d-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ec4d-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8ec4d-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ec4d-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ec4d-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8ec4d-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8ec4d-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ec4d-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ec4d-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ec4d-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ec4d-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ec4d-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ec4d-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ec4d-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ec4d-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ec4d-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8ec4d-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8ec4d-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8ec4d-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8ec4d-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8ec4d-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8ec4d-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8ec4d-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ec4d-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8ec4d-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8ec4d-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8ec4d-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8ec4d-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8ec4d-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8ec4d-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8ec4d-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8ec4d-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
