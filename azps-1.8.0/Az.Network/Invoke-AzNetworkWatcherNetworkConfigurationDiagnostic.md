---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: a79de3beadefefd3de65b830f42e4728ca6b6b82
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760438"
---
# <span data-ttu-id="ddab5-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ddab5-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="ddab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddab5-102">SYNOPSIS</span></span>
<span data-ttu-id="ddab5-103">Hedef kaynakta belirtilen ağ profillerinde ağ yapılandırması tanılama oturumunu çağır.</span><span class="sxs-lookup"><span data-stu-id="ddab5-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="ddab5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddab5-104">SYNTAX</span></span>

### <span data-ttu-id="ddab5-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ddab5-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddab5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ddab5-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddab5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ddab5-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddab5-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="ddab5-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddab5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddab5-109">DESCRIPTION</span></span>
<span data-ttu-id="ddab5-110">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet 'i hedef kaynakta belirtilen ağ profilleri için ağ yapılandırması tanılama oturumunu çağırır.</span><span class="sxs-lookup"><span data-stu-id="ddab5-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="ddab5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddab5-111">EXAMPLES</span></span>

### <span data-ttu-id="ddab5-112">Örnek 1: VM için ağ yapılandırması Tanılama oturumu</span><span class="sxs-lookup"><span data-stu-id="ddab5-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="ddab5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddab5-113">PARAMETERS</span></span>

### <span data-ttu-id="ddab5-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="ddab5-114">-AsJob</span></span>
<span data-ttu-id="ddab5-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ddab5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddab5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddab5-116">-DefaultProfile</span></span>
<span data-ttu-id="ddab5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddab5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddab5-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="ddab5-118">-Location</span></span>
<span data-ttu-id="ddab5-119">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="ddab5-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ddab5-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ddab5-120">-NetworkWatcher</span></span>
<span data-ttu-id="ddab5-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="ddab5-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="ddab5-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ddab5-122">-NetworkWatcherName</span></span>
<span data-ttu-id="ddab5-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="ddab5-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddab5-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="ddab5-124">-Profile</span></span>
<span data-ttu-id="ddab5-125">Ağ yapılandırması tanılama profillerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="ddab5-125">List of network configuration diagnostic profiles.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddab5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddab5-126">-ResourceGroupName</span></span>
<span data-ttu-id="ddab5-127">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ddab5-127">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddab5-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ddab5-128">-ResourceId</span></span>
<span data-ttu-id="ddab5-129">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ddab5-129">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddab5-130">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="ddab5-130">-TargetResourceId</span></span>
<span data-ttu-id="ddab5-131">Ağ yapılandırması tanılaması 'nı gerçekleştirecek hedef kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ddab5-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="ddab5-132">Geçerli seçenekler VM, NetworkInterface, VMSS/NetworkInterface ve uygulama ağ geçididir.</span><span class="sxs-lookup"><span data-stu-id="ddab5-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="ddab5-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="ddab5-133">-VerbosityLevel</span></span>
<span data-ttu-id="ddab5-134">Ayrıntı düzeyi.</span><span class="sxs-lookup"><span data-stu-id="ddab5-134">Verbosity level.</span></span>
<span data-ttu-id="ddab5-135">Kabul edilen değerler ' normal ', ' en az ', ' tam ' dir.</span><span class="sxs-lookup"><span data-stu-id="ddab5-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddab5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddab5-136">CommonParameters</span></span>
<span data-ttu-id="ddab5-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddab5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddab5-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddab5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddab5-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddab5-139">INPUTS</span></span>

### <span data-ttu-id="ddab5-140">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ddab5-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ddab5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ddab5-141">System.String</span></span>

## <span data-ttu-id="ddab5-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddab5-142">OUTPUTS</span></span>

### <span data-ttu-id="ddab5-143">Microsoft. Azure. Commands. Network. model. PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="ddab5-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="ddab5-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddab5-144">NOTES</span></span>
<span data-ttu-id="ddab5-145">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, tanılama, profil</span><span class="sxs-lookup"><span data-stu-id="ddab5-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="ddab5-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddab5-146">RELATED LINKS</span></span>

[<span data-ttu-id="ddab5-147">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="ddab5-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ddab5-148">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ddab5-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ddab5-149">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ddab5-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ddab5-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ddab5-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ddab5-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ddab5-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ddab5-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ddab5-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ddab5-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ddab5-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ddab5-154">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ddab5-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ddab5-155">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ddab5-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ddab5-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ddab5-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ddab5-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ddab5-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ddab5-158">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ddab5-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ddab5-159">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddab5-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ddab5-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ddab5-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ddab5-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ddab5-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ddab5-162">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ddab5-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ddab5-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ddab5-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ddab5-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ddab5-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ddab5-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ddab5-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ddab5-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ddab5-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ddab5-167">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ddab5-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ddab5-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ddab5-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ddab5-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ddab5-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ddab5-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ddab5-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ddab5-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ddab5-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ddab5-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ddab5-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="ddab5-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ddab5-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
