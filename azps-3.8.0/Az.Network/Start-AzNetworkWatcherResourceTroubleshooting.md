---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: e8e8b9dfd217f9407af8db18a5f468d7d971c97d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937426"
---
# <span data-ttu-id="3d3fe-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3d3fe-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="3d3fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3fe-103">Azure 'daki bir ağ kaynağında sorun gidermeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="3d3fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d3fe-104">SYNTAX</span></span>

### <span data-ttu-id="3d3fe-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d3fe-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d3fe-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3d3fe-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d3fe-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3d3fe-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d3fe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d3fe-108">DESCRIPTION</span></span>
<span data-ttu-id="3d3fe-109">Start-AzNetworkWatcherResourceTroubleshooting cmdlet 'i Azure 'daki bir ağ kaynağında sorun gidermeyi başlatır ve olası sorunlar ve Azaltıcı Etkenler hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="3d3fe-110">Şu anda sanal ağ geçitleri ve bağlantılar desteklenir.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="3d3fe-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d3fe-111">EXAMPLES</span></span>

### <span data-ttu-id="3d3fe-112">Örnek 1: sanal ağ geçidinde sorun gidermeyi başlatma</span><span class="sxs-lookup"><span data-stu-id="3d3fe-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="3d3fe-113">Yukarıdaki örnek sanal ağ geçidinde sorun gidermeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="3d3fe-114">İşlemin tamamlanması birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="3d3fe-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d3fe-115">PARAMETERS</span></span>

### <span data-ttu-id="3d3fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3fe-116">-DefaultProfile</span></span>
<span data-ttu-id="3d3fe-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d3fe-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="3d3fe-118">-Location</span></span>
<span data-ttu-id="3d3fe-119">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3d3fe-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3d3fe-120">-NetworkWatcher</span></span>
<span data-ttu-id="3d3fe-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="3d3fe-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3d3fe-122">-NetworkWatcherName</span></span>
<span data-ttu-id="3d3fe-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="3d3fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d3fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d3fe-125">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3d3fe-126">-Storageıd</span><span class="sxs-lookup"><span data-stu-id="3d3fe-126">-StorageId</span></span>
<span data-ttu-id="3d3fe-127">Depolama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-127">The storage ID.</span></span>

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

### <span data-ttu-id="3d3fe-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="3d3fe-128">-StoragePath</span></span>
<span data-ttu-id="3d3fe-129">Depolama yolu.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-129">The storage path.</span></span>

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

### <span data-ttu-id="3d3fe-130">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="3d3fe-130">-TargetResourceId</span></span>
<span data-ttu-id="3d3fe-131">Sorunu gidermek için kaynağın kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="3d3fe-132">Örnek biçim: "/Subscriptions/$ {SubscriptionID}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="3d3fe-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="3d3fe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3fe-133">CommonParameters</span></span>
<span data-ttu-id="3d3fe-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d3fe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3fe-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d3fe-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3fe-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d3fe-136">INPUTS</span></span>

### <span data-ttu-id="3d3fe-137">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3d3fe-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3d3fe-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3d3fe-138">System.String</span></span>

## <span data-ttu-id="3d3fe-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d3fe-139">OUTPUTS</span></span>

### <span data-ttu-id="3d3fe-140">Microsoft. Azure. Commands. Network. modeller. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3d3fe-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="3d3fe-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d3fe-141">NOTES</span></span>
<span data-ttu-id="3d3fe-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sorun giderme, VPN, bağlantı</span><span class="sxs-lookup"><span data-stu-id="3d3fe-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="3d3fe-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d3fe-143">RELATED LINKS</span></span>

[<span data-ttu-id="3d3fe-144">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="3d3fe-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3d3fe-145">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3d3fe-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3d3fe-146">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3d3fe-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3d3fe-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3d3fe-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3d3fe-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3d3fe-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3d3fe-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3d3fe-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3d3fe-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3d3fe-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3d3fe-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d3fe-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d3fe-152">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3d3fe-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3d3fe-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d3fe-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d3fe-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d3fe-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d3fe-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d3fe-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d3fe-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d3fe-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3d3fe-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3d3fe-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3d3fe-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3d3fe-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3d3fe-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d3fe-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d3fe-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d3fe-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d3fe-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d3fe-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d3fe-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3d3fe-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3d3fe-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d3fe-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d3fe-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d3fe-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d3fe-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3d3fe-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3d3fe-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3d3fe-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3d3fe-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3d3fe-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3d3fe-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3d3fe-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3d3fe-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3d3fe-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="3d3fe-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d3fe-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)