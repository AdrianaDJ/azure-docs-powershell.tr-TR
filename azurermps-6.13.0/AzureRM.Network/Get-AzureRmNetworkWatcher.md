---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: c8417f8a1f1d16e00629d06a75be2802801afd2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765090"
---
# <span data-ttu-id="32299-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32299-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="32299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32299-102">SYNOPSIS</span></span>
<span data-ttu-id="32299-103">Ağ Izleyicisi özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="32299-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32299-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32299-104">SYNTAX</span></span>

### <span data-ttu-id="32299-105">Al</span><span class="sxs-lookup"><span data-stu-id="32299-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32299-106">Listeniz</span><span class="sxs-lookup"><span data-stu-id="32299-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32299-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="32299-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32299-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="32299-108">DESCRIPTION</span></span>
<span data-ttu-id="32299-109">Get-AzureRmNetworkWatcher cmdlet bir veya birden çok Azure ağ Izleyicisi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="32299-109">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="32299-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32299-110">EXAMPLES</span></span>

### <span data-ttu-id="32299-111">Örnek 1: ağ Izleyicisi alma</span><span class="sxs-lookup"><span data-stu-id="32299-111">Example 1: Get a Network Watcher</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="32299-112">NetworkWatcherRG kaynak grubundaki ağ Izleyicisi NetworkWatcher_westcentralus 'Ni alır.</span><span class="sxs-lookup"><span data-stu-id="32299-112">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="32299-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32299-113">PARAMETERS</span></span>

### <span data-ttu-id="32299-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32299-114">-DefaultProfile</span></span>
<span data-ttu-id="32299-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32299-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32299-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="32299-116">-Location</span></span>
<span data-ttu-id="32299-117">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="32299-117">Location of the network watcher.</span></span>

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

### <span data-ttu-id="32299-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="32299-118">-Name</span></span>
<span data-ttu-id="32299-119">Ağ İzleyici adı.</span><span class="sxs-lookup"><span data-stu-id="32299-119">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32299-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32299-120">-ResourceGroupName</span></span>
<span data-ttu-id="32299-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="32299-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32299-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32299-122">CommonParameters</span></span>
<span data-ttu-id="32299-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32299-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32299-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32299-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32299-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32299-125">INPUTS</span></span>

### <span data-ttu-id="32299-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="32299-126">None</span></span>

## <span data-ttu-id="32299-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32299-127">OUTPUTS</span></span>

### <span data-ttu-id="32299-128">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="32299-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="32299-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32299-129">NOTES</span></span>
<span data-ttu-id="32299-130">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="32299-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="32299-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32299-131">RELATED LINKS</span></span>

[<span data-ttu-id="32299-132">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="32299-132">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="32299-133">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="32299-133">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="32299-134">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="32299-134">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="32299-135">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="32299-135">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="32299-136">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="32299-136">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="32299-137">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="32299-137">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="32299-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="32299-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="32299-139">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32299-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32299-140">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="32299-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="32299-141">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32299-141">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32299-142">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32299-142">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32299-143">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32299-143">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32299-144">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="32299-144">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="32299-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="32299-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="32299-146">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="32299-146">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="32299-147">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32299-147">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32299-148">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32299-148">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32299-149">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32299-149">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32299-150">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="32299-150">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="32299-151">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32299-151">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32299-152">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32299-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="32299-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="32299-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="32299-154">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="32299-154">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="32299-155">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="32299-155">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="32299-156">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="32299-156">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="32299-157">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="32299-157">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="32299-158">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="32299-158">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
