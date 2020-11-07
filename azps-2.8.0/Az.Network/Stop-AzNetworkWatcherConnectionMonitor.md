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
ms.locfileid: "93932708"
---
# <span data-ttu-id="85527-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85527-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="85527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85527-102">SYNOPSIS</span></span>
<span data-ttu-id="85527-103">Bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="85527-103">Stop a connection monitor</span></span>

## <span data-ttu-id="85527-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85527-104">SYNTAX</span></span>

### <span data-ttu-id="85527-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="85527-105">SetByName (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85527-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="85527-106">SetByResource</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85527-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="85527-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85527-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="85527-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85527-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="85527-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85527-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="85527-110">DESCRIPTION</span></span>
<span data-ttu-id="85527-111">Stop-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini durdurur.</span><span class="sxs-lookup"><span data-stu-id="85527-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="85527-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85527-112">EXAMPLES</span></span>

### <span data-ttu-id="85527-113">Örnek 1: bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="85527-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="85527-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini durdurmamız</span><span class="sxs-lookup"><span data-stu-id="85527-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="85527-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85527-115">PARAMETERS</span></span>

### <span data-ttu-id="85527-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="85527-116">-AsJob</span></span>
<span data-ttu-id="85527-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="85527-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85527-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85527-118">-DefaultProfile</span></span>
<span data-ttu-id="85527-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85527-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85527-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85527-120">-InputObject</span></span>
<span data-ttu-id="85527-121">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="85527-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="85527-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="85527-122">-Location</span></span>
<span data-ttu-id="85527-123">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="85527-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="85527-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="85527-124">-Name</span></span>
<span data-ttu-id="85527-125">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="85527-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="85527-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="85527-126">-NetworkWatcher</span></span>
<span data-ttu-id="85527-127">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="85527-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="85527-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="85527-128">-NetworkWatcherName</span></span>
<span data-ttu-id="85527-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="85527-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="85527-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="85527-130">-PassThru</span></span>
<span data-ttu-id="85527-131">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="85527-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="85527-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85527-132">-ResourceGroupName</span></span>
<span data-ttu-id="85527-133">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="85527-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="85527-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="85527-134">-ResourceId</span></span>
<span data-ttu-id="85527-135">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="85527-135">Resource ID.</span></span>

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

### <span data-ttu-id="85527-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="85527-136">-Confirm</span></span>
<span data-ttu-id="85527-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="85527-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85527-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85527-138">-WhatIf</span></span>
<span data-ttu-id="85527-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85527-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85527-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="85527-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85527-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85527-141">CommonParameters</span></span>
<span data-ttu-id="85527-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85527-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85527-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85527-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85527-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85527-144">INPUTS</span></span>

### <span data-ttu-id="85527-145">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="85527-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="85527-146">System. String</span><span class="sxs-lookup"><span data-stu-id="85527-146">System.String</span></span>

### <span data-ttu-id="85527-147">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="85527-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="85527-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85527-148">OUTPUTS</span></span>

### <span data-ttu-id="85527-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85527-149">System.Boolean</span></span>

## <span data-ttu-id="85527-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85527-150">NOTES</span></span>
<span data-ttu-id="85527-151">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="85527-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="85527-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85527-152">RELATED LINKS</span></span>

[<span data-ttu-id="85527-153">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="85527-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="85527-154">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="85527-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="85527-155">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="85527-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="85527-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="85527-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="85527-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="85527-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="85527-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="85527-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="85527-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="85527-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="85527-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85527-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85527-161">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="85527-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="85527-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85527-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85527-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85527-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85527-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85527-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85527-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85527-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85527-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="85527-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="85527-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85527-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85527-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85527-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85527-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85527-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85527-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85527-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85527-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="85527-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="85527-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="85527-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="85527-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="85527-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="85527-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="85527-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="85527-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85527-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85527-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="85527-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="85527-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="85527-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="85527-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="85527-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="85527-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="85527-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
