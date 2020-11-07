---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteConnection.md
ms.openlocfilehash: 01b8c32af3edc6c10070bdbd61c7f84fa055af23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760589"
---
# <span data-ttu-id="47896-101">Get-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="47896-101">Get-AzExpressRouteConnection</span></span>

## <span data-ttu-id="47896-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47896-102">SYNOPSIS</span></span>
<span data-ttu-id="47896-103">Bir ExpressRouteGateway 'e bağlı tüm ExpressRoute bağlantılarını ada göre bir ExpressRoute bağlantısını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="47896-103">Gets a ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="47896-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47896-104">SYNTAX</span></span>

### <span data-ttu-id="47896-105">ByExpressRouteGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47896-105">ByExpressRouteGatewayName (Default)</span></span>
```
Get-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47896-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="47896-106">ByExpressRouteGatewayObject</span></span>
```
Get-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47896-107">Byexpressroutegatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="47896-107">ByExpressRouteGatewayResourceId</span></span>
```
Get-AzExpressRouteConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47896-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47896-108">DESCRIPTION</span></span>
<span data-ttu-id="47896-109">ExpressRouteGateway 'e bağlı tüm ExpressRoute bağlantılarını ada göre bir ExpressRoute bağlantısını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="47896-109">Gets an ExpressRoute connection by name or lists all ExpressRoute connections connected to a ExpressRouteGateway.</span></span>

## <span data-ttu-id="47896-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47896-110">EXAMPLES</span></span>

### <span data-ttu-id="47896-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="47896-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="47896-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir ExpressRouteSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47896-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="47896-113">Daha sonra 2 ölçekli birim içeren sanal hub 'da bir ExpressRoute ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="47896-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="47896-114">Ağ Geçidi oluşturulduktan sonra, New-AzExpressRouteConnection komutunu kullanarak şirket içi ExpressRoute devresi 'e bağlanır.</span><span class="sxs-lookup"><span data-stu-id="47896-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="47896-115">Ardından bağlantı adını kullanarak bağlantıyı alır.</span><span class="sxs-lookup"><span data-stu-id="47896-115">Then it gets the connection using the connection name.</span></span>

### <span data-ttu-id="47896-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="47896-116">Example 2</span></span>

```powershell
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName ps9361 -ParentResourceName testExpressRoutegw -Name test*

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection1
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection1

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection2
Etag                               : W/"00000000-0000-0000-0000-000000000000"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection2
```

<span data-ttu-id="47896-117">Bu komut ExpressRoute 'ta "testExpressRoutegw" ile başlayan tüm bağlantıları alır</span><span class="sxs-lookup"><span data-stu-id="47896-117">This command will get all Connections in ExpressRoute "testExpressRoutegw" that start with "test"</span></span>

## <span data-ttu-id="47896-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47896-118">PARAMETERS</span></span>

### <span data-ttu-id="47896-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47896-119">-DefaultProfile</span></span>
<span data-ttu-id="47896-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47896-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47896-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="47896-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="47896-122">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="47896-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47896-123">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="47896-123">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="47896-124">Bu bağlantı için üst ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="47896-124">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47896-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="47896-125">-Name</span></span>
<span data-ttu-id="47896-126">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="47896-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="47896-127">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="47896-127">-ParentResourceId</span></span>
<span data-ttu-id="47896-128">Bu bağlantı için üst ExpressRouteGateway 'in kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="47896-128">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47896-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47896-129">-ResourceGroupName</span></span>
<span data-ttu-id="47896-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="47896-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47896-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47896-131">CommonParameters</span></span>
<span data-ttu-id="47896-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47896-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47896-133">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="47896-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47896-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47896-134">INPUTS</span></span>

### <span data-ttu-id="47896-135">System. String</span><span class="sxs-lookup"><span data-stu-id="47896-135">System.String</span></span>

## <span data-ttu-id="47896-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47896-136">OUTPUTS</span></span>

### <span data-ttu-id="47896-137">Microsoft. Azure. Commands. Network. model. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="47896-137">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="47896-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47896-138">NOTES</span></span>

## <span data-ttu-id="47896-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47896-139">RELATED LINKS</span></span>