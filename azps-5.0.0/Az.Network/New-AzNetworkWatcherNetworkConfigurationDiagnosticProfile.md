---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275974"
---
# <span data-ttu-id="492bb-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="492bb-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="492bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="492bb-102">SYNOPSIS</span></span>
<span data-ttu-id="492bb-103">Yeni bir ağ yapılandırması tanılama profili nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="492bb-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="492bb-104">Bu nesne, belirtilen ölçütleri kullanarak Tanılama oturumu sırasında ağ yapılandırmasını kısıtlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="492bb-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="492bb-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="492bb-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="492bb-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="492bb-106">DESCRIPTION</span></span>
<span data-ttu-id="492bb-107">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet 'i yeni bir tanılama profili nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="492bb-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="492bb-108">Bu nesne, ağ yapılandırması Tanılama oturumu sırasında belirtilen ölçütleri kullanarak ağ yapılandırmasını kısıtlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="492bb-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="492bb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="492bb-109">EXAMPLES</span></span>

### <span data-ttu-id="492bb-110">Örnek 1: VM için ağ yapılandırması Tanılama oturumu</span><span class="sxs-lookup"><span data-stu-id="492bb-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="492bb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="492bb-111">PARAMETERS</span></span>

### <span data-ttu-id="492bb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="492bb-112">-DefaultProfile</span></span>
<span data-ttu-id="492bb-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="492bb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="492bb-114">-Hedef</span><span class="sxs-lookup"><span data-stu-id="492bb-114">-Destination</span></span>
<span data-ttu-id="492bb-115">Trafik hedefi.</span><span class="sxs-lookup"><span data-stu-id="492bb-115">Traffic destination.</span></span>
<span data-ttu-id="492bb-116">Kabul edilen değerler: ' \* ', IP adresi/CıDR, hizmet etiketi.</span><span class="sxs-lookup"><span data-stu-id="492bb-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="492bb-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="492bb-117">-DestinationPort</span></span>
<span data-ttu-id="492bb-118">Trafik hedef bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="492bb-118">Traffic destination port.</span></span>
<span data-ttu-id="492bb-119">Kabul edilen değerler ' \* ', bağlantı noktası (örneğin, 3389) ve bağlantı noktası aralığı (örneğin, 80-100).</span><span class="sxs-lookup"><span data-stu-id="492bb-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="492bb-120">-Yön</span><span class="sxs-lookup"><span data-stu-id="492bb-120">-Direction</span></span>
<span data-ttu-id="492bb-121">Trafiğin yönü.</span><span class="sxs-lookup"><span data-stu-id="492bb-121">The direction of the traffic.</span></span>
<span data-ttu-id="492bb-122">Kabul edilen değerler ' gelen ' ve ' giden '</span><span class="sxs-lookup"><span data-stu-id="492bb-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="492bb-123">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="492bb-123">-Protocol</span></span>
<span data-ttu-id="492bb-124">Doğrulanacak iletişim kuralı.</span><span class="sxs-lookup"><span data-stu-id="492bb-124">Protocol to be verified on.</span></span>
<span data-ttu-id="492bb-125">Kabul edilen değerler ' \* ', TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="492bb-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="492bb-126">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="492bb-126">-Source</span></span>
<span data-ttu-id="492bb-127">Trafik kaynağı.</span><span class="sxs-lookup"><span data-stu-id="492bb-127">Traffic source.</span></span>
<span data-ttu-id="492bb-128">Kabul edilen değerler ' \* ', IP adresi/CıDR, hizmet etiketi.</span><span class="sxs-lookup"><span data-stu-id="492bb-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="492bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="492bb-129">CommonParameters</span></span>
<span data-ttu-id="492bb-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="492bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="492bb-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="492bb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="492bb-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="492bb-132">INPUTS</span></span>

### <span data-ttu-id="492bb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="492bb-133">System.String</span></span>

## <span data-ttu-id="492bb-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="492bb-134">OUTPUTS</span></span>

### <span data-ttu-id="492bb-135">Microsoft. Azure. Commands. Network. model. PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="492bb-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="492bb-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="492bb-136">NOTES</span></span>
<span data-ttu-id="492bb-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, tanılama, profil</span><span class="sxs-lookup"><span data-stu-id="492bb-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="492bb-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="492bb-138">RELATED LINKS</span></span>

[<span data-ttu-id="492bb-139">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="492bb-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="492bb-140">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="492bb-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="492bb-141">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="492bb-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="492bb-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="492bb-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="492bb-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="492bb-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="492bb-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="492bb-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="492bb-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="492bb-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="492bb-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="492bb-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="492bb-147">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="492bb-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="492bb-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="492bb-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="492bb-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="492bb-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="492bb-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="492bb-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="492bb-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="492bb-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="492bb-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="492bb-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="492bb-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="492bb-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="492bb-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="492bb-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="492bb-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="492bb-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="492bb-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="492bb-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="492bb-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="492bb-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="492bb-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="492bb-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="492bb-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="492bb-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="492bb-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="492bb-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="492bb-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="492bb-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="492bb-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="492bb-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="492bb-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="492bb-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="492bb-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="492bb-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="492bb-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="492bb-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
