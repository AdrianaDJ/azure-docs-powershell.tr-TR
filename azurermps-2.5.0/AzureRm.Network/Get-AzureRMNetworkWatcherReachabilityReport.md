---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
ms.openlocfilehash: 75335fb09bb8f4187879ab69ab138952cc873993
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940107"
---
# <span data-ttu-id="842a2-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="842a2-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="842a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="842a2-102">SYNOPSIS</span></span>
<span data-ttu-id="842a2-103">Belirtilen konumdan Azure bölgelerine Internet servis sağlayıcılarının göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="842a2-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="842a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="842a2-104">SYNTAX</span></span>

### <span data-ttu-id="842a2-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="842a2-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="842a2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="842a2-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="842a2-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="842a2-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="842a2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="842a2-108">DESCRIPTION</span></span>
<span data-ttu-id="842a2-109">Get-AzureRmNetworkWatcherReachabilityReport, Internet servis sağlayıcılarının belirli bir konumdan Azure bölgelerine göreli gecikme süresini alır.</span><span class="sxs-lookup"><span data-stu-id="842a2-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="842a2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="842a2-110">EXAMPLES</span></span>

### <span data-ttu-id="842a2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="842a2-111">Example 1</span></span>
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

<span data-ttu-id="842a2-112">ABD 'deki 2017-10-10 'dan 2017-10-12 'a kadar Batı ABD 'deki Azure veri merkezi 'ne göreli gecikmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="842a2-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="842a2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="842a2-113">PARAMETERS</span></span>

### <span data-ttu-id="842a2-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="842a2-114">-AsJob</span></span>
<span data-ttu-id="842a2-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="842a2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="842a2-116">-Şehir</span><span class="sxs-lookup"><span data-stu-id="842a2-116">-City</span></span>
<span data-ttu-id="842a2-117">Şehrin adı.</span><span class="sxs-lookup"><span data-stu-id="842a2-117">The name of the city.</span></span>

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

### <span data-ttu-id="842a2-118">-Ülke</span><span class="sxs-lookup"><span data-stu-id="842a2-118">-Country</span></span>
<span data-ttu-id="842a2-119">Ülkenin adı.</span><span class="sxs-lookup"><span data-stu-id="842a2-119">The name of the country.</span></span>

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

### <span data-ttu-id="842a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="842a2-120">-DefaultProfile</span></span>
<span data-ttu-id="842a2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="842a2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="842a2-122">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="842a2-122">-EndTime</span></span>
<span data-ttu-id="842a2-123">Azure erişilebilirlik raporu için bitiş saati.</span><span class="sxs-lookup"><span data-stu-id="842a2-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="842a2-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="842a2-124">-Location</span></span>
<span data-ttu-id="842a2-125">Sorgunun kapsamını atamak için isteğe bağlı Azure bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="842a2-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="842a2-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="842a2-126">-NetworkWatcher</span></span>
<span data-ttu-id="842a2-127">Ağ İzleyicisi kaynağı</span><span class="sxs-lookup"><span data-stu-id="842a2-127">The network watcher resource</span></span>

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

### <span data-ttu-id="842a2-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="842a2-128">-NetworkWatcherName</span></span>
<span data-ttu-id="842a2-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="842a2-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="842a2-130">-Sağlayıcı</span><span class="sxs-lookup"><span data-stu-id="842a2-130">-Provider</span></span>
<span data-ttu-id="842a2-131">Internet hizmet sağlayıcılarının listesi.</span><span class="sxs-lookup"><span data-stu-id="842a2-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="842a2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="842a2-132">-ResourceGroupName</span></span>
<span data-ttu-id="842a2-133">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="842a2-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="842a2-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="842a2-134">-ResourceId</span></span>
<span data-ttu-id="842a2-135">Ağ İzleyicisi kaynağının kimliği.</span><span class="sxs-lookup"><span data-stu-id="842a2-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="842a2-136">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="842a2-136">-StartTime</span></span>
<span data-ttu-id="842a2-137">Azure erişilebilirlik raporu için başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="842a2-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="842a2-138">Durumlu</span><span class="sxs-lookup"><span data-stu-id="842a2-138">-State</span></span>
<span data-ttu-id="842a2-139">Durumun adı.</span><span class="sxs-lookup"><span data-stu-id="842a2-139">The name of the state.</span></span>

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

### <span data-ttu-id="842a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="842a2-140">CommonParameters</span></span>
<span data-ttu-id="842a2-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="842a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="842a2-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="842a2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="842a2-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="842a2-143">INPUTS</span></span>

### <span data-ttu-id="842a2-144">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="842a2-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="842a2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="842a2-145">System.String</span></span>

## <span data-ttu-id="842a2-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="842a2-146">OUTPUTS</span></span>

### <span data-ttu-id="842a2-147">Microsoft. Azure. Commands. Network. model. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="842a2-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="842a2-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="842a2-148">NOTES</span></span>
<span data-ttu-id="842a2-149">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, erişilebilirlik, rapor</span><span class="sxs-lookup"><span data-stu-id="842a2-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="842a2-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="842a2-150">RELATED LINKS</span></span>

[<span data-ttu-id="842a2-151">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="842a2-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="842a2-152">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="842a2-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="842a2-153">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="842a2-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="842a2-154">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="842a2-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="842a2-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="842a2-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="842a2-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="842a2-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="842a2-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="842a2-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="842a2-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="842a2-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="842a2-159">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="842a2-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="842a2-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="842a2-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="842a2-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="842a2-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="842a2-162">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="842a2-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
