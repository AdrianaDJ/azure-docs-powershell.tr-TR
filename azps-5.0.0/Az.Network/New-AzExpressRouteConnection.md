---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteConnection.md
ms.openlocfilehash: 565e79420821e8d8764b5e461e33d275247ddb3c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278538"
---
# <span data-ttu-id="1b811-101">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="1b811-101">New-AzExpressRouteConnection</span></span>

## <span data-ttu-id="1b811-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b811-102">SYNOPSIS</span></span>
<span data-ttu-id="1b811-103">Bir ExpressRoute bağlantısını şirket içi ExpressRoute devresine bağlayan bir ExpressRoute bağlantısı oluşturur</span><span class="sxs-lookup"><span data-stu-id="1b811-103">Creates an ExpressRoute connection that connects an ExpressRoute gateway to an on premise ExpressRoute circuit</span></span>

## <span data-ttu-id="1b811-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b811-104">SYNTAX</span></span>

### <span data-ttu-id="1b811-105">ByExpressRouteGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b811-105">ByExpressRouteGatewayName (Default)</span></span>
```
New-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b811-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="1b811-106">ByExpressRouteGatewayObject</span></span>
```
New-AzExpressRouteConnection -ExpressRouteGatewayObject <PSExpressRouteGateway> -Name <String>
 -ExpressRouteCircuitPeeringId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b811-107">Byexpressroutegatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="1b811-107">ByExpressRouteGatewayResourceId</span></span>
```
New-AzExpressRouteConnection -ParentResourceId <String> -Name <String> -ExpressRouteCircuitPeeringId <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-RoutingConfiguration <PSRoutingConfiguration>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b811-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b811-108">DESCRIPTION</span></span>
<span data-ttu-id="1b811-109">Sanal hub içindeki ExpressRoute ağ geçidiyle şirket içi ExpressRoute devresi BGP eşlemesi arasında bir ExpressRoute bağlantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b811-109">Creates an ExpressRoute connection between an on-premise ExpressRoute circuit BGP peering to the ExpressRoute gateway inside a Virtual hub.</span></span>

## <span data-ttu-id="1b811-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b811-110">EXAMPLES</span></span>

### <span data-ttu-id="1b811-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b811-111">Example 1</span></span>

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
ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 20
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
RoutingConfiguration               : {
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

<span data-ttu-id="1b811-112">Yukarıdaki bir kaynak grubu, sanal WAN, sanal ağ, sanal hub, hızlı rota ağ geçidi ve Azure 'daki "testRG" kaynak grubunda Batı merkezi</span><span class="sxs-lookup"><span data-stu-id="1b811-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub, Express Route gateway and an ExpressRoute circuit with private peering in West Central US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="1b811-113">Ağ Geçidi oluşturulduktan sonra, New-AzExpressRouteConnection komutu kullanılarak ExpressRoute devresi eşliğini içerir.</span><span class="sxs-lookup"><span data-stu-id="1b811-113">Once the gateway has been created, it is connected to the ExpressRoute Circuit Peering using the New-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="1b811-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b811-114">PARAMETERS</span></span>

### <span data-ttu-id="1b811-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="1b811-115">-AsJob</span></span>
<span data-ttu-id="1b811-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1b811-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b811-117">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="1b811-117">-AuthorizationKey</span></span>
<span data-ttu-id="1b811-118">ExpressRoute devresi sahibinden alınan bir anahtar, farklı bir abonelikteki ağ geçidiyle bağlantı oluşturabilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1b811-118">A key obtained from the ExpressRoute circuit owner to be able to create a connection with a gateway in a different subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b811-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b811-119">-DefaultProfile</span></span>
<span data-ttu-id="1b811-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b811-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b811-121">-Enableınternetgüvenlik</span><span class="sxs-lookup"><span data-stu-id="1b811-121">-EnableInternetSecurity</span></span>
<span data-ttu-id="1b811-122">Bu ExpressRoute ağ geçidi bağlantısı için Internet güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="1b811-122">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="1b811-123">-Expressroutedevresi Peeringıd</span><span class="sxs-lookup"><span data-stu-id="1b811-123">-ExpressRouteCircuitPeeringId</span></span>
<span data-ttu-id="1b811-124">Bu hızlı rota devre Ağ Geçidi bağlantısının oluşturulduğu hızlı rota devresi eşleme kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1b811-124">The resource id of the Express Route Circuit Peering to which this Express Route gateway connection is to be created to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b811-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="1b811-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="1b811-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1b811-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b811-127">-ExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="1b811-127">-ExpressRouteGatewayObject</span></span>
<span data-ttu-id="1b811-128">Bu bağlantı için üst ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="1b811-128">The parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b811-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b811-129">-Name</span></span>
<span data-ttu-id="1b811-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1b811-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b811-131">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="1b811-131">-ParentResourceId</span></span>
<span data-ttu-id="1b811-132">Bu bağlantı için üst ExpressRouteGateway 'in kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="1b811-132">The resource id of the parent ExpressRouteGateway for this connection.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: ExpressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b811-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b811-133">-ResourceGroupName</span></span>
<span data-ttu-id="1b811-134">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1b811-134">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b811-135">-RoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b811-135">-RoutingConfiguration</span></span>
<span data-ttu-id="1b811-136">Bu bağlantı için Yönlendirme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="1b811-136">Routing configuration for this connection</span></span>

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

### <span data-ttu-id="1b811-137">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="1b811-137">-RoutingWeight</span></span>
<span data-ttu-id="1b811-138">Bu bağlantıya atanması gereken paket yönlendirme ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="1b811-138">The weight for packet routing that needs to be assigned to this connection.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b811-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b811-139">-Confirm</span></span>
<span data-ttu-id="1b811-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b811-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b811-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b811-141">-WhatIf</span></span>
<span data-ttu-id="1b811-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b811-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b811-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b811-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b811-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b811-144">CommonParameters</span></span>
<span data-ttu-id="1b811-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b811-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b811-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b811-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b811-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b811-147">INPUTS</span></span>

### <span data-ttu-id="1b811-148">Microsoft. Azure. Commands. Network. model. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="1b811-148">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="1b811-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1b811-149">System.String</span></span>

## <span data-ttu-id="1b811-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b811-150">OUTPUTS</span></span>

### <span data-ttu-id="1b811-151">Microsoft. Azure. Commands. Network. model. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="1b811-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="1b811-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b811-152">NOTES</span></span>

## <span data-ttu-id="1b811-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b811-153">RELATED LINKS</span></span>

[<span data-ttu-id="1b811-154">Yeni-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b811-154">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)
