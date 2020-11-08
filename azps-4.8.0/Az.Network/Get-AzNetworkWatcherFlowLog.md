---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5f4322ba81cdae5bdb0b33c2658a6d7934ed638d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266558"
---
# <span data-ttu-id="99b27-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="99b27-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="99b27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99b27-102">SYNOPSIS</span></span>
<span data-ttu-id="99b27-103">Belirtilen abonelik ve bölgedeki akış günlüğü kaynağı veya akış günlüğü kaynaklarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="99b27-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="99b27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99b27-104">SYNTAX</span></span>

### <span data-ttu-id="99b27-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="99b27-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b27-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="99b27-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b27-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="99b27-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99b27-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="99b27-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99b27-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="99b27-109">DESCRIPTION</span></span>
<span data-ttu-id="99b27-110">Belirtilen abonelik ve bölgedeki akış günlüğü kaynağı veya akış günlüğü kaynaklarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="99b27-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="99b27-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99b27-111">EXAMPLES</span></span>

### <span data-ttu-id="99b27-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99b27-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="99b27-113">Ad: pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: başarılı konum: eastus Targetresourceıd:/Subscriptions/56abfbvseç6-ec72-4ce9-831F-bc2b6f2c5505/ResourceGroups/myflowlog/set RS/Microsoft. Network/networkSecurityGroups/MyNSG Storageıd:/Subscriptions/56abfbvseç6-ec72-4ce9-831F-bc2b6f2c5505/dcgroups/flowlogsv2, RetentionPolicy: {"Days": 5, "Enabled": true} biçimi: {"tür": "JSON", "sürüm": 2} Flowanalyzer Ticsconfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": true, "çalışma" workspaceRegion ":" eastus "," workspaceResourceId ":"/Subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/FlowLogsV2Demo/Providers/Microsoft. Operationalınsights/ÇalışmaAlanı "," trafficAnalyticsInterval ": 60}</span><span class="sxs-lookup"><span data-stu-id="99b27-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="99b27-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99b27-114">PARAMETERS</span></span>

### <span data-ttu-id="99b27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b27-115">-DefaultProfile</span></span>
<span data-ttu-id="99b27-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99b27-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b27-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="99b27-117">-Location</span></span>
<span data-ttu-id="99b27-118">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="99b27-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b27-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="99b27-119">-Name</span></span>
<span data-ttu-id="99b27-120">Akış günlüğü adı.</span><span class="sxs-lookup"><span data-stu-id="99b27-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b27-121">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="99b27-121">-NetworkWatcher</span></span>
<span data-ttu-id="99b27-122">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="99b27-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="99b27-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="99b27-123">-NetworkWatcherName</span></span>
<span data-ttu-id="99b27-124">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="99b27-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b27-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b27-125">-ResourceGroupName</span></span>
<span data-ttu-id="99b27-126">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="99b27-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b27-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="99b27-127">-ResourceId</span></span>
<span data-ttu-id="99b27-128">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="99b27-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b27-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b27-129">CommonParameters</span></span>
<span data-ttu-id="99b27-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99b27-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b27-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="99b27-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b27-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99b27-132">INPUTS</span></span>

### <span data-ttu-id="99b27-133">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="99b27-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="99b27-134">System. String</span><span class="sxs-lookup"><span data-stu-id="99b27-134">System.String</span></span>

## <span data-ttu-id="99b27-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99b27-135">OUTPUTS</span></span>

### <span data-ttu-id="99b27-136">Microsoft. Azure. Commands. Network. model. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="99b27-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="99b27-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99b27-137">NOTES</span></span>

## <span data-ttu-id="99b27-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99b27-138">RELATED LINKS</span></span>

[<span data-ttu-id="99b27-139">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="99b27-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="99b27-140">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="99b27-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="99b27-141">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="99b27-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="99b27-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="99b27-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="99b27-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="99b27-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="99b27-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="99b27-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="99b27-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="99b27-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="99b27-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99b27-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99b27-147">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="99b27-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="99b27-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99b27-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99b27-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99b27-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99b27-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="99b27-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="99b27-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="99b27-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="99b27-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="99b27-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="99b27-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="99b27-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="99b27-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99b27-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99b27-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99b27-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99b27-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99b27-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99b27-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="99b27-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="99b27-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99b27-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99b27-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99b27-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="99b27-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="99b27-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="99b27-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="99b27-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="99b27-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="99b27-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="99b27-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="99b27-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="99b27-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="99b27-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="99b27-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="99b27-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="99b27-166">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="99b27-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="99b27-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="99b27-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="99b27-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="99b27-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
