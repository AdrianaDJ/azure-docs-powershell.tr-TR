---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f4087782e247e574cd49634e148b6852e9fb8dc6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323680"
---
# <span data-ttu-id="02668-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="02668-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="02668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02668-102">SYNOPSIS</span></span>
<span data-ttu-id="02668-103">New-AzVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="02668-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="02668-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02668-104">SYNTAX</span></span>

### <span data-ttu-id="02668-105">ByVirtualHubNameByRemoteVirtualNetworkObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02668-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02668-106">Byvirtualhubnamebyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="02668-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02668-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="02668-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02668-108">Byvirtualhubobjectbyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="02668-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02668-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="02668-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>]
 [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02668-110">Byvirtualhubresourceıdbyremotevirtualnetworkresourceıd</span><span class="sxs-lookup"><span data-stu-id="02668-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-EnableInternetSecurityFlag <Boolean>] [-RoutingConfiguration <PSRoutingConfiguration>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02668-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="02668-111">DESCRIPTION</span></span>
<span data-ttu-id="02668-112">New-AzVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="02668-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="02668-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02668-113">EXAMPLES</span></span>

### <span data-ttu-id="02668-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02668-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
RoutingConfiguration : {
                            "AssociatedRouteTable": {
                                "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                            },
                            "PropagatedRouteTables": {
                                "Labels": [],
                                "Ids": [
                                    {
                                        "Id": "/subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubRouteTables/defaultRouteTable"
                                    }
                                ]
                            },
                            "VnetRoutes": {
                                "StaticRoutes": []
                            }
                        }
```

<span data-ttu-id="02668-115">Yukarıdaki, Azure 'daki bu kaynak grubunda merkezi olarak ABD 'de bir kaynak grubu, sanal WAN, sanal ağ ve sanal hub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="02668-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="02668-116">Bundan sonra sanal ağı sanal hub 'a eşler.</span><span class="sxs-lookup"><span data-stu-id="02668-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

### <span data-ttu-id="02668-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="02668-117">Example 2</span></span>

<span data-ttu-id="02668-118">New-AzVirtualHubVnetConnection cmdlet 'i, Azure sanal hub 'a sanal bir ağı eşuygulayan bir HubVirtualNetworkConnection kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="02668-118">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span> <span data-ttu-id="02668-119">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="02668-119">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVirtualHubVnetConnection -EnableInternetSecurity -Name 'testvnetconnection' -ParentResourceName 'westushub' -RemoteVirtualNetwork <PSVirtualNetwork> -ResourceGroupName 'testRG'
```


### <span data-ttu-id="02668-120">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="02668-120">Example 3</span></span>
```powershell
PS C:\> $rgName = "testRg"
PS C:\> $virtualHubName = "testHub"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName $rgName -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $rt1 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "defaultRouteTable"
PS C:\> $rt2 = Get-AzVHubRouteTable -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "noneRouteTable"
PS C:\> $route1 = New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16")-NextHopIpAddress "10.90.0.5"
PS C:\> $routingconfig = New-AzRoutingConfiguration -AssociatedRouteTable $rt1.Id -Label @("testLabel") -Id @($rt2.Id) -StaticRoute @($route1)

AssociatedRouteTable  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/defaultRouteTable"
PropagatedRouteTables : {
                          "Labels": [
                            "testLabel"
                          ],
                          "Ids": [
                            {
                              "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testRg/providers/Microsoft.Network/virtualHubs/testHub/hubRouteTables/noneRouteTable"
                            }
                          ]
                        }
VnetRoutes            : {
                          "StaticRoutes": [
                            {
                              "Name": "route1",
                              "AddressPrefixes": [
                                "10.20.0.0/16",
                                "10.30.0.0/16"
                              ],
                              "NextHopIpAddress": "10.90.0.5"
                            }
                          ]
                        }
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName $rgName -VirtualHubName $virtualHubName -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork -RoutingConfiguration $routingconfig
```
<span data-ttu-id="02668-121">Yukarıdaki, yeni bir yönlendirme yapılandırması oluşturur ve yönlendirme yapılandırmasında belirtilen IP adresi olarak bir sonraki atlamada statik yollar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="02668-121">The above will create a new routing configuration and create static routes in the routing config with the next hop as a specified IP address.</span></span> <span data-ttu-id="02668-122">Bu yönlendirme yapılandırması daha sonra New-AzVirtualHubVnetConnection komutuna parametre-RoutingConfiguration olarak iletilebilir.</span><span class="sxs-lookup"><span data-stu-id="02668-122">This routing configuration can then be passed into  the New-AzVirtualHubVnetConnection command as the parameter -RoutingConfiguration.</span></span>

## <span data-ttu-id="02668-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02668-123">PARAMETERS</span></span>

### <span data-ttu-id="02668-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="02668-124">-AsJob</span></span>
<span data-ttu-id="02668-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="02668-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02668-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02668-126">-DefaultProfile</span></span>
<span data-ttu-id="02668-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02668-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02668-128">-Enableınternetgüvenlik</span><span class="sxs-lookup"><span data-stu-id="02668-128">-EnableInternetSecurity</span></span>
<span data-ttu-id="02668-129">Bu bağlantı için İnternet güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="02668-129">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="02668-130">-Enableınternetsecurityflag</span><span class="sxs-lookup"><span data-stu-id="02668-130">-EnableInternetSecurityFlag</span></span>
<span data-ttu-id="02668-131">Bu bağlantı için İnternet güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="02668-131">Enable internet security for this connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02668-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="02668-132">-Name</span></span>
<span data-ttu-id="02668-133">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="02668-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02668-134">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02668-134">-ParentObject</span></span>
<span data-ttu-id="02668-135">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="02668-135">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02668-136">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="02668-136">-ParentResourceId</span></span>
<span data-ttu-id="02668-137">Üst kaynak.</span><span class="sxs-lookup"><span data-stu-id="02668-137">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02668-138">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="02668-138">-ParentResourceName</span></span>
<span data-ttu-id="02668-139">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="02668-139">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02668-140">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="02668-140">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="02668-141">Bu hub sanal ağ bağlantısının bağlı olduğu uzaktaki sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="02668-141">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02668-142">-Remotevirtualnetworkıd</span><span class="sxs-lookup"><span data-stu-id="02668-142">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="02668-143">Bu hub sanal ağ bağlantısının bağlı olduğu uzaktaki sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="02668-143">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02668-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02668-144">-ResourceGroupName</span></span>
<span data-ttu-id="02668-145">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="02668-145">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02668-146">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="02668-146">-RoutingConfiguration</span></span>
<span data-ttu-id="02668-147">Bu bağlantı için Yönlendirme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="02668-147">Routing configuration for this connection</span></span>

```yaml
Type: PSRoutingConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02668-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="02668-148">-Confirm</span></span>
<span data-ttu-id="02668-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02668-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02668-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02668-150">-WhatIf</span></span>
<span data-ttu-id="02668-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02668-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02668-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02668-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02668-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02668-153">CommonParameters</span></span>
<span data-ttu-id="02668-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02668-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02668-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02668-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02668-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02668-156">INPUTS</span></span>

### <span data-ttu-id="02668-157">Microsoft. Azure. Commands. Network. modeller. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="02668-157">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="02668-158">System. String</span><span class="sxs-lookup"><span data-stu-id="02668-158">System.String</span></span>

## <span data-ttu-id="02668-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02668-159">OUTPUTS</span></span>

### <span data-ttu-id="02668-160">Microsoft. Azure. Commands. Network. model. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="02668-160">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="02668-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02668-161">NOTES</span></span>

## <span data-ttu-id="02668-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02668-162">RELATED LINKS</span></span>

[<span data-ttu-id="02668-163">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="02668-163">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="02668-164">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="02668-164">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="02668-165">Yeni-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="02668-165">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
