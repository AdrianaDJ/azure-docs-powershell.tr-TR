---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: f098e0d776ab115211fb562ed4889502995ffdd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764928"
---
# <span data-ttu-id="c431f-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c431f-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="c431f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c431f-102">SYNOPSIS</span></span>
<span data-ttu-id="c431f-103">Yeni bir ağ Izleyicisi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c431f-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c431f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c431f-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c431f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c431f-105">DESCRIPTION</span></span>
<span data-ttu-id="c431f-106">New-AzureRmNetworkWatcher cmdlet 'i yeni bir ağ Izleyici kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c431f-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="c431f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c431f-107">EXAMPLES</span></span>

### <span data-ttu-id="c431f-108">Örnek 1: ağ Izleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c431f-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="c431f-109">Bu örnek, yeni oluşturulan bir kaynak grubunun içinde yeni bir ağ Izleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c431f-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="c431f-110">Her abonelik için bölge başına yalnızca bir ağ Izleyicisi oluşturulabiliriz.</span><span class="sxs-lookup"><span data-stu-id="c431f-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="c431f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c431f-111">PARAMETERS</span></span>

### <span data-ttu-id="c431f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c431f-112">-DefaultProfile</span></span>
<span data-ttu-id="c431f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c431f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c431f-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="c431f-114">-Location</span></span>
<span data-ttu-id="c431f-115">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="c431f-115">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c431f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c431f-116">-Name</span></span>
<span data-ttu-id="c431f-117">Ağ İzleyici adı.</span><span class="sxs-lookup"><span data-stu-id="c431f-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c431f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c431f-118">-ResourceGroupName</span></span>
<span data-ttu-id="c431f-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c431f-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c431f-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c431f-120">-Tag</span></span>
<span data-ttu-id="c431f-121">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="c431f-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c431f-122">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c431f-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c431f-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c431f-123">-Confirm</span></span>
<span data-ttu-id="c431f-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c431f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c431f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c431f-125">-WhatIf</span></span>
<span data-ttu-id="c431f-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c431f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c431f-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c431f-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c431f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c431f-128">CommonParameters</span></span>
<span data-ttu-id="c431f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c431f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c431f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c431f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c431f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c431f-131">INPUTS</span></span>

### <span data-ttu-id="c431f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c431f-132">System.String</span></span>

### <span data-ttu-id="c431f-133">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c431f-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c431f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c431f-134">OUTPUTS</span></span>

### <span data-ttu-id="c431f-135">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c431f-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="c431f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c431f-136">NOTES</span></span>
<span data-ttu-id="c431f-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="c431f-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="c431f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c431f-138">RELATED LINKS</span></span>

[<span data-ttu-id="c431f-139">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c431f-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c431f-140">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c431f-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c431f-141">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="c431f-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c431f-142">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c431f-142">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c431f-143">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c431f-143">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c431f-144">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c431f-144">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c431f-145">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c431f-145">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c431f-146">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c431f-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c431f-147">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c431f-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c431f-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c431f-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c431f-149">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c431f-149">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c431f-150">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c431f-150">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c431f-151">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c431f-151">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c431f-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c431f-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c431f-153">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c431f-153">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="c431f-154">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c431f-154">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c431f-155">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c431f-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c431f-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c431f-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c431f-157">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c431f-157">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c431f-158">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c431f-158">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c431f-159">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c431f-159">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c431f-160">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c431f-160">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c431f-161">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c431f-161">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c431f-162">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c431f-162">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c431f-163">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c431f-163">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c431f-164">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c431f-164">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c431f-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c431f-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
