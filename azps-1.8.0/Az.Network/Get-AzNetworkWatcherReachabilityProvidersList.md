---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: cf35292be5005a957e245370a5b15b78bb7d4fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760519"
---
# <span data-ttu-id="4abf4-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4abf4-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="4abf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4abf4-102">SYNOPSIS</span></span>
<span data-ttu-id="4abf4-103">Belirtilen bir Azure bölgesi için kullanılabilir tüm internet hizmeti sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="4abf4-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="4abf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4abf4-104">SYNTAX</span></span>

### <span data-ttu-id="4abf4-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4abf4-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4abf4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4abf4-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4abf4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4abf4-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4abf4-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4abf4-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4abf4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4abf4-109">DESCRIPTION</span></span>
<span data-ttu-id="4abf4-110">Get-AzNetworkWatcherReachabilityProvidersList, belirli bir Azure bölgesi için kullanılabilir tüm internet hizmeti sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="4abf4-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="4abf4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4abf4-111">EXAMPLES</span></span>

### <span data-ttu-id="4abf4-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4abf4-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="4abf4-113">Istanbul 'daki tüm kullanılabilir sağlayıcıları, Batı ABD 'deki Azure veri merkezi için WA listeler.</span><span class="sxs-lookup"><span data-stu-id="4abf4-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="4abf4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4abf4-114">PARAMETERS</span></span>

### <span data-ttu-id="4abf4-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="4abf4-115">-AsJob</span></span>
<span data-ttu-id="4abf4-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4abf4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4abf4-117">-Şehir</span><span class="sxs-lookup"><span data-stu-id="4abf4-117">-City</span></span>
<span data-ttu-id="4abf4-118">Şehrin adı.</span><span class="sxs-lookup"><span data-stu-id="4abf4-118">The name of the city.</span></span>

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

### <span data-ttu-id="4abf4-119">-Ülke</span><span class="sxs-lookup"><span data-stu-id="4abf4-119">-Country</span></span>
<span data-ttu-id="4abf4-120">Ülkenin adı.</span><span class="sxs-lookup"><span data-stu-id="4abf4-120">The name of the country.</span></span>

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

### <span data-ttu-id="4abf4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abf4-121">-DefaultProfile</span></span>
<span data-ttu-id="4abf4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4abf4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4abf4-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="4abf4-123">-Location</span></span>
<span data-ttu-id="4abf4-124">Sorgunun kapsamını atamak için isteğe bağlı Azure bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="4abf4-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="4abf4-125">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4abf4-125">-NetworkWatcher</span></span>
<span data-ttu-id="4abf4-126">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="4abf4-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="4abf4-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="4abf4-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="4abf4-128">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="4abf4-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4abf4-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4abf4-129">-NetworkWatcherName</span></span>
<span data-ttu-id="4abf4-130">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="4abf4-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="4abf4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abf4-131">-ResourceGroupName</span></span>
<span data-ttu-id="4abf4-132">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4abf4-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4abf4-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4abf4-133">-ResourceId</span></span>
<span data-ttu-id="4abf4-134">Ağ İzleyicisi kaynağının kimliği.</span><span class="sxs-lookup"><span data-stu-id="4abf4-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="4abf4-135">Durumlu</span><span class="sxs-lookup"><span data-stu-id="4abf4-135">-State</span></span>
<span data-ttu-id="4abf4-136">Durumun adı.</span><span class="sxs-lookup"><span data-stu-id="4abf4-136">The name of the state.</span></span>

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

### <span data-ttu-id="4abf4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abf4-137">CommonParameters</span></span>
<span data-ttu-id="4abf4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4abf4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abf4-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4abf4-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abf4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4abf4-140">INPUTS</span></span>

### <span data-ttu-id="4abf4-141">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4abf4-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4abf4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4abf4-142">System.String</span></span>

## <span data-ttu-id="4abf4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4abf4-143">OUTPUTS</span></span>

### <span data-ttu-id="4abf4-144">Microsoft. Azure. Commands. Network. model. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="4abf4-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="4abf4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4abf4-145">NOTES</span></span>
<span data-ttu-id="4abf4-146">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sonraki, atlama</span><span class="sxs-lookup"><span data-stu-id="4abf4-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="4abf4-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4abf4-147">RELATED LINKS</span></span>

[<span data-ttu-id="4abf4-148">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="4abf4-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="4abf4-149">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4abf4-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="4abf4-150">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4abf4-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="4abf4-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4abf4-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="4abf4-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4abf4-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4abf4-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4abf4-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="4abf4-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4abf4-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4abf4-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4abf4-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4abf4-156">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4abf4-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="4abf4-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4abf4-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4abf4-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4abf4-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4abf4-159">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4abf4-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4abf4-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4abf4-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4abf4-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4abf4-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="4abf4-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4abf4-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="4abf4-163">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4abf4-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4abf4-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4abf4-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4abf4-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4abf4-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4abf4-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4abf4-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4abf4-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4abf4-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4abf4-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4abf4-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4abf4-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4abf4-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4abf4-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4abf4-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4abf4-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4abf4-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4abf4-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4abf4-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4abf4-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4abf4-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4abf4-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4abf4-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
