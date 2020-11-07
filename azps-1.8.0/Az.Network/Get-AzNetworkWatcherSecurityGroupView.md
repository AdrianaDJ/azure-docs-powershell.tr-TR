---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: f40b7e28bce34ef9e4cc289bed7f8c4524ef49d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760517"
---
# <span data-ttu-id="88652-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="88652-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="88652-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88652-102">SYNOPSIS</span></span>
<span data-ttu-id="88652-103">VM 'ye uygulanan yapılandırılmış ve etkin ağ güvenlik grubu kurallarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="88652-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="88652-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88652-104">SYNTAX</span></span>

### <span data-ttu-id="88652-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88652-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88652-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="88652-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88652-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="88652-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88652-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="88652-108">DESCRIPTION</span></span>
<span data-ttu-id="88652-109">Get-AzNetworkWatcherSecurityGroupView, VM 'ye uygulanan yapılandırılmış ve etkili ağ güvenlik grubu kurallarını görüntülemenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="88652-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="88652-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88652-110">EXAMPLES</span></span>

### <span data-ttu-id="88652-111">Örnek 1: bir VM 'de güvenlik grubu görünümü araması yapma</span><span class="sxs-lookup"><span data-stu-id="88652-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="88652-112">Yukarıdaki örnekte, önce bölgesel ağ Izleyicisi 'ni, ardından bölgedeki bir VM 'yi ediniyoruz.</span><span class="sxs-lookup"><span data-stu-id="88652-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="88652-113">Ardından belirtilen VM 'de bir güvenlik grubu görünümü araması yaptık.</span><span class="sxs-lookup"><span data-stu-id="88652-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="88652-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88652-114">PARAMETERS</span></span>

### <span data-ttu-id="88652-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="88652-115">-AsJob</span></span>
<span data-ttu-id="88652-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="88652-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88652-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88652-117">-DefaultProfile</span></span>
<span data-ttu-id="88652-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88652-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88652-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="88652-119">-Location</span></span>
<span data-ttu-id="88652-120">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="88652-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="88652-121">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="88652-121">-NetworkWatcher</span></span>
<span data-ttu-id="88652-122">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="88652-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="88652-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="88652-123">-NetworkWatcherName</span></span>
<span data-ttu-id="88652-124">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="88652-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="88652-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88652-125">-ResourceGroupName</span></span>
<span data-ttu-id="88652-126">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="88652-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="88652-127">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="88652-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="88652-128">Hedef VM kimliği</span><span class="sxs-lookup"><span data-stu-id="88652-128">The target VM Id</span></span>

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

### <span data-ttu-id="88652-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88652-129">CommonParameters</span></span>
<span data-ttu-id="88652-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88652-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88652-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="88652-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88652-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88652-132">INPUTS</span></span>

### <span data-ttu-id="88652-133">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="88652-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="88652-134">System. String</span><span class="sxs-lookup"><span data-stu-id="88652-134">System.String</span></span>

## <span data-ttu-id="88652-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88652-135">OUTPUTS</span></span>

### <span data-ttu-id="88652-136">Microsoft. Azure. Commands. Network. model. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="88652-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="88652-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88652-137">NOTES</span></span>
<span data-ttu-id="88652-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="88652-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="88652-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88652-139">RELATED LINKS</span></span>

[<span data-ttu-id="88652-140">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="88652-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="88652-141">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="88652-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="88652-142">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="88652-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="88652-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="88652-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="88652-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="88652-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="88652-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="88652-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="88652-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="88652-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="88652-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="88652-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="88652-148">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="88652-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="88652-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="88652-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="88652-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="88652-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="88652-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="88652-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="88652-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="88652-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="88652-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="88652-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="88652-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="88652-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="88652-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="88652-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="88652-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="88652-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="88652-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="88652-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="88652-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="88652-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="88652-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="88652-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="88652-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="88652-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="88652-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="88652-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="88652-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="88652-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="88652-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="88652-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="88652-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="88652-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="88652-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="88652-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="88652-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="88652-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)