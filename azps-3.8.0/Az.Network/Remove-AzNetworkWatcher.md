---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 7723d717a35f4c5e3e693bc5ff115b484df5fa2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104064"
---
# <span data-ttu-id="cbcf0-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbcf0-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="cbcf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbcf0-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcf0-103">Ağ Izleyicisi 'Ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="cbcf0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbcf0-104">SYNTAX</span></span>

### <span data-ttu-id="cbcf0-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cbcf0-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbcf0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cbcf0-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbcf0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cbcf0-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbcf0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbcf0-108">DESCRIPTION</span></span>
<span data-ttu-id="cbcf0-109">Remove-AzNetworkWatcher cmdlet 'i ağ Izleyicisi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="cbcf0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbcf0-110">EXAMPLES</span></span>

### <span data-ttu-id="cbcf0-111">Örnek 1: ağ Izleyicisi oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="cbcf0-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="cbcf0-112">Bu örnekte, kaynak grubunda bir ağ Izleyicisi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="cbcf0-113">Her abonelik için bölge başına yalnızca bir ağ Izleyicisi oluşturulabiliriz.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="cbcf0-114">Sanal ağı silerken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="cbcf0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbcf0-115">PARAMETERS</span></span>

### <span data-ttu-id="cbcf0-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="cbcf0-116">-AsJob</span></span>
<span data-ttu-id="cbcf0-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cbcf0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbcf0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcf0-118">-DefaultProfile</span></span>
<span data-ttu-id="cbcf0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbcf0-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="cbcf0-120">-Location</span></span>
<span data-ttu-id="cbcf0-121">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cbcf0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="cbcf0-122">-Name</span></span>
<span data-ttu-id="cbcf0-123">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcf0-124">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cbcf0-124">-NetworkWatcher</span></span>
<span data-ttu-id="cbcf0-125">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="cbcf0-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cbcf0-126">-PassThru</span></span>
<span data-ttu-id="cbcf0-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-127">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbcf0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcf0-128">-ResourceGroupName</span></span>
<span data-ttu-id="cbcf0-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbcf0-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="cbcf0-130">-Confirm</span></span>
<span data-ttu-id="cbcf0-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbcf0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbcf0-132">-WhatIf</span></span>
<span data-ttu-id="cbcf0-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbcf0-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbcf0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcf0-135">CommonParameters</span></span>
<span data-ttu-id="cbcf0-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbcf0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcf0-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbcf0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcf0-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbcf0-138">INPUTS</span></span>

### <span data-ttu-id="cbcf0-139">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cbcf0-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cbcf0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cbcf0-140">System.String</span></span>

## <span data-ttu-id="cbcf0-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbcf0-141">OUTPUTS</span></span>

### <span data-ttu-id="cbcf0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cbcf0-142">System.Boolean</span></span>

## <span data-ttu-id="cbcf0-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbcf0-143">NOTES</span></span>
<span data-ttu-id="cbcf0-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="cbcf0-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="cbcf0-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbcf0-145">RELATED LINKS</span></span>

[<span data-ttu-id="cbcf0-146">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="cbcf0-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cbcf0-147">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cbcf0-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cbcf0-148">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="cbcf0-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cbcf0-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cbcf0-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cbcf0-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cbcf0-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cbcf0-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cbcf0-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cbcf0-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cbcf0-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cbcf0-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbcf0-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbcf0-154">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cbcf0-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cbcf0-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbcf0-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbcf0-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbcf0-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbcf0-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbcf0-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbcf0-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbcf0-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cbcf0-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cbcf0-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cbcf0-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cbcf0-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="cbcf0-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbcf0-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbcf0-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbcf0-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbcf0-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbcf0-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbcf0-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cbcf0-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cbcf0-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbcf0-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbcf0-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbcf0-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbcf0-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cbcf0-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cbcf0-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cbcf0-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cbcf0-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cbcf0-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cbcf0-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cbcf0-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cbcf0-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cbcf0-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="cbcf0-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbcf0-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
