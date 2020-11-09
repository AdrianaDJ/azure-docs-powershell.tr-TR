---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherConnectivity.md
ms.openlocfilehash: 8d3a714f2798c4866df39cd63c664228f078c37c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325186"
---
# <span data-ttu-id="b9c93-101">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b9c93-101">Test-AzNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="b9c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c93-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c93-103">Belirtilen kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b9c93-103">Returns connectivity information for a specified source VM and a destination.</span></span>

## <span data-ttu-id="b9c93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9c93-104">SYNTAX</span></span>

### <span data-ttu-id="b9c93-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b9c93-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c93-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b9c93-106">SetByName</span></span>
```
Test-AzNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c93-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b9c93-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c93-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9c93-108">DESCRIPTION</span></span>
<span data-ttu-id="b9c93-109">Test-AzNetworkWatcherConnectivity cmdlet 'i, belirli bir kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b9c93-109">The Test-AzNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="b9c93-110">Kaynak ile hedef arasındaki bağlantı kurulamazsa, cmdlet sorun hakkında ayrıntılı bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="b9c93-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="b9c93-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9c93-111">EXAMPLES</span></span>

### <span data-ttu-id="b9c93-112">Örnek 1: VM 'den Web sitesine ağ Izleyicisi bağlantısını sınama</span><span class="sxs-lookup"><span data-stu-id="b9c93-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```powershell
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

<span data-ttu-id="b9c93-113">Bu örnekte, Azure 'daki bir VM 'den www.bing.com 'e bağlantıyı test ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="b9c93-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

### <span data-ttu-id="b9c93-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b9c93-114">Example 2</span></span>

<span data-ttu-id="b9c93-115">Belirtilen kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b9c93-115">Returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="b9c93-116">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="b9c93-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Test-AzNetworkWatcherConnectivity -DestinationAddress 'bing.com' -DestinationPort 80 -NetworkWatcher <PSNetworkWatcher> -SourceId '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0'
```

## <span data-ttu-id="b9c93-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9c93-117">PARAMETERS</span></span>

### <span data-ttu-id="b9c93-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="b9c93-118">-AsJob</span></span>
<span data-ttu-id="b9c93-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b9c93-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9c93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c93-120">-DefaultProfile</span></span>
<span data-ttu-id="b9c93-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9c93-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c93-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="b9c93-122">-DestinationAddress</span></span>
<span data-ttu-id="b9c93-123">Bir bağlantı girişiminin gerçekleştirildiği kaynağın IP adresi veya URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="b9c93-123">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="b9c93-124">-Destinationıd</span><span class="sxs-lookup"><span data-stu-id="b9c93-124">-DestinationId</span></span>
<span data-ttu-id="b9c93-125">Bağlantı girişiminin gerçekleştirildiği kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b9c93-125">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="b9c93-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="b9c93-126">-DestinationPort</span></span>
<span data-ttu-id="b9c93-127">Denetim bağlantısının gerçekleştirileceği bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="b9c93-127">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="b9c93-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="b9c93-128">-Location</span></span>
<span data-ttu-id="b9c93-129">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="b9c93-129">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b9c93-130">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b9c93-130">-NetworkWatcher</span></span>
<span data-ttu-id="b9c93-131">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="b9c93-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="b9c93-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b9c93-132">-NetworkWatcherName</span></span>
<span data-ttu-id="b9c93-133">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="b9c93-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="b9c93-134">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9c93-134">-ProtocolConfiguration</span></span>
<span data-ttu-id="b9c93-135">Denetim bağlantısının gerçekleştirileceği iletişim kuralı yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="b9c93-135">Protocol configuration on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="b9c93-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c93-136">-ResourceGroupName</span></span>
<span data-ttu-id="b9c93-137">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b9c93-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b9c93-138">-SourceID</span><span class="sxs-lookup"><span data-stu-id="b9c93-138">-SourceId</span></span>
<span data-ttu-id="b9c93-139">Bağlantı denetiminin başlatılacağı kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b9c93-139">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="b9c93-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="b9c93-140">-SourcePort</span></span>
<span data-ttu-id="b9c93-141">Bağlantı denetiminin gerçekleştirileceği kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="b9c93-141">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="b9c93-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c93-142">CommonParameters</span></span>
<span data-ttu-id="b9c93-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9c93-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c93-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c93-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c93-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9c93-145">INPUTS</span></span>

### <span data-ttu-id="b9c93-146">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b9c93-146">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b9c93-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c93-147">System.String</span></span>

### <span data-ttu-id="b9c93-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b9c93-148">System.Int32</span></span>

## <span data-ttu-id="b9c93-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9c93-149">OUTPUTS</span></span>

### <span data-ttu-id="b9c93-150">Microsoft. Azure. Commands. Network. model. Psconnectivityınformation</span><span class="sxs-lookup"><span data-stu-id="b9c93-150">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="b9c93-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9c93-151">NOTES</span></span>
<span data-ttu-id="b9c93-152">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="b9c93-152">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="b9c93-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9c93-153">RELATED LINKS</span></span>

<span data-ttu-id="b9c93-154">[Yeni-Azağ İzleyicisi](./New-AzNetworkWatcher.md) 
 [Get-Azağizleyicisi](./Get-AzNetworkWatcher.md) 
 [Remove-Aznetworkizleyicisi](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="b9c93-154">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="b9c93-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="b9c93-155">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="b9c93-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Yeni-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="b9c93-156">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="b9c93-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md) 
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
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="b9c93-157">[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)
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
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)</span></span>
