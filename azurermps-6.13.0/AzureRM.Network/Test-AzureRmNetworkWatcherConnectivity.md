---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcherconnectivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
ms.openlocfilehash: 6e851b8ac695a2c5fcfd9ef84571899492386124
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764607"
---
# <span data-ttu-id="2ae0e-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2ae0e-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="2ae0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ae0e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae0e-103">Belirtilen kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ae0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ae0e-104">SYNTAX</span></span>

### <span data-ttu-id="2ae0e-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ae0e-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ae0e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2ae0e-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ae0e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2ae0e-107">SetByLocation</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -Location <String> -SourceId <String> [-SourcePort <Int32>]
 [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-ProtocolConfiguration <PSNetworkWatcherProtocolConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ae0e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ae0e-108">DESCRIPTION</span></span>
<span data-ttu-id="2ae0e-109">Test-AzureRmNetworkWatcherConnectivity cmdlet 'i, belirli bir kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-109">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="2ae0e-110">Kaynak ile hedef arasındaki bağlantı kurulamazsa, cmdlet sorun hakkında ayrıntılı bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-110">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="2ae0e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ae0e-111">EXAMPLES</span></span>

### <span data-ttu-id="2ae0e-112">Örnek 1: VM 'den Web sitesine ağ Izleyicisi bağlantısını sınama</span><span class="sxs-lookup"><span data-stu-id="2ae0e-112">Example 1: Test Network Watcher Connectivity from a VM to a website</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


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

<span data-ttu-id="2ae0e-113">Bu örnekte, Azure 'daki bir VM 'den www.bing.com 'e bağlantıyı test ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="2ae0e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ae0e-114">PARAMETERS</span></span>

### <span data-ttu-id="2ae0e-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="2ae0e-115">-AsJob</span></span>
<span data-ttu-id="2ae0e-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2ae0e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ae0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae0e-117">-DefaultProfile</span></span>
<span data-ttu-id="2ae0e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ae0e-119">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="2ae0e-119">-DestinationAddress</span></span>
<span data-ttu-id="2ae0e-120">Bir bağlantı girişiminin gerçekleştirildiği kaynağın IP adresi veya URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-120">The IP address or URI the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="2ae0e-121">-Destinationıd</span><span class="sxs-lookup"><span data-stu-id="2ae0e-121">-DestinationId</span></span>
<span data-ttu-id="2ae0e-122">Bağlantı girişiminin gerçekleştirildiği kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-122">The ID of the resource to which a connection attempt will be made.</span></span>

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

### <span data-ttu-id="2ae0e-123">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2ae0e-123">-DestinationPort</span></span>
<span data-ttu-id="2ae0e-124">Denetim bağlantısının gerçekleştirileceği bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-124">Port on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="2ae0e-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="2ae0e-125">-Location</span></span>
<span data-ttu-id="2ae0e-126">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2ae0e-127">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="2ae0e-127">-NetworkWatcher</span></span>
<span data-ttu-id="2ae0e-128">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="2ae0e-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2ae0e-129">-NetworkWatcherName</span></span>
<span data-ttu-id="2ae0e-130">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="2ae0e-131">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ae0e-131">-ProtocolConfiguration</span></span>
<span data-ttu-id="2ae0e-132">Denetim bağlantısının gerçekleştirileceği protocal yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-132">Protocal configuration on which check connectivity will be performed.</span></span>

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

### <span data-ttu-id="2ae0e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ae0e-133">-ResourceGroupName</span></span>
<span data-ttu-id="2ae0e-134">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2ae0e-135">-SourceID</span><span class="sxs-lookup"><span data-stu-id="2ae0e-135">-SourceId</span></span>
<span data-ttu-id="2ae0e-136">Bağlantı denetiminin başlatılacağı kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-136">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="2ae0e-137">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="2ae0e-137">-SourcePort</span></span>
<span data-ttu-id="2ae0e-138">Bağlantı denetiminin gerçekleştirileceği kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-138">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="2ae0e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae0e-139">CommonParameters</span></span>
<span data-ttu-id="2ae0e-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ae0e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae0e-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ae0e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae0e-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ae0e-142">INPUTS</span></span>

### <span data-ttu-id="2ae0e-143">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="2ae0e-143">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2ae0e-144">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ae0e-144">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="2ae0e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2ae0e-145">System.String</span></span>

### <span data-ttu-id="2ae0e-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2ae0e-146">System.Int32</span></span>

## <span data-ttu-id="2ae0e-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ae0e-147">OUTPUTS</span></span>

### <span data-ttu-id="2ae0e-148">Microsoft. Azure. Commands. Network. model. Psconnectivityınformation</span><span class="sxs-lookup"><span data-stu-id="2ae0e-148">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="2ae0e-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ae0e-149">NOTES</span></span>
<span data-ttu-id="2ae0e-150">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="2ae0e-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="2ae0e-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ae0e-151">RELATED LINKS</span></span>

<span data-ttu-id="2ae0e-152">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="2ae0e-152">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="2ae0e-153">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="2ae0e-153">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="2ae0e-154">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="2ae0e-154">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>


<span data-ttu-id="2ae0e-155">[Start-AzureRmNetworkWatcherResourceTroubleshooting](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md) 
 [New-AzureRmNetworkWatcherProtocolConfiguration](./New-AzureRmNetworkWatcherProtocolConfiguration.md) 
 [Test-AzureRmNetworkWatcherIPFlow](./Test-AzureRmNetworkWatcherIPFlow.md) 
 [Test-AzureRmNetworkWatcherConnectivity](./Test-AzureRmNetworkWatcherConnectivity.md) 
 [Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConfigFlowLog](./Set-AzureRmNetworkWatcherConfigFlowLog.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRMNetworkWatcherReachabilityReport](./Get-AzureRMNetworkWatcherReachabilityReport.md) 
 [Get-AzureRmNetworkWatcherReachabilityProvidersList](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md) 
 [Get-AzureRmNetworkWatcherFlowLogStatus](./Get-AzureRmNetworkWatcherFlowLogStatus.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor)</span><span class="sxs-lookup"><span data-stu-id="2ae0e-155">[Start-AzureRmNetworkWatcherResourceTroubleshooting](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
[New-AzureRmNetworkWatcherProtocolConfiguration](./New-AzureRmNetworkWatcherProtocolConfiguration.md)
[Test-AzureRmNetworkWatcherIPFlow](./Test-AzureRmNetworkWatcherIPFlow.md)
[Test-AzureRmNetworkWatcherConnectivity](./Test-AzureRmNetworkWatcherConnectivity.md)
[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConfigFlowLog](./Set-AzureRmNetworkWatcherConfigFlowLog.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRMNetworkWatcherReachabilityReport](./Get-AzureRMNetworkWatcherReachabilityReport.md)
[Get-AzureRmNetworkWatcherReachabilityProvidersList](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)
[Get-AzureRmNetworkWatcherFlowLogStatus](./Get-AzureRmNetworkWatcherFlowLogStatus.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor)</span></span>
