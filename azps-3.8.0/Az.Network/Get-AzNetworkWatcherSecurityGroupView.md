---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 01334e8a94ad4f73ec5f347748468bada119c070
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937674"
---
# <span data-ttu-id="aed80-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="aed80-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="aed80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aed80-102">SYNOPSIS</span></span>
<span data-ttu-id="aed80-103">VM 'ye uygulanan yapılandırılmış ve etkin ağ güvenlik grubu kurallarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="aed80-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="aed80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aed80-104">SYNTAX</span></span>

### <span data-ttu-id="aed80-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aed80-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed80-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="aed80-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aed80-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="aed80-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aed80-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aed80-108">DESCRIPTION</span></span>
<span data-ttu-id="aed80-109">Get-AzNetworkWatcherSecurityGroupView, VM 'ye uygulanan yapılandırılmış ve etkili ağ güvenlik grubu kurallarını görüntülemenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="aed80-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="aed80-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aed80-110">EXAMPLES</span></span>

### <span data-ttu-id="aed80-111">Örnek 1: bir VM 'de güvenlik grubu görünümü araması yapma</span><span class="sxs-lookup"><span data-stu-id="aed80-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="aed80-112">Yukarıdaki örnekte, önce bölgesel ağ Izleyicisi 'ni, ardından bölgedeki bir VM 'yi ediniyoruz.</span><span class="sxs-lookup"><span data-stu-id="aed80-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="aed80-113">Ardından belirtilen VM 'de bir güvenlik grubu görünümü araması yaptık.</span><span class="sxs-lookup"><span data-stu-id="aed80-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="aed80-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aed80-114">PARAMETERS</span></span>

### <span data-ttu-id="aed80-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="aed80-115">-AsJob</span></span>
<span data-ttu-id="aed80-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="aed80-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aed80-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed80-117">-DefaultProfile</span></span>
<span data-ttu-id="aed80-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aed80-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aed80-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="aed80-119">-Location</span></span>
<span data-ttu-id="aed80-120">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="aed80-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="aed80-121">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="aed80-121">-NetworkWatcher</span></span>
<span data-ttu-id="aed80-122">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="aed80-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="aed80-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="aed80-123">-NetworkWatcherName</span></span>
<span data-ttu-id="aed80-124">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="aed80-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aed80-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed80-125">-ResourceGroupName</span></span>
<span data-ttu-id="aed80-126">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="aed80-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="aed80-127">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="aed80-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="aed80-128">Hedef VM kimliği</span><span class="sxs-lookup"><span data-stu-id="aed80-128">The target VM Id</span></span>

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

### <span data-ttu-id="aed80-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed80-129">CommonParameters</span></span>
<span data-ttu-id="aed80-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aed80-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aed80-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aed80-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed80-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aed80-132">INPUTS</span></span>

### <span data-ttu-id="aed80-133">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="aed80-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="aed80-134">System. String</span><span class="sxs-lookup"><span data-stu-id="aed80-134">System.String</span></span>

## <span data-ttu-id="aed80-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aed80-135">OUTPUTS</span></span>

### <span data-ttu-id="aed80-136">Microsoft. Azure. Commands. Network. model. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="aed80-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="aed80-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aed80-137">NOTES</span></span>
<span data-ttu-id="aed80-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="aed80-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="aed80-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aed80-139">RELATED LINKS</span></span>

[<span data-ttu-id="aed80-140">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="aed80-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="aed80-141">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="aed80-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="aed80-142">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="aed80-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="aed80-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="aed80-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="aed80-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="aed80-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="aed80-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="aed80-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="aed80-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="aed80-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="aed80-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aed80-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aed80-148">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="aed80-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="aed80-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aed80-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aed80-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aed80-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aed80-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aed80-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="aed80-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="aed80-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="aed80-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="aed80-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="aed80-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="aed80-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="aed80-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aed80-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aed80-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aed80-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aed80-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aed80-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aed80-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="aed80-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="aed80-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aed80-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aed80-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aed80-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="aed80-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="aed80-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="aed80-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="aed80-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="aed80-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="aed80-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="aed80-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="aed80-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="aed80-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="aed80-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="aed80-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="aed80-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
