---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRMNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 09d75e73cc6139bfa2c3d0d6293b07060a709f15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764345"
---
# <span data-ttu-id="cc60d-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cc60d-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="cc60d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc60d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc60d-103">Belirtilen konumdan Azure bölgelerine Internet servis sağlayıcılarının göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="cc60d-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc60d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc60d-104">SYNTAX</span></span>

### <span data-ttu-id="cc60d-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cc60d-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc60d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cc60d-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc60d-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="cc60d-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc60d-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cc60d-108">SetByLocation</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherLocation <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc60d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc60d-109">DESCRIPTION</span></span>
<span data-ttu-id="cc60d-110">Get-AzureRmNetworkWatcherReachabilityReport, Internet servis sağlayıcılarının belirli bir konumdan Azure bölgelerine göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="cc60d-110">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="cc60d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc60d-111">EXAMPLES</span></span>

### <span data-ttu-id="cc60d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cc60d-112">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="cc60d-113">ABD 'deki 2017-10-10 'dan 2017-10-12 'a kadar Batı ABD 'deki Azure veri merkezi 'ne göreli gecikmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="cc60d-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="cc60d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc60d-114">PARAMETERS</span></span>

### <span data-ttu-id="cc60d-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="cc60d-115">-AsJob</span></span>
<span data-ttu-id="cc60d-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cc60d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc60d-117">-Şehir</span><span class="sxs-lookup"><span data-stu-id="cc60d-117">-City</span></span>
<span data-ttu-id="cc60d-118">Şehrin adı.</span><span class="sxs-lookup"><span data-stu-id="cc60d-118">The name of the city.</span></span>

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

### <span data-ttu-id="cc60d-119">-Ülke</span><span class="sxs-lookup"><span data-stu-id="cc60d-119">-Country</span></span>
<span data-ttu-id="cc60d-120">Ülkenin adı.</span><span class="sxs-lookup"><span data-stu-id="cc60d-120">The name of the country.</span></span>

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

### <span data-ttu-id="cc60d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc60d-121">-DefaultProfile</span></span>
<span data-ttu-id="cc60d-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc60d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc60d-123">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="cc60d-123">-EndTime</span></span>
<span data-ttu-id="cc60d-124">Azure erişilebilirlik raporu için bitiş saati.</span><span class="sxs-lookup"><span data-stu-id="cc60d-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="cc60d-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="cc60d-125">-Location</span></span>
<span data-ttu-id="cc60d-126">Sorgunun kapsamını atamak için isteğe bağlı Azure bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="cc60d-126">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc60d-127">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cc60d-127">-NetworkWatcher</span></span>
<span data-ttu-id="cc60d-128">Ağ İzleyicisi kaynağı</span><span class="sxs-lookup"><span data-stu-id="cc60d-128">The network watcher resource</span></span>

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

### <span data-ttu-id="cc60d-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="cc60d-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="cc60d-130">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="cc60d-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cc60d-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cc60d-131">-NetworkWatcherName</span></span>
<span data-ttu-id="cc60d-132">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="cc60d-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="cc60d-133">-Sağlayıcı</span><span class="sxs-lookup"><span data-stu-id="cc60d-133">-Provider</span></span>
<span data-ttu-id="cc60d-134">Internet hizmet sağlayıcılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="cc60d-134">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc60d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc60d-135">-ResourceGroupName</span></span>
<span data-ttu-id="cc60d-136">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cc60d-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cc60d-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cc60d-137">-ResourceId</span></span>
<span data-ttu-id="cc60d-138">Ağ İzleyicisi kaynağının kimliği.</span><span class="sxs-lookup"><span data-stu-id="cc60d-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="cc60d-139">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="cc60d-139">-StartTime</span></span>
<span data-ttu-id="cc60d-140">Azure erişilebilirlik raporu için başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="cc60d-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="cc60d-141">Durumlu</span><span class="sxs-lookup"><span data-stu-id="cc60d-141">-State</span></span>
<span data-ttu-id="cc60d-142">Durumun adı.</span><span class="sxs-lookup"><span data-stu-id="cc60d-142">The name of the state.</span></span>

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

### <span data-ttu-id="cc60d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc60d-143">CommonParameters</span></span>
<span data-ttu-id="cc60d-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc60d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc60d-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc60d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc60d-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc60d-146">INPUTS</span></span>

### <span data-ttu-id="cc60d-147">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cc60d-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="cc60d-148">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cc60d-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="cc60d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="cc60d-149">System.String</span></span>

## <span data-ttu-id="cc60d-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc60d-150">OUTPUTS</span></span>

### <span data-ttu-id="cc60d-151">Microsoft. Azure. Commands. Network. model. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cc60d-151">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="cc60d-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc60d-152">NOTES</span></span>
<span data-ttu-id="cc60d-153">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, erişilebilirlik, rapor</span><span class="sxs-lookup"><span data-stu-id="cc60d-153">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="cc60d-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc60d-154">RELATED LINKS</span></span>

[<span data-ttu-id="cc60d-155">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cc60d-155">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cc60d-156">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cc60d-156">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cc60d-157">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cc60d-157">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cc60d-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cc60d-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="cc60d-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cc60d-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cc60d-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cc60d-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="cc60d-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cc60d-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cc60d-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc60d-162">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cc60d-163">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cc60d-163">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="cc60d-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc60d-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cc60d-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc60d-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cc60d-166">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cc60d-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cc60d-167">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc60d-167">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cc60d-168">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cc60d-168">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="cc60d-169">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cc60d-169">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="cc60d-170">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cc60d-170">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cc60d-171">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cc60d-171">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cc60d-172">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cc60d-172">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cc60d-173">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cc60d-173">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cc60d-174">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cc60d-174">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cc60d-175">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cc60d-175">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cc60d-176">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cc60d-176">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cc60d-177">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cc60d-177">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cc60d-178">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cc60d-178">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cc60d-179">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cc60d-179">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cc60d-180">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cc60d-180">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="cc60d-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cc60d-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
