---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: cace33dd9831dcfcc01f2a57eefb5f28367966d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935371"
---
# <span data-ttu-id="8a6d7-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8a6d7-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="8a6d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6d7-103">Yeni bir ağ Izleyicisi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8a6d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a6d7-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a6d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a6d7-105">DESCRIPTION</span></span>
<span data-ttu-id="8a6d7-106">New-AzNetworkWatcher cmdlet 'i yeni bir ağ Izleyici kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8a6d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a6d7-107">EXAMPLES</span></span>

### <span data-ttu-id="8a6d7-108">Örnek 1: ağ Izleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8a6d7-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="8a6d7-109">Bu örnek, yeni oluşturulan bir kaynak grubunun içinde yeni bir ağ Izleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="8a6d7-110">Her abonelik için bölge başına yalnızca bir ağ Izleyicisi oluşturulabiliriz.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="8a6d7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a6d7-111">PARAMETERS</span></span>

### <span data-ttu-id="8a6d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6d7-112">-DefaultProfile</span></span>
<span data-ttu-id="8a6d7-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a6d7-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="8a6d7-114">-Location</span></span>
<span data-ttu-id="8a6d7-115">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-115">Location.</span></span>

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

### <span data-ttu-id="8a6d7-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a6d7-116">-Name</span></span>
<span data-ttu-id="8a6d7-117">Ağ İzleyici adı.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-117">The network watcher name.</span></span>

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

### <span data-ttu-id="8a6d7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6d7-118">-ResourceGroupName</span></span>
<span data-ttu-id="8a6d7-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-119">The resource group name.</span></span>

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

### <span data-ttu-id="8a6d7-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8a6d7-120">-Tag</span></span>
<span data-ttu-id="8a6d7-121">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8a6d7-122">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="8a6d7-122">For example:</span></span>

<span data-ttu-id="8a6d7-123">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="8a6d7-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8a6d7-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a6d7-124">-Confirm</span></span>
<span data-ttu-id="8a6d7-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a6d7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a6d7-126">-WhatIf</span></span>
<span data-ttu-id="8a6d7-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a6d7-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a6d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6d7-129">CommonParameters</span></span>
<span data-ttu-id="8a6d7-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6d7-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a6d7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6d7-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a6d7-132">INPUTS</span></span>

### <span data-ttu-id="8a6d7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8a6d7-133">System.String</span></span>
<span data-ttu-id="8a6d7-134">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8a6d7-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8a6d7-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a6d7-135">OUTPUTS</span></span>

### <span data-ttu-id="8a6d7-136">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8a6d7-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="8a6d7-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a6d7-137">NOTES</span></span>
<span data-ttu-id="8a6d7-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="8a6d7-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="8a6d7-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a6d7-139">RELATED LINKS</span></span>

[<span data-ttu-id="8a6d7-140">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8a6d7-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8a6d7-141">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="8a6d7-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8a6d7-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a6d7-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a6d7-143">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8a6d7-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8a6d7-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a6d7-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a6d7-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a6d7-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a6d7-146">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a6d7-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8a6d7-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8a6d7-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8a6d7-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8a6d7-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8a6d7-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8a6d7-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8a6d7-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8a6d7-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8a6d7-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8a6d7-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
