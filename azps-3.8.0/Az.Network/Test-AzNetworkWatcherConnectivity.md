---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: b6c33809c1b738db47407ec65352adfcfb001957
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096574"
---
# <span data-ttu-id="e22d0-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e22d0-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="e22d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e22d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e22d0-103">Belirtilen kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e22d0-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="e22d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e22d0-104">SYNTAX</span></span>

### <span data-ttu-id="e22d0-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e22d0-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e22d0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e22d0-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e22d0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e22d0-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e22d0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e22d0-108">DESCRIPTION</span></span>
<span data-ttu-id="e22d0-109">Test-AzNetworkWatcherConnectivity cmdlet 'i, belirli bir kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e22d0-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="e22d0-110">Kaynak ile hedef arasındaki bağlantı kurulamazsa, cmdlet sorun hakkında ayrıntılı bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="e22d0-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="e22d0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e22d0-111">EXAMPLES</span></span>

### <span data-ttu-id="e22d0-112">Örnek 1: VM 'den Web sitesine ağ Izleyicisi bağlantısını sınama</span><span class="sxs-lookup"><span data-stu-id="e22d0-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="e22d0-113">Bu örnekte, Azure 'daki bir VM 'den www.bing.com 'e bağlantıyı test ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="e22d0-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="e22d0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e22d0-114">PARAMETERS</span></span>

### <span data-ttu-id="e22d0-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="e22d0-115">-AsJob</span></span>
<span data-ttu-id="e22d0-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e22d0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e22d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22d0-117">-DefaultProfile</span></span>
<span data-ttu-id="e22d0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e22d0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e22d0-119">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e22d0-119">-DestinationAddress</span></span>
<span data-ttu-id="e22d0-120">Bir bağlantı girişiminin gerçekleştirildiği kaynağın IP adresi veya URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="e22d0-120">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e22d0-121">-Destinationıd</span><span class="sxs-lookup"><span data-stu-id="e22d0-121">-DestinationId</span></span>
<span data-ttu-id="e22d0-122">Bağlantı girişiminin gerçekleştirildiği kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e22d0-122">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e22d0-123">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e22d0-123">-DestinationPort</span></span>
<span data-ttu-id="e22d0-124">Denetim bağlantısının gerçekleştirileceği bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="e22d0-124">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e22d0-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="e22d0-125">-Location</span></span>
<span data-ttu-id="e22d0-126">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="e22d0-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e22d0-127">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="e22d0-127">-NetworkWatcher</span></span>
<span data-ttu-id="e22d0-128">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="e22d0-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="e22d0-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e22d0-129">-NetworkWatcherName</span></span>
<span data-ttu-id="e22d0-130">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="e22d0-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e22d0-131">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e22d0-131">-ProtocolConfiguration</span></span>
<span data-ttu-id="e22d0-132">Denetim bağlantısının gerçekleştirileceği iletişim kuralı yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="e22d0-132">Protocol configuration on which check connectivity will be performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e22d0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e22d0-133">-ResourceGroupName</span></span>
<span data-ttu-id="e22d0-134">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e22d0-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e22d0-135">-SourceID</span><span class="sxs-lookup"><span data-stu-id="e22d0-135">-SourceId</span></span>
<span data-ttu-id="e22d0-136">Bağlantı denetiminin başlatılacağı kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e22d0-136">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="e22d0-137">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="e22d0-137">-SourcePort</span></span>
<span data-ttu-id="e22d0-138">Bağlantı denetiminin gerçekleştirileceği kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="e22d0-138">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e22d0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22d0-139">CommonParameters</span></span>
<span data-ttu-id="e22d0-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e22d0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22d0-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e22d0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22d0-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e22d0-142">INPUTS</span></span>

### <span data-ttu-id="e22d0-143">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="e22d0-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e22d0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e22d0-144">System.String</span></span>

### <span data-ttu-id="e22d0-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e22d0-145">System.Int32</span></span>

## <span data-ttu-id="e22d0-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e22d0-146">OUTPUTS</span></span>

### <span data-ttu-id="e22d0-147">Microsoft. Azure. Commands. Network. model. Psconnectivityınformation</span><span class="sxs-lookup"><span data-stu-id="e22d0-147">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="e22d0-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e22d0-148">NOTES</span></span>
<span data-ttu-id="e22d0-149">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="e22d0-149">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="e22d0-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e22d0-150">RELATED LINKS</span></span>

<span data-ttu-id="e22d0-151">[Yeni-Azağ İzleyicisi](./New-AzNetworkWatcher.md) 
 [Get-Azağizleyicisi](./Get-AzNetworkWatcher.md) 
 [Remove-Aznetworkizleyicisi](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="e22d0-151">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="e22d0-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="e22d0-152">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="e22d0-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Yeni-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="e22d0-153">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="e22d0-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
 [New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md) 
 [Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md) 
 [Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md) 
 [Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md) 
 [Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="e22d0-154">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)
[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)
[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)
[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)
[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span></span>