---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 72f5c803c7fa4f4693da3660c41f73eadb464ab7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935501"
---
# <span data-ttu-id="6867a-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6867a-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="6867a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6867a-102">SYNOPSIS</span></span>
<span data-ttu-id="6867a-103">Kaynak grubundaki kaynakların ve ilişkilerin ağ düzeyi görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="6867a-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="6867a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6867a-104">SYNTAX</span></span>

### <span data-ttu-id="6867a-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6867a-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6867a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6867a-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6867a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6867a-107">DESCRIPTION</span></span>
<span data-ttu-id="6867a-108">Get-AzNetworkWatcherTopology cmdlet 'i kaynak grubundaki kaynakların ve ilişkilerin ağ düzeyi görünümünü görüntüler.</span><span class="sxs-lookup"><span data-stu-id="6867a-108">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="6867a-109">Not: birden çok bölgedeki kaynaklar kaynak grubunda bulunuyorsa, yalnızca ağ Izleyicisi ile aynı bölgedeki kaynaklar JSON çıktısına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="6867a-109">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="6867a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6867a-110">EXAMPLES</span></span>

### <span data-ttu-id="6867a-111">--------------------------Örnek 1: Azure topolojisi alma--------------------------</span><span class="sxs-lookup"><span data-stu-id="6867a-111">--------------------------  Example 1: Get an Azure Topology  --------------------------</span></span>
```
$networkWatcher = Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

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

<span data-ttu-id="6867a-112">Bu örnekte, VM, NIC, NSG ve ortak IP içeren bir kaynak grubunda Get-AzNetworkWatcherTopology cmdlet 'i çalıştırdık.</span><span class="sxs-lookup"><span data-stu-id="6867a-112">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="6867a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6867a-113">PARAMETERS</span></span>

### <span data-ttu-id="6867a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6867a-114">-DefaultProfile</span></span>
<span data-ttu-id="6867a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6867a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6867a-116">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6867a-116">-NetworkWatcher</span></span>
<span data-ttu-id="6867a-117">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="6867a-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="6867a-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6867a-118">-NetworkWatcherName</span></span>
<span data-ttu-id="6867a-119">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="6867a-119">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6867a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6867a-120">-ResourceGroupName</span></span>
<span data-ttu-id="6867a-121">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6867a-121">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6867a-122">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6867a-122">-TargetResourceGroupName</span></span>
<span data-ttu-id="6867a-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6867a-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6867a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6867a-124">CommonParameters</span></span>
<span data-ttu-id="6867a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6867a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6867a-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6867a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6867a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6867a-127">INPUTS</span></span>

### <span data-ttu-id="6867a-128">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6867a-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6867a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6867a-129">System.String</span></span>

## <span data-ttu-id="6867a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6867a-130">OUTPUTS</span></span>

### <span data-ttu-id="6867a-131">Microsoft. Azure. Commands. Network. model. Pstopoloji</span><span class="sxs-lookup"><span data-stu-id="6867a-131">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="6867a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6867a-132">NOTES</span></span>
<span data-ttu-id="6867a-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, topoloji, görüntüleme</span><span class="sxs-lookup"><span data-stu-id="6867a-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="6867a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6867a-134">RELATED LINKS</span></span>

[<span data-ttu-id="6867a-135">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="6867a-135">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6867a-136">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6867a-136">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6867a-137">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6867a-137">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6867a-138">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6867a-138">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6867a-139">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6867a-139">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6867a-140">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6867a-140">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6867a-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6867a-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6867a-142">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6867a-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6867a-143">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6867a-143">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6867a-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6867a-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6867a-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6867a-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6867a-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6867a-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

