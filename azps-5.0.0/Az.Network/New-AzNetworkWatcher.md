---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 7c8f33d8339bb873b713acabd71ca57fe9107383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323305"
---
# <span data-ttu-id="84451-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84451-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="84451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84451-102">SYNOPSIS</span></span>
<span data-ttu-id="84451-103">Yeni bir ağ Izleyicisi kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84451-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="84451-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84451-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84451-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84451-105">DESCRIPTION</span></span>
<span data-ttu-id="84451-106">New-AzNetworkWatcher cmdlet 'i yeni bir ağ Izleyici kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84451-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="84451-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84451-107">EXAMPLES</span></span>

### <span data-ttu-id="84451-108">Örnek 1: ağ Izleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="84451-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="84451-109">Bu örnek, yeni oluşturulan bir kaynak grubunun içinde yeni bir ağ Izleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="84451-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="84451-110">Her abonelik için bölge başına yalnızca bir ağ Izleyicisi oluşturulabiliriz.</span><span class="sxs-lookup"><span data-stu-id="84451-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="84451-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84451-111">PARAMETERS</span></span>

### <span data-ttu-id="84451-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84451-112">-DefaultProfile</span></span>
<span data-ttu-id="84451-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84451-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84451-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="84451-114">-Location</span></span>
<span data-ttu-id="84451-115">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="84451-115">Location.</span></span>

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

### <span data-ttu-id="84451-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="84451-116">-Name</span></span>
<span data-ttu-id="84451-117">Ağ İzleyici adı.</span><span class="sxs-lookup"><span data-stu-id="84451-117">The network watcher name.</span></span>

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

### <span data-ttu-id="84451-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84451-118">-ResourceGroupName</span></span>
<span data-ttu-id="84451-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="84451-119">The resource group name.</span></span>

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

### <span data-ttu-id="84451-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="84451-120">-Tag</span></span>
<span data-ttu-id="84451-121">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="84451-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="84451-122">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="84451-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="84451-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="84451-123">-Confirm</span></span>
<span data-ttu-id="84451-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84451-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84451-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84451-125">-WhatIf</span></span>
<span data-ttu-id="84451-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84451-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84451-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84451-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84451-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84451-128">CommonParameters</span></span>
<span data-ttu-id="84451-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84451-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84451-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84451-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84451-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84451-131">INPUTS</span></span>

### <span data-ttu-id="84451-132">System. String</span><span class="sxs-lookup"><span data-stu-id="84451-132">System.String</span></span>

### <span data-ttu-id="84451-133">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="84451-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="84451-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84451-134">OUTPUTS</span></span>

### <span data-ttu-id="84451-135">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="84451-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="84451-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84451-136">NOTES</span></span>
<span data-ttu-id="84451-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="84451-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="84451-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84451-138">RELATED LINKS</span></span>

[<span data-ttu-id="84451-139">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="84451-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="84451-140">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="84451-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="84451-141">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="84451-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="84451-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="84451-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="84451-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="84451-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="84451-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="84451-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="84451-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="84451-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="84451-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84451-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84451-147">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="84451-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="84451-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84451-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84451-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84451-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84451-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84451-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84451-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="84451-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="84451-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="84451-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="84451-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="84451-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="84451-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84451-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84451-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84451-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84451-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84451-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84451-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="84451-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="84451-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84451-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84451-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84451-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84451-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="84451-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="84451-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="84451-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="84451-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="84451-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="84451-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="84451-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="84451-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="84451-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="84451-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84451-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
