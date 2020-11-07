---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935505"
---
# <span data-ttu-id="b2533-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b2533-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="b2533-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2533-102">SYNOPSIS</span></span>
<span data-ttu-id="b2533-103">Belirtilen bir Azure bölgesi için kullanılabilir tüm internet hizmeti sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b2533-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="b2533-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2533-104">SYNTAX</span></span>

### <span data-ttu-id="b2533-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2533-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2533-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b2533-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2533-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b2533-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2533-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2533-108">DESCRIPTION</span></span>
<span data-ttu-id="b2533-109">Get-AzNetworkWatcherReachabilityProvidersList, belirli bir Azure bölgesi için kullanılabilir tüm internet hizmeti sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="b2533-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="b2533-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2533-110">EXAMPLES</span></span>

### <span data-ttu-id="b2533-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b2533-111">Example 1</span></span>
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

<span data-ttu-id="b2533-112">Istanbul 'daki tüm kullanılabilir sağlayıcıları, Batı ABD 'deki Azure veri merkezi için WA listeler.</span><span class="sxs-lookup"><span data-stu-id="b2533-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="b2533-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2533-113">PARAMETERS</span></span>

### <span data-ttu-id="b2533-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b2533-114">-AsJob</span></span>
<span data-ttu-id="b2533-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b2533-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2533-116">-Şehir</span><span class="sxs-lookup"><span data-stu-id="b2533-116">-City</span></span>
<span data-ttu-id="b2533-117">Şehrin adı.</span><span class="sxs-lookup"><span data-stu-id="b2533-117">The name of the city.</span></span>

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

### <span data-ttu-id="b2533-118">-Ülke</span><span class="sxs-lookup"><span data-stu-id="b2533-118">-Country</span></span>
<span data-ttu-id="b2533-119">Ülkenin adı.</span><span class="sxs-lookup"><span data-stu-id="b2533-119">The name of the country.</span></span>

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

### <span data-ttu-id="b2533-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2533-120">-DefaultProfile</span></span>
<span data-ttu-id="b2533-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2533-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2533-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="b2533-122">-Location</span></span>
<span data-ttu-id="b2533-123">Sorgunun kapsamını atamak için isteğe bağlı Azure bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="b2533-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="b2533-124">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b2533-124">-NetworkWatcher</span></span>
<span data-ttu-id="b2533-125">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="b2533-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="b2533-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b2533-126">-NetworkWatcherName</span></span>
<span data-ttu-id="b2533-127">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="b2533-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="b2533-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2533-128">-ResourceGroupName</span></span>
<span data-ttu-id="b2533-129">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b2533-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b2533-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b2533-130">-ResourceId</span></span>
<span data-ttu-id="b2533-131">Ağ İzleyicisi kaynağının kimliği.</span><span class="sxs-lookup"><span data-stu-id="b2533-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="b2533-132">Durumlu</span><span class="sxs-lookup"><span data-stu-id="b2533-132">-State</span></span>
<span data-ttu-id="b2533-133">Durumun adı.</span><span class="sxs-lookup"><span data-stu-id="b2533-133">The name of the state.</span></span>

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

### <span data-ttu-id="b2533-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2533-134">CommonParameters</span></span>
<span data-ttu-id="b2533-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2533-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2533-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2533-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2533-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2533-137">INPUTS</span></span>

### <span data-ttu-id="b2533-138">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b2533-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b2533-139">System. String System. Koleksiyonlar. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b2533-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b2533-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2533-140">OUTPUTS</span></span>

### <span data-ttu-id="b2533-141">Microsoft. Azure. Commands. Network. model. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="b2533-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="b2533-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2533-142">NOTES</span></span>
<span data-ttu-id="b2533-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sonraki, atlama</span><span class="sxs-lookup"><span data-stu-id="b2533-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="b2533-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2533-144">RELATED LINKS</span></span>

[<span data-ttu-id="b2533-145">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="b2533-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b2533-146">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b2533-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b2533-147">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="b2533-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b2533-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b2533-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b2533-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b2533-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b2533-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b2533-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b2533-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b2533-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b2533-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2533-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2533-153">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b2533-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b2533-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2533-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2533-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2533-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b2533-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2533-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
