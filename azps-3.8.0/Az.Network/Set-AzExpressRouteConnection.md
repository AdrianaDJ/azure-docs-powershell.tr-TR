---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: 1e2156b955f4b7a98f6c8886ea538f77cee7fe34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096817"
---
# <span data-ttu-id="8358d-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8358d-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="8358d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8358d-102">SYNOPSIS</span></span>
<span data-ttu-id="8358d-103">Bir hızlı rota ağ geçidi ile şirket içi hızlı rota devresi eşlemesi arasında oluşturulmuş bir hızlı rota bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8358d-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="8358d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8358d-104">SYNTAX</span></span>

### <span data-ttu-id="8358d-105">ByExpressRouteConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8358d-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8358d-106">Byexpressrouteconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="8358d-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8358d-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="8358d-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8358d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8358d-108">DESCRIPTION</span></span>
<span data-ttu-id="8358d-109">**Set-AzExpressRouteConnection** cmdlet 'i, bir hızlı rota ağ geçidi ile şirket içi hızlı rota devresi eşlemesi arasında oluşturulmuş bir hızlı rota bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8358d-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="8358d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8358d-110">EXAMPLES</span></span>

### <span data-ttu-id="8358d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8358d-111">Example 1</span></span>

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
PS C:\> Set-AzExpressRouteConnection -InputObject $ExpressRouteConnection -RoutingWeight 30

ExpressRouteCircuitPeeringId       : Microsoft.Azure.Commands.Network.Models.PSResourceId
AuthorizationKey                   :
RoutingWeight                      : 30
ProvisioningState                  : Succeeded
Name                               : testConnection
Etag                               : W/"4580a2e2-2fab-4cff-88eb-92013a76b5a8"
Id                                 : /subscriptions/{subscriptionId}/resourceGroups/ps9361/providers/Microsoft.Network/ExpressRouteGateways/testExpressRoutegw/expressRouteConnections/testConnection
```

<span data-ttu-id="8358d-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir ExpressRouteSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8358d-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="8358d-113">Daha sonra 2 ölçekli birim içeren sanal hub 'da bir ExpressRoute ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8358d-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="8358d-114">Ağ Geçidi oluşturulduktan sonra, New-AzExpressRouteConnection komutunu kullanarak şirket içi ExpressRoute devresi ile bağlantılıdır.</span><span class="sxs-lookup"><span data-stu-id="8358d-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="8358d-115">Bağlantı daha sonra Set-AzExpressRouteConnection komutu kullanılarak farklı bir RoutingWeight olacak şekilde güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8358d-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="8358d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8358d-116">PARAMETERS</span></span>

### <span data-ttu-id="8358d-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="8358d-117">-AsJob</span></span>
<span data-ttu-id="8358d-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8358d-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8358d-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="8358d-119">-AuthorizationKey</span></span>
<span data-ttu-id="8358d-120">ExpressRoute ağ geçidi bağlantısını oluşturmak için kullanılacak yetkilendirme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="8358d-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="8358d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8358d-121">-DefaultProfile</span></span>
<span data-ttu-id="8358d-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8358d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8358d-123">-Enableınternetgüvenlik</span><span class="sxs-lookup"><span data-stu-id="8358d-123">-EnableInternetSecurity</span></span>
<span data-ttu-id="8358d-124">Bu ExpressRoute ağ geçidi bağlantısı için Internet güvenliğini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="8358d-124">Enable internet security for this ExpressRoute Gateway connection</span></span>

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

### <span data-ttu-id="8358d-125">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="8358d-125">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="8358d-126">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8358d-126">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8358d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8358d-127">-InputObject</span></span>
<span data-ttu-id="8358d-128">Güncelleştirilecek ExpressRouteConnection nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8358d-128">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8358d-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="8358d-129">-Name</span></span>
<span data-ttu-id="8358d-130">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8358d-130">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8358d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8358d-131">-ResourceGroupName</span></span>
<span data-ttu-id="8358d-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8358d-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8358d-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8358d-133">-ResourceId</span></span>
<span data-ttu-id="8358d-134">Silinecek ExpressRouteConnection nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8358d-134">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8358d-135">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="8358d-135">-RoutingWeight</span></span>
<span data-ttu-id="8358d-136">Paket yönlendirme için bu bağlantıya atanması gereken ağırlık.</span><span class="sxs-lookup"><span data-stu-id="8358d-136">The weight that needs to be assigned to this connection for packet routing.</span></span>

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

### <span data-ttu-id="8358d-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="8358d-137">-Confirm</span></span>
<span data-ttu-id="8358d-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8358d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8358d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8358d-139">-WhatIf</span></span>
<span data-ttu-id="8358d-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8358d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8358d-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8358d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8358d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8358d-142">CommonParameters</span></span>
<span data-ttu-id="8358d-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8358d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8358d-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8358d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8358d-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8358d-145">INPUTS</span></span>

### <span data-ttu-id="8358d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="8358d-146">System.String</span></span>

### <span data-ttu-id="8358d-147">Microsoft. Azure. Commands. Network. model. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8358d-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="8358d-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8358d-148">OUTPUTS</span></span>

### <span data-ttu-id="8358d-149">Microsoft. Azure. Commands. Network. model. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="8358d-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="8358d-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8358d-150">NOTES</span></span>

## <span data-ttu-id="8358d-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8358d-151">RELATED LINKS</span></span>
