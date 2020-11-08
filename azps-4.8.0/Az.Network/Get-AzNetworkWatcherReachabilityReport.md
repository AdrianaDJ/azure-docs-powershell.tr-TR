---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266549"
---
# <span data-ttu-id="3423b-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3423b-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="3423b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3423b-102">SYNOPSIS</span></span>
<span data-ttu-id="3423b-103">Belirtilen konumdan Azure bölgelerine Internet servis sağlayıcılarının göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="3423b-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="3423b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3423b-104">SYNTAX</span></span>

### <span data-ttu-id="3423b-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3423b-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3423b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3423b-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3423b-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="3423b-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3423b-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3423b-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3423b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3423b-109">DESCRIPTION</span></span>
<span data-ttu-id="3423b-110">Get-AzNetworkWatcherReachabilityReport, Internet servis sağlayıcılarının belirli bir konumdan Azure bölgelerine göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="3423b-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="3423b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3423b-111">EXAMPLES</span></span>

### <span data-ttu-id="3423b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3423b-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="3423b-113">ABD 'deki 2017-10-10 'dan 2017-10-12 'a kadar Batı ABD 'deki Azure veri merkezi 'ne göreli gecikmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="3423b-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="3423b-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3423b-114">Example 2</span></span>

<span data-ttu-id="3423b-115">Belirtilen konumdan Azure bölgelerine Internet servis sağlayıcılarının göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="3423b-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="3423b-116">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="3423b-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="3423b-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3423b-117">PARAMETERS</span></span>

### <span data-ttu-id="3423b-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="3423b-118">-AsJob</span></span>
<span data-ttu-id="3423b-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3423b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3423b-120">-Şehir</span><span class="sxs-lookup"><span data-stu-id="3423b-120">-City</span></span>
<span data-ttu-id="3423b-121">Şehrin adı.</span><span class="sxs-lookup"><span data-stu-id="3423b-121">The name of the city.</span></span>

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

### <span data-ttu-id="3423b-122">-Ülke</span><span class="sxs-lookup"><span data-stu-id="3423b-122">-Country</span></span>
<span data-ttu-id="3423b-123">Ülkenin adı.</span><span class="sxs-lookup"><span data-stu-id="3423b-123">The name of the country.</span></span>

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

### <span data-ttu-id="3423b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3423b-124">-DefaultProfile</span></span>
<span data-ttu-id="3423b-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3423b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3423b-126">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="3423b-126">-EndTime</span></span>
<span data-ttu-id="3423b-127">Azure erişilebilirlik raporu için bitiş saati.</span><span class="sxs-lookup"><span data-stu-id="3423b-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="3423b-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="3423b-128">-Location</span></span>
<span data-ttu-id="3423b-129">Sorgunun kapsamını atamak için isteğe bağlı Azure bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="3423b-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="3423b-130">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3423b-130">-NetworkWatcher</span></span>
<span data-ttu-id="3423b-131">Ağ İzleyicisi kaynağı</span><span class="sxs-lookup"><span data-stu-id="3423b-131">The network watcher resource</span></span>

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

### <span data-ttu-id="3423b-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="3423b-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="3423b-133">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="3423b-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3423b-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3423b-134">-NetworkWatcherName</span></span>
<span data-ttu-id="3423b-135">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="3423b-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="3423b-136">-Sağlayıcı</span><span class="sxs-lookup"><span data-stu-id="3423b-136">-Provider</span></span>
<span data-ttu-id="3423b-137">Internet hizmet sağlayıcılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="3423b-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="3423b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3423b-138">-ResourceGroupName</span></span>
<span data-ttu-id="3423b-139">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3423b-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3423b-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3423b-140">-ResourceId</span></span>
<span data-ttu-id="3423b-141">Ağ İzleyicisi kaynağının kimliği.</span><span class="sxs-lookup"><span data-stu-id="3423b-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="3423b-142">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="3423b-142">-StartTime</span></span>
<span data-ttu-id="3423b-143">Azure erişilebilirlik raporu için başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="3423b-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="3423b-144">Durumlu</span><span class="sxs-lookup"><span data-stu-id="3423b-144">-State</span></span>
<span data-ttu-id="3423b-145">Durumun adı.</span><span class="sxs-lookup"><span data-stu-id="3423b-145">The name of the state.</span></span>

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

### <span data-ttu-id="3423b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3423b-146">CommonParameters</span></span>
<span data-ttu-id="3423b-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3423b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3423b-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3423b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3423b-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3423b-149">INPUTS</span></span>

### <span data-ttu-id="3423b-150">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3423b-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3423b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3423b-151">System.String</span></span>

## <span data-ttu-id="3423b-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3423b-152">OUTPUTS</span></span>

### <span data-ttu-id="3423b-153">Microsoft. Azure. Commands. Network. model. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3423b-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="3423b-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3423b-154">NOTES</span></span>
<span data-ttu-id="3423b-155">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, erişilebilirlik, rapor</span><span class="sxs-lookup"><span data-stu-id="3423b-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="3423b-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3423b-156">RELATED LINKS</span></span>

[<span data-ttu-id="3423b-157">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="3423b-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3423b-158">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3423b-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3423b-159">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="3423b-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3423b-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3423b-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3423b-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3423b-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3423b-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3423b-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3423b-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3423b-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3423b-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3423b-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3423b-165">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3423b-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3423b-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3423b-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3423b-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3423b-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3423b-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3423b-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3423b-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3423b-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3423b-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3423b-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3423b-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3423b-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3423b-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3423b-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3423b-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3423b-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3423b-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3423b-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3423b-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3423b-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3423b-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3423b-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3423b-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3423b-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3423b-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3423b-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3423b-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3423b-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3423b-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3423b-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3423b-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3423b-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3423b-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3423b-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3423b-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3423b-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
