---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTopology.md
ms.openlocfilehash: 527102bc6ee80215885efc0be42bbf740d21aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590167"
---
# <span data-ttu-id="4d08f-101">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4d08f-101">Get-AzureRmNetworkWatcherTopology</span></span>

## <span data-ttu-id="4d08f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d08f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d08f-103">Kaynak grubundaki kaynakların ve ilişkilerin ağ düzeyi görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="4d08f-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d08f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d08f-104">SYNTAX</span></span>

### <span data-ttu-id="4d08f-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d08f-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d08f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4d08f-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d08f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4d08f-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherTopology -Location <String> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d08f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d08f-108">DESCRIPTION</span></span>
<span data-ttu-id="4d08f-109">Get-AzureRmNetworkWatcherTopology cmdlet 'i kaynak grubundaki kaynakların ve ilişkilerin ağ düzeyi görünümünü görüntüler.</span><span class="sxs-lookup"><span data-stu-id="4d08f-109">The Get-AzureRmNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="4d08f-110">Not: birden çok bölgedeki kaynaklar kaynak grubunda bulunuyorsa, yalnızca ağ Izleyicisi ile aynı bölgedeki kaynaklar JSON çıktısına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="4d08f-110">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="4d08f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d08f-111">EXAMPLES</span></span>

### <span data-ttu-id="4d08f-112">Örnek 1: Azure topolojisi alma</span><span class="sxs-lookup"><span data-stu-id="4d08f-112">Example 1: Get an Azure Topology</span></span>
```
$networkWatcher = Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzureRmNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

Id                : e33d80cf-4f76-4b8f-b51c-5bb8eba80103
CreatedDateTime   : 0/00/0000 9:21:51 PM
LastModified      : 0/00/0000 4:53:29 AM
TopologyResources : [
                      {
                        "Name": "testresourcegroup-vnet",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "vm0131",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "VM0",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-nsg",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-ip",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                            "AssociationType": "Associated"
                          }
                        ]
                      },
                      {
                        "Name": "VM0-nsg",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default-allow-rdp",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default-allow-rdp",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0-ip",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Associated"
                          }
                        ]
                      }
                    ]
```

<span data-ttu-id="4d08f-113">Bu örnekte, VM, NIC, NSG ve ortak IP içeren bir kaynak grubunda Get-AzureRmNetworkWatcherTopology cmdlet 'i çalıştırdık.</span><span class="sxs-lookup"><span data-stu-id="4d08f-113">In this example we run the Get-AzureRmNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="4d08f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d08f-114">PARAMETERS</span></span>

### <span data-ttu-id="4d08f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d08f-115">-DefaultProfile</span></span>
<span data-ttu-id="4d08f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d08f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d08f-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="4d08f-117">-Location</span></span>
<span data-ttu-id="4d08f-118">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="4d08f-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4d08f-119">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4d08f-119">-NetworkWatcher</span></span>
<span data-ttu-id="4d08f-120">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="4d08f-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="4d08f-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4d08f-121">-NetworkWatcherName</span></span>
<span data-ttu-id="4d08f-122">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="4d08f-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="4d08f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d08f-123">-ResourceGroupName</span></span>
<span data-ttu-id="4d08f-124">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4d08f-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4d08f-125">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d08f-125">-TargetResourceGroupName</span></span>
<span data-ttu-id="4d08f-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4d08f-126">The resource group name.</span></span>

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

### <span data-ttu-id="4d08f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d08f-127">CommonParameters</span></span>
<span data-ttu-id="4d08f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d08f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d08f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d08f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d08f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d08f-130">INPUTS</span></span>

### <span data-ttu-id="4d08f-131">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4d08f-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4d08f-132">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d08f-132">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="4d08f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4d08f-133">System.String</span></span>
<span data-ttu-id="4d08f-134">Parametreler: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4d08f-134">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="4d08f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d08f-135">OUTPUTS</span></span>

### <span data-ttu-id="4d08f-136">Microsoft. Azure. Commands. Network. model. Pstopoloji</span><span class="sxs-lookup"><span data-stu-id="4d08f-136">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="4d08f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d08f-137">NOTES</span></span>
<span data-ttu-id="4d08f-138">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, topoloji, görüntüleme</span><span class="sxs-lookup"><span data-stu-id="4d08f-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="4d08f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d08f-139">RELATED LINKS</span></span>

[<span data-ttu-id="4d08f-140">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4d08f-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d08f-141">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4d08f-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d08f-142">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4d08f-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4d08f-143">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4d08f-143">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4d08f-144">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4d08f-144">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4d08f-145">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4d08f-145">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4d08f-146">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4d08f-146">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4d08f-147">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d08f-147">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d08f-148">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4d08f-148">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4d08f-149">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d08f-149">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d08f-150">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d08f-150">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d08f-151">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4d08f-151">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4d08f-152">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d08f-152">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="4d08f-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4d08f-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4d08f-154">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="4d08f-154">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="4d08f-155">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d08f-155">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d08f-156">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d08f-156">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d08f-157">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d08f-157">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d08f-158">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4d08f-158">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4d08f-159">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d08f-159">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d08f-160">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d08f-160">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="4d08f-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4d08f-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="4d08f-162">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="4d08f-162">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="4d08f-163">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="4d08f-163">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="4d08f-164">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4d08f-164">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4d08f-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="4d08f-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="4d08f-166">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4d08f-166">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)

