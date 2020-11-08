---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 9906af7da12f76650ebbe45ff764da78c90ef340
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265924"
---
# <span data-ttu-id="10c57-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="10c57-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="10c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10c57-102">SYNOPSIS</span></span>
<span data-ttu-id="10c57-103">Belirtilen akış günlüğü kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="10c57-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="10c57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10c57-104">SYNTAX</span></span>

### <span data-ttu-id="10c57-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="10c57-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c57-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="10c57-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c57-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="10c57-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c57-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="10c57-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c57-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="10c57-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10c57-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="10c57-110">DESCRIPTION</span></span>
<span data-ttu-id="10c57-111">Belirtilen akış günlüğü kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="10c57-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="10c57-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10c57-112">EXAMPLES</span></span>

### <span data-ttu-id="10c57-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="10c57-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="10c57-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10c57-114">PARAMETERS</span></span>

### <span data-ttu-id="10c57-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="10c57-115">-AsJob</span></span>
<span data-ttu-id="10c57-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="10c57-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10c57-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c57-117">-DefaultProfile</span></span>
<span data-ttu-id="10c57-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10c57-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c57-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10c57-119">-InputObject</span></span>
<span data-ttu-id="10c57-120">Akış günlüğü nesnesi.</span><span class="sxs-lookup"><span data-stu-id="10c57-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10c57-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="10c57-121">-Location</span></span>
<span data-ttu-id="10c57-122">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="10c57-122">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c57-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="10c57-123">-Name</span></span>
<span data-ttu-id="10c57-124">Akış günlüğü adı.</span><span class="sxs-lookup"><span data-stu-id="10c57-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c57-125">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="10c57-125">-NetworkWatcher</span></span>
<span data-ttu-id="10c57-126">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="10c57-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="10c57-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="10c57-127">-NetworkWatcherName</span></span>
<span data-ttu-id="10c57-128">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="10c57-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="10c57-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="10c57-129">-PassThru</span></span>
<span data-ttu-id="10c57-130">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="10c57-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="10c57-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c57-131">-ResourceGroupName</span></span>
<span data-ttu-id="10c57-132">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="10c57-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="10c57-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="10c57-133">-ResourceId</span></span>
<span data-ttu-id="10c57-134">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="10c57-134">Resource ID.</span></span>

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

### <span data-ttu-id="10c57-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="10c57-135">-Confirm</span></span>
<span data-ttu-id="10c57-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="10c57-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c57-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c57-137">-WhatIf</span></span>
<span data-ttu-id="10c57-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10c57-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10c57-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="10c57-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c57-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c57-140">CommonParameters</span></span>
<span data-ttu-id="10c57-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10c57-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c57-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="10c57-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c57-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10c57-143">INPUTS</span></span>

### <span data-ttu-id="10c57-144">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="10c57-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="10c57-145">System. String</span><span class="sxs-lookup"><span data-stu-id="10c57-145">System.String</span></span>

### <span data-ttu-id="10c57-146">Microsoft. Azure. Commands. Network. model. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="10c57-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="10c57-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10c57-147">OUTPUTS</span></span>

### <span data-ttu-id="10c57-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10c57-148">System.Boolean</span></span>

## <span data-ttu-id="10c57-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10c57-149">NOTES</span></span>

## <span data-ttu-id="10c57-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10c57-150">RELATED LINKS</span></span>

[<span data-ttu-id="10c57-151">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="10c57-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="10c57-152">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="10c57-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="10c57-153">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="10c57-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="10c57-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="10c57-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="10c57-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="10c57-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="10c57-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="10c57-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="10c57-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="10c57-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="10c57-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="10c57-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="10c57-159">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="10c57-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="10c57-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="10c57-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="10c57-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="10c57-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="10c57-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="10c57-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="10c57-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="10c57-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="10c57-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="10c57-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="10c57-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="10c57-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="10c57-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="10c57-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="10c57-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="10c57-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="10c57-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="10c57-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="10c57-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="10c57-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="10c57-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="10c57-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="10c57-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="10c57-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="10c57-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="10c57-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="10c57-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="10c57-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="10c57-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="10c57-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="10c57-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="10c57-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="10c57-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="10c57-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="10c57-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="10c57-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="10c57-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="10c57-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="10c57-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="10c57-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="10c57-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="10c57-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)
