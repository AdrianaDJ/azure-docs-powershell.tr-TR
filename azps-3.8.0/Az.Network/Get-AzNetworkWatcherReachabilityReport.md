---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 0ad2b1fa6278e085a57d94f2fec9be2c6853993d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937679"
---
# <span data-ttu-id="8c9d4-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8c9d4-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="8c9d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="8c9d4-103">Belirtilen konumdan Azure bölgelerine Internet servis sağlayıcılarının göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="8c9d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c9d4-104">SYNTAX</span></span>

### <span data-ttu-id="8c9d4-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8c9d4-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c9d4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8c9d4-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c9d4-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="8c9d4-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c9d4-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8c9d4-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c9d4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c9d4-109">DESCRIPTION</span></span>
<span data-ttu-id="8c9d4-110">Get-AzNetworkWatcherReachabilityReport, Internet servis sağlayıcılarının belirli bir konumdan Azure bölgelerine göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="8c9d4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c9d4-111">EXAMPLES</span></span>

### <span data-ttu-id="8c9d4-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8c9d4-112">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="8c9d4-113">ABD 'deki 2017-10-10 'dan 2017-10-12 'a kadar Batı ABD 'deki Azure veri merkezi 'ne göreli gecikmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="8c9d4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c9d4-114">PARAMETERS</span></span>

### <span data-ttu-id="8c9d4-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="8c9d4-115">-AsJob</span></span>
<span data-ttu-id="8c9d4-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8c9d4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c9d4-117">-Şehir</span><span class="sxs-lookup"><span data-stu-id="8c9d4-117">-City</span></span>
<span data-ttu-id="8c9d4-118">Şehrin adı.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-118">The name of the city.</span></span>

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

### <span data-ttu-id="8c9d4-119">-Ülke</span><span class="sxs-lookup"><span data-stu-id="8c9d4-119">-Country</span></span>
<span data-ttu-id="8c9d4-120">Ülkenin adı.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-120">The name of the country.</span></span>

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

### <span data-ttu-id="8c9d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c9d4-121">-DefaultProfile</span></span>
<span data-ttu-id="8c9d4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c9d4-123">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="8c9d4-123">-EndTime</span></span>
<span data-ttu-id="8c9d4-124">Azure erişilebilirlik raporu için bitiş saati.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-124">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9d4-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="8c9d4-125">-Location</span></span>
<span data-ttu-id="8c9d4-126">Sorgunun kapsamını atamak için isteğe bağlı Azure bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9d4-127">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8c9d4-127">-NetworkWatcher</span></span>
<span data-ttu-id="8c9d4-128">Ağ İzleyicisi kaynağı</span><span class="sxs-lookup"><span data-stu-id="8c9d4-128">The network watcher resource</span></span>

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

### <span data-ttu-id="8c9d4-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="8c9d4-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="8c9d4-130">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8c9d4-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8c9d4-131">-NetworkWatcherName</span></span>
<span data-ttu-id="8c9d4-132">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-132">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9d4-133">-Sağlayıcı</span><span class="sxs-lookup"><span data-stu-id="8c9d4-133">-Provider</span></span>
<span data-ttu-id="8c9d4-134">Internet hizmet sağlayıcılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-134">List of Internet service providers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9d4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c9d4-135">-ResourceGroupName</span></span>
<span data-ttu-id="8c9d4-136">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8c9d4-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8c9d4-137">-ResourceId</span></span>
<span data-ttu-id="8c9d4-138">Ağ İzleyicisi kaynağının kimliği.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="8c9d4-139">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="8c9d4-139">-StartTime</span></span>
<span data-ttu-id="8c9d4-140">Azure erişilebilirlik raporu için başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-140">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c9d4-141">Durumlu</span><span class="sxs-lookup"><span data-stu-id="8c9d4-141">-State</span></span>
<span data-ttu-id="8c9d4-142">Durumun adı.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-142">The name of the state.</span></span>

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

### <span data-ttu-id="8c9d4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c9d4-143">CommonParameters</span></span>
<span data-ttu-id="8c9d4-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c9d4-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8c9d4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c9d4-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c9d4-146">INPUTS</span></span>

### <span data-ttu-id="8c9d4-147">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8c9d4-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8c9d4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8c9d4-148">System.String</span></span>

## <span data-ttu-id="8c9d4-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c9d4-149">OUTPUTS</span></span>

### <span data-ttu-id="8c9d4-150">Microsoft. Azure. Commands. Network. model. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8c9d4-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="8c9d4-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c9d4-151">NOTES</span></span>
<span data-ttu-id="8c9d4-152">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, erişilebilirlik, rapor</span><span class="sxs-lookup"><span data-stu-id="8c9d4-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="8c9d4-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c9d4-153">RELATED LINKS</span></span>

[<span data-ttu-id="8c9d4-154">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="8c9d4-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8c9d4-155">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8c9d4-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8c9d4-156">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8c9d4-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8c9d4-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8c9d4-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8c9d4-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8c9d4-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8c9d4-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8c9d4-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8c9d4-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8c9d4-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8c9d4-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c9d4-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c9d4-162">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8c9d4-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8c9d4-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c9d4-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c9d4-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c9d4-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c9d4-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c9d4-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c9d4-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c9d4-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8c9d4-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8c9d4-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8c9d4-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8c9d4-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8c9d4-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c9d4-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c9d4-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c9d4-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c9d4-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c9d4-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c9d4-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8c9d4-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8c9d4-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c9d4-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c9d4-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c9d4-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c9d4-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8c9d4-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8c9d4-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8c9d4-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8c9d4-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8c9d4-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8c9d4-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8c9d4-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8c9d4-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8c9d4-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="8c9d4-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c9d4-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)