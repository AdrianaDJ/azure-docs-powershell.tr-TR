---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: cdc97ff5e528e58aa088950f5272e7689f35b10e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931993"
---
# <span data-ttu-id="dc491-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="dc491-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="dc491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc491-102">SYNOPSIS</span></span>
<span data-ttu-id="dc491-103">Bir kaynaktaki akış günlüğünün durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="dc491-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="dc491-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc491-104">SYNTAX</span></span>

### <span data-ttu-id="dc491-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dc491-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc491-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dc491-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc491-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="dc491-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc491-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc491-108">DESCRIPTION</span></span>
<span data-ttu-id="dc491-109">Get-AzNetworkWatcherFlowLogStatus cmdlet 'i bir kaynaktaki akış günlüğünün durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="dc491-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="dc491-110">Bu durum, sağlanan kaynak için akış günlüğünün etkinleştirilip etkinleştirilmeyeceğini, günlükleri gönderecek yapılandırılmış depolama hesabının ve günlüklerin bekletme ilkesinin etkinleştirilip etkinleştirilmediğini içerir.</span><span class="sxs-lookup"><span data-stu-id="dc491-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="dc491-111">Ağ güvenlik grupları akış günlüğü için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="dc491-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="dc491-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc491-112">EXAMPLES</span></span>

### <span data-ttu-id="dc491-113">Örnek 1: belirli bir NSG için akış günlüğü durumunu alma</span><span class="sxs-lookup"><span data-stu-id="dc491-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="dc491-114">Bu örnekte, bir ağ güvenlik grubunun akış günlüğü durumu.</span><span class="sxs-lookup"><span data-stu-id="dc491-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="dc491-115">Belirtilen NSG 'de akış günlüğü etkin, varsayılan biçim ve bekletme ilkesi ayarlanmamış.</span><span class="sxs-lookup"><span data-stu-id="dc491-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="dc491-116">Örnek 2: belirli bir NSG için akış günlüğü ve trafik analizi durumunu alma</span><span class="sxs-lookup"><span data-stu-id="dc491-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="dc491-117">Bu örnekte, bir ağ güvenlik grubuna akış günlüğü ve trafik analizi durumu yaptık.</span><span class="sxs-lookup"><span data-stu-id="dc491-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="dc491-118">Belirtilen NSG 'de akış günlüğü ve trafik analizi etkinleştirilmiş, varsayılan biçim ve bekletme ilkesi ayarlanmamış.</span><span class="sxs-lookup"><span data-stu-id="dc491-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="dc491-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc491-119">PARAMETERS</span></span>

### <span data-ttu-id="dc491-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="dc491-120">-AsJob</span></span>
<span data-ttu-id="dc491-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="dc491-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc491-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc491-122">-DefaultProfile</span></span>
<span data-ttu-id="dc491-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc491-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc491-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="dc491-124">-Location</span></span>
<span data-ttu-id="dc491-125">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="dc491-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="dc491-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="dc491-126">-NetworkWatcher</span></span>
<span data-ttu-id="dc491-127">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="dc491-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="dc491-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dc491-128">-NetworkWatcherName</span></span>
<span data-ttu-id="dc491-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="dc491-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="dc491-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc491-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc491-131">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="dc491-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dc491-132">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="dc491-132">-TargetResourceId</span></span>
<span data-ttu-id="dc491-133">Hedef kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="dc491-133">The target resource ID.</span></span>

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

### <span data-ttu-id="dc491-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc491-134">CommonParameters</span></span>
<span data-ttu-id="dc491-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc491-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc491-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dc491-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc491-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc491-137">INPUTS</span></span>

### <span data-ttu-id="dc491-138">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="dc491-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="dc491-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc491-139">System.String</span></span>

## <span data-ttu-id="dc491-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc491-140">OUTPUTS</span></span>

### <span data-ttu-id="dc491-141">Microsoft. Azure. Commands. Network. modeller. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="dc491-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="dc491-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc491-142">NOTES</span></span>
<span data-ttu-id="dc491-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, akış, Günlükler, akışgünlüğü, günlüğe kaydetme</span><span class="sxs-lookup"><span data-stu-id="dc491-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="dc491-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc491-144">RELATED LINKS</span></span>

[<span data-ttu-id="dc491-145">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="dc491-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="dc491-146">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="dc491-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="dc491-147">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="dc491-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="dc491-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dc491-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="dc491-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dc491-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dc491-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dc491-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="dc491-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dc491-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dc491-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc491-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc491-153">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dc491-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="dc491-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc491-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc491-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc491-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc491-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc491-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc491-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc491-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="dc491-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dc491-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="dc491-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="dc491-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="dc491-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc491-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc491-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc491-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc491-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc491-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc491-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="dc491-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="dc491-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc491-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc491-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc491-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc491-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="dc491-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="dc491-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="dc491-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="dc491-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="dc491-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="dc491-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="dc491-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="dc491-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="dc491-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="dc491-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc491-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)