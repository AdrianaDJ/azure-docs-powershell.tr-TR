---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935503"
---
# <span data-ttu-id="d2be9-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d2be9-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="d2be9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2be9-102">SYNOPSIS</span></span>
<span data-ttu-id="d2be9-103">Belirtilen konumdan Azure bölgelerine Internet servis sağlayıcılarının göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="d2be9-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="d2be9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2be9-104">SYNTAX</span></span>

### <span data-ttu-id="d2be9-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2be9-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2be9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d2be9-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2be9-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d2be9-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2be9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2be9-108">DESCRIPTION</span></span>
<span data-ttu-id="d2be9-109">Get-AzNetworkWatcherReachabilityReport, Internet servis sağlayıcılarının belirli bir konumdan Azure bölgelerine göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="d2be9-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="d2be9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2be9-110">EXAMPLES</span></span>

### <span data-ttu-id="d2be9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2be9-111">Example 1</span></span>
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

<span data-ttu-id="d2be9-112">ABD 'deki 2017-10-10 'dan 2017-10-12 'a kadar Batı ABD 'deki Azure veri merkezi 'ne göreli gecikmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="d2be9-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="d2be9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2be9-113">PARAMETERS</span></span>

### <span data-ttu-id="d2be9-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d2be9-114">-AsJob</span></span>
<span data-ttu-id="d2be9-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d2be9-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2be9-116">-Şehir</span><span class="sxs-lookup"><span data-stu-id="d2be9-116">-City</span></span>
<span data-ttu-id="d2be9-117">Şehrin adı.</span><span class="sxs-lookup"><span data-stu-id="d2be9-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2be9-118">-Ülke</span><span class="sxs-lookup"><span data-stu-id="d2be9-118">-Country</span></span>
<span data-ttu-id="d2be9-119">Ülkenin adı.</span><span class="sxs-lookup"><span data-stu-id="d2be9-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2be9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2be9-120">-DefaultProfile</span></span>
<span data-ttu-id="d2be9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2be9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2be9-122">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="d2be9-122">-EndTime</span></span>
<span data-ttu-id="d2be9-123">Azure erişilebilirlik raporu için bitiş saati.</span><span class="sxs-lookup"><span data-stu-id="d2be9-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2be9-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="d2be9-124">-Location</span></span>
<span data-ttu-id="d2be9-125">Sorgunun kapsamını atamak için isteğe bağlı Azure bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="d2be9-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="d2be9-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d2be9-126">-NetworkWatcher</span></span>
<span data-ttu-id="d2be9-127">Ağ İzleyicisi kaynağı</span><span class="sxs-lookup"><span data-stu-id="d2be9-127">The network watcher resource</span></span>

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

### <span data-ttu-id="d2be9-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d2be9-128">-NetworkWatcherName</span></span>
<span data-ttu-id="d2be9-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="d2be9-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2be9-130">-Sağlayıcı</span><span class="sxs-lookup"><span data-stu-id="d2be9-130">-Provider</span></span>
<span data-ttu-id="d2be9-131">Internet hizmet sağlayıcılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="d2be9-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="d2be9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2be9-132">-ResourceGroupName</span></span>
<span data-ttu-id="d2be9-133">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d2be9-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d2be9-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d2be9-134">-ResourceId</span></span>
<span data-ttu-id="d2be9-135">Ağ İzleyicisi kaynağının kimliği.</span><span class="sxs-lookup"><span data-stu-id="d2be9-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="d2be9-136">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="d2be9-136">-StartTime</span></span>
<span data-ttu-id="d2be9-137">Azure erişilebilirlik raporu için başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="d2be9-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2be9-138">Durumlu</span><span class="sxs-lookup"><span data-stu-id="d2be9-138">-State</span></span>
<span data-ttu-id="d2be9-139">Durumun adı.</span><span class="sxs-lookup"><span data-stu-id="d2be9-139">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2be9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2be9-140">CommonParameters</span></span>
<span data-ttu-id="d2be9-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2be9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2be9-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2be9-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2be9-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2be9-143">INPUTS</span></span>

### <span data-ttu-id="d2be9-144">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d2be9-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d2be9-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d2be9-145">System.String</span></span>

## <span data-ttu-id="d2be9-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2be9-146">OUTPUTS</span></span>

### <span data-ttu-id="d2be9-147">Microsoft. Azure. Commands. Network. model. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d2be9-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="d2be9-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2be9-148">NOTES</span></span>
<span data-ttu-id="d2be9-149">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, erişilebilirlik, rapor</span><span class="sxs-lookup"><span data-stu-id="d2be9-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="d2be9-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2be9-150">RELATED LINKS</span></span>

[<span data-ttu-id="d2be9-151">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="d2be9-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d2be9-152">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d2be9-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d2be9-153">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d2be9-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d2be9-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d2be9-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d2be9-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d2be9-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d2be9-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d2be9-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d2be9-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d2be9-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d2be9-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2be9-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2be9-159">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d2be9-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d2be9-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2be9-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2be9-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2be9-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d2be9-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d2be9-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
