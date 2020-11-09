---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 83d7da65ad8c525d4c37ab1b5f78eb72bf1d9f49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323203"
---
# <span data-ttu-id="94af4-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94af4-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="94af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94af4-102">SYNOPSIS</span></span>
<span data-ttu-id="94af4-103">Bağlantı izleyicisini başlatma</span><span class="sxs-lookup"><span data-stu-id="94af4-103">Start a connection monitor</span></span>

## <span data-ttu-id="94af4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94af4-104">SYNTAX</span></span>

### <span data-ttu-id="94af4-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="94af4-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94af4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="94af4-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94af4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="94af4-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94af4-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="94af4-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94af4-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="94af4-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94af4-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="94af4-110">DESCRIPTION</span></span>
<span data-ttu-id="94af4-111">Start-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini başlatır.</span><span class="sxs-lookup"><span data-stu-id="94af4-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="94af4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94af4-112">EXAMPLES</span></span>

### <span data-ttu-id="94af4-113">Örnek 1: bağlantı izleyicisini başlatma</span><span class="sxs-lookup"><span data-stu-id="94af4-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="94af4-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini başlatabiliriz</span><span class="sxs-lookup"><span data-stu-id="94af4-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="94af4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94af4-115">PARAMETERS</span></span>

### <span data-ttu-id="94af4-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="94af4-116">-AsJob</span></span>
<span data-ttu-id="94af4-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="94af4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94af4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94af4-118">-DefaultProfile</span></span>
<span data-ttu-id="94af4-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94af4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94af4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94af4-120">-InputObject</span></span>
<span data-ttu-id="94af4-121">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="94af4-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="94af4-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="94af4-122">-Location</span></span>
<span data-ttu-id="94af4-123">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="94af4-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="94af4-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="94af4-124">-Name</span></span>
<span data-ttu-id="94af4-125">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="94af4-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="94af4-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="94af4-126">-NetworkWatcher</span></span>
<span data-ttu-id="94af4-127">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="94af4-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="94af4-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="94af4-128">-NetworkWatcherName</span></span>
<span data-ttu-id="94af4-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="94af4-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="94af4-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="94af4-130">-PassThru</span></span>
<span data-ttu-id="94af4-131">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="94af4-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="94af4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94af4-132">-ResourceGroupName</span></span>
<span data-ttu-id="94af4-133">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="94af4-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="94af4-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="94af4-134">-ResourceId</span></span>
<span data-ttu-id="94af4-135">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="94af4-135">Resource ID.</span></span>

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

### <span data-ttu-id="94af4-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="94af4-136">-Confirm</span></span>
<span data-ttu-id="94af4-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94af4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94af4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94af4-138">-WhatIf</span></span>
<span data-ttu-id="94af4-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94af4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94af4-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94af4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94af4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94af4-141">CommonParameters</span></span>
<span data-ttu-id="94af4-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94af4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94af4-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94af4-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94af4-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94af4-144">INPUTS</span></span>

### <span data-ttu-id="94af4-145">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="94af4-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="94af4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="94af4-146">System.String</span></span>

### <span data-ttu-id="94af4-147">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="94af4-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="94af4-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94af4-148">OUTPUTS</span></span>

### <span data-ttu-id="94af4-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94af4-149">System.Boolean</span></span>

## <span data-ttu-id="94af4-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94af4-150">NOTES</span></span>
<span data-ttu-id="94af4-151">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="94af4-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="94af4-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94af4-152">RELATED LINKS</span></span>

[<span data-ttu-id="94af4-153">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="94af4-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="94af4-154">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="94af4-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="94af4-155">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="94af4-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="94af4-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="94af4-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="94af4-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="94af4-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="94af4-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="94af4-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="94af4-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="94af4-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="94af4-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94af4-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94af4-161">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="94af4-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="94af4-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94af4-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94af4-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94af4-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94af4-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="94af4-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="94af4-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94af4-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94af4-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="94af4-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="94af4-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94af4-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94af4-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94af4-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94af4-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94af4-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94af4-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94af4-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94af4-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="94af4-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="94af4-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="94af4-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="94af4-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="94af4-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="94af4-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="94af4-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="94af4-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="94af4-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="94af4-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="94af4-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="94af4-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="94af4-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="94af4-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="94af4-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="94af4-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="94af4-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
