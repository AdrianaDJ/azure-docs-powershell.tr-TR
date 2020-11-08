---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: b096c87e588c48b609fe0a55be7344b39df98c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939513"
---
# <span data-ttu-id="dbebc-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dbebc-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="dbebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbebc-102">SYNOPSIS</span></span>
<span data-ttu-id="dbebc-103">Yeni bir ağ Izleyicisi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbebc-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbebc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbebc-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbebc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbebc-105">DESCRIPTION</span></span>
<span data-ttu-id="dbebc-106">New-AzureRmNetworkWatcher cmdlet 'i yeni bir ağ Izleyici kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbebc-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="dbebc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbebc-107">EXAMPLES</span></span>

### <span data-ttu-id="dbebc-108">Örnek 1: ağ Izleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dbebc-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="dbebc-109">Bu örnek, yeni oluşturulan bir kaynak grubunun içinde yeni bir ağ Izleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbebc-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="dbebc-110">Her abonelik için bölge başına yalnızca bir ağ Izleyicisi oluşturulabiliriz.</span><span class="sxs-lookup"><span data-stu-id="dbebc-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="dbebc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbebc-111">PARAMETERS</span></span>

### <span data-ttu-id="dbebc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbebc-112">-DefaultProfile</span></span>
<span data-ttu-id="dbebc-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbebc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbebc-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="dbebc-114">-Location</span></span>
<span data-ttu-id="dbebc-115">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="dbebc-115">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbebc-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="dbebc-116">-Name</span></span>
<span data-ttu-id="dbebc-117">Ağ İzleyici adı.</span><span class="sxs-lookup"><span data-stu-id="dbebc-117">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbebc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbebc-118">-ResourceGroupName</span></span>
<span data-ttu-id="dbebc-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dbebc-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbebc-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dbebc-120">-Tag</span></span>
<span data-ttu-id="dbebc-121">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="dbebc-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dbebc-122">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="dbebc-122">For example:</span></span>

<span data-ttu-id="dbebc-123">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="dbebc-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbebc-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="dbebc-124">-Confirm</span></span>
<span data-ttu-id="dbebc-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dbebc-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbebc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbebc-126">-WhatIf</span></span>
<span data-ttu-id="dbebc-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dbebc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbebc-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dbebc-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbebc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbebc-129">CommonParameters</span></span>
<span data-ttu-id="dbebc-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbebc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbebc-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbebc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbebc-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbebc-132">INPUTS</span></span>

### <span data-ttu-id="dbebc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dbebc-133">System.String</span></span>
<span data-ttu-id="dbebc-134">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dbebc-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dbebc-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbebc-135">OUTPUTS</span></span>

### <span data-ttu-id="dbebc-136">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="dbebc-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="dbebc-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbebc-137">NOTES</span></span>
<span data-ttu-id="dbebc-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="dbebc-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="dbebc-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbebc-139">RELATED LINKS</span></span>

[<span data-ttu-id="dbebc-140">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="dbebc-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dbebc-141">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="dbebc-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dbebc-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbebc-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbebc-143">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dbebc-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="dbebc-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbebc-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbebc-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbebc-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbebc-146">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dbebc-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dbebc-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dbebc-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="dbebc-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dbebc-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="dbebc-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dbebc-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dbebc-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dbebc-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="dbebc-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dbebc-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)