---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 093a847154c75ee7c640bda522ebf16baa04560a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764985"
---
# <span data-ttu-id="24cc9-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="24cc9-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="24cc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="24cc9-103">Belirtilen bir Azure bölgesi için kullanılabilir tüm internet hizmeti sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="24cc9-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24cc9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24cc9-104">SYNTAX</span></span>

### <span data-ttu-id="24cc9-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="24cc9-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24cc9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="24cc9-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24cc9-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="24cc9-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24cc9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="24cc9-108">DESCRIPTION</span></span>
<span data-ttu-id="24cc9-109">Get-AzureRmNetworkWatcherReachabilityProvidersList, belirli bir Azure bölgesi için kullanılabilir tüm internet hizmeti sağlayıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="24cc9-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="24cc9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24cc9-110">EXAMPLES</span></span>

### <span data-ttu-id="24cc9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="24cc9-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="24cc9-112">Istanbul 'daki tüm kullanılabilir sağlayıcıları, Batı ABD 'deki Azure veri merkezi için WA listeler.</span><span class="sxs-lookup"><span data-stu-id="24cc9-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="24cc9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24cc9-113">PARAMETERS</span></span>

### <span data-ttu-id="24cc9-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="24cc9-114">-AsJob</span></span>
<span data-ttu-id="24cc9-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="24cc9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24cc9-116">-Şehir</span><span class="sxs-lookup"><span data-stu-id="24cc9-116">-City</span></span>
<span data-ttu-id="24cc9-117">Şehrin adı.</span><span class="sxs-lookup"><span data-stu-id="24cc9-117">The name of the city.</span></span>

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

### <span data-ttu-id="24cc9-118">-Ülke</span><span class="sxs-lookup"><span data-stu-id="24cc9-118">-Country</span></span>
<span data-ttu-id="24cc9-119">Ülkenin adı.</span><span class="sxs-lookup"><span data-stu-id="24cc9-119">The name of the country.</span></span>

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

### <span data-ttu-id="24cc9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cc9-120">-DefaultProfile</span></span>
<span data-ttu-id="24cc9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24cc9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24cc9-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="24cc9-122">-Location</span></span>
<span data-ttu-id="24cc9-123">Sorgunun kapsamını atamak için isteğe bağlı Azure bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="24cc9-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="24cc9-124">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="24cc9-124">-NetworkWatcher</span></span>
<span data-ttu-id="24cc9-125">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="24cc9-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="24cc9-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="24cc9-126">-NetworkWatcherName</span></span>
<span data-ttu-id="24cc9-127">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="24cc9-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="24cc9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24cc9-128">-ResourceGroupName</span></span>
<span data-ttu-id="24cc9-129">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="24cc9-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="24cc9-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="24cc9-130">-ResourceId</span></span>
<span data-ttu-id="24cc9-131">Ağ İzleyicisi kaynağının kimliği.</span><span class="sxs-lookup"><span data-stu-id="24cc9-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="24cc9-132">Durumlu</span><span class="sxs-lookup"><span data-stu-id="24cc9-132">-State</span></span>
<span data-ttu-id="24cc9-133">Durumun adı.</span><span class="sxs-lookup"><span data-stu-id="24cc9-133">The name of the state.</span></span>

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

### <span data-ttu-id="24cc9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cc9-134">CommonParameters</span></span>
<span data-ttu-id="24cc9-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24cc9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cc9-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24cc9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cc9-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24cc9-137">INPUTS</span></span>

### <span data-ttu-id="24cc9-138">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="24cc9-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="24cc9-139">System. String System. Koleksiyonlar. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="24cc9-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="24cc9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24cc9-140">OUTPUTS</span></span>

### <span data-ttu-id="24cc9-141">Microsoft. Azure. Commands. Network. model. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="24cc9-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="24cc9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24cc9-142">NOTES</span></span>
<span data-ttu-id="24cc9-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sonraki, atlama</span><span class="sxs-lookup"><span data-stu-id="24cc9-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="24cc9-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24cc9-144">RELATED LINKS</span></span>

[<span data-ttu-id="24cc9-145">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="24cc9-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="24cc9-146">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="24cc9-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="24cc9-147">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="24cc9-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="24cc9-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="24cc9-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="24cc9-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="24cc9-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="24cc9-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="24cc9-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="24cc9-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="24cc9-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="24cc9-152">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24cc9-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24cc9-153">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="24cc9-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="24cc9-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24cc9-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24cc9-155">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24cc9-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="24cc9-156">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="24cc9-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
