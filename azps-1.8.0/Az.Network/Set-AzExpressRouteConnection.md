---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteConnection.md
ms.openlocfilehash: 70f349fbb6a97009db4ba11e8de945b0700e3c2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760022"
---
# <span data-ttu-id="7fac1-101">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7fac1-101">Set-AzExpressRouteConnection</span></span>

## <span data-ttu-id="7fac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fac1-102">SYNOPSIS</span></span>
<span data-ttu-id="7fac1-103">Bir hızlı rota ağ geçidi ile şirket içi hızlı rota devresi eşlemesi arasında oluşturulmuş bir hızlı rota bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7fac1-103">Updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="7fac1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fac1-104">SYNTAX</span></span>

### <span data-ttu-id="7fac1-105">ByExpressRouteConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7fac1-105">ByExpressRouteConnectionName (Default)</span></span>
```
Set-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-AuthorizationKey <String>] [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fac1-106">Byexpressrouteconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="7fac1-106">ByExpressRouteConnectionResourceId</span></span>
```
Set-AzExpressRouteConnection -ResourceId <String> [-AuthorizationKey <String>] [-RoutingWeight <UInt32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fac1-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="7fac1-107">ByExpressRouteConnectionObject</span></span>
```
Set-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-AuthorizationKey <String>]
 [-RoutingWeight <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fac1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fac1-108">DESCRIPTION</span></span>
<span data-ttu-id="7fac1-109">**Set-AzExpressRouteConnection** cmdlet 'i, bir hızlı rota ağ geçidi ile şirket içi hızlı rota devresi eşlemesi arasında oluşturulmuş bir hızlı rota bağlantısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7fac1-109">The **Set-AzExpressRouteConnection** cmdlet updates an express route connection created between an express route gateway and on-premise express route circuit peering.</span></span>

## <span data-ttu-id="7fac1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fac1-110">EXAMPLES</span></span>

### <span data-ttu-id="7fac1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7fac1-111">Example 1</span></span>

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

<span data-ttu-id="7fac1-112">Yukarıdaki, Azure 'daki "testRG" kaynak grubunda Batı ABD 'de bir kaynak grubu, sanal WAN, sanal ağ, sanal hub ve bir ExpressRouteSite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7fac1-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a ExpressRouteSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="7fac1-113">Daha sonra 2 ölçekli birim içeren sanal hub 'da bir ExpressRoute ağ geçidi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7fac1-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="7fac1-114">Ağ Geçidi oluşturulduktan sonra, New-AzExpressRouteConnection komutunu kullanarak şirket içi ExpressRoute devresi ile bağlantılıdır.</span><span class="sxs-lookup"><span data-stu-id="7fac1-114">Once the gateway has been created, it is connected to the on premise ExpressRoute circuit peering using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="7fac1-115">Bağlantı daha sonra Set-AzExpressRouteConnection komutu kullanılarak farklı bir RoutingWeight olacak şekilde güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7fac1-115">The connection is then updated to have a different RoutingWeight by using the Set-AzExpressRouteConnection command.</span></span>

## <span data-ttu-id="7fac1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fac1-116">PARAMETERS</span></span>

### <span data-ttu-id="7fac1-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="7fac1-117">-AsJob</span></span>
<span data-ttu-id="7fac1-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7fac1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fac1-119">-AuthorizationKey</span><span class="sxs-lookup"><span data-stu-id="7fac1-119">-AuthorizationKey</span></span>
<span data-ttu-id="7fac1-120">ExpressRoute ağ geçidi bağlantısını oluşturmak için kullanılacak yetkilendirme anahtarı.</span><span class="sxs-lookup"><span data-stu-id="7fac1-120">The authorization key to be used to create the ExpressRoute gateway connection.</span></span>

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

### <span data-ttu-id="7fac1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fac1-121">-DefaultProfile</span></span>
<span data-ttu-id="7fac1-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fac1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fac1-123">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="7fac1-123">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="7fac1-124">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7fac1-124">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fac1-125">-InputObject</span></span>
<span data-ttu-id="7fac1-126">Güncelleştirilecek ExpressRouteConenction nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7fac1-126">The ExpressRouteConenction object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fac1-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="7fac1-127">-Name</span></span>
<span data-ttu-id="7fac1-128">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7fac1-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fac1-129">-ResourceGroupName</span></span>
<span data-ttu-id="7fac1-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7fac1-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac1-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7fac1-131">-ResourceId</span></span>
<span data-ttu-id="7fac1-132">Silinecek ExpressRouteConenction nesnesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="7fac1-132">The resource id of the ExpressRouteConenction object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fac1-133">-RoutingWeight</span><span class="sxs-lookup"><span data-stu-id="7fac1-133">-RoutingWeight</span></span>
<span data-ttu-id="7fac1-134">Paket yönlendirme için bu bağlantıya atanması gereken ağırlık.</span><span class="sxs-lookup"><span data-stu-id="7fac1-134">The weight that needs to be assigned to this connection for packet routing.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac1-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="7fac1-135">-Confirm</span></span>
<span data-ttu-id="7fac1-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7fac1-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fac1-137">-WhatIf</span></span>
<span data-ttu-id="7fac1-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fac1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fac1-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7fac1-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fac1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fac1-140">CommonParameters</span></span>
<span data-ttu-id="7fac1-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fac1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fac1-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fac1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fac1-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fac1-143">INPUTS</span></span>

### <span data-ttu-id="7fac1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7fac1-144">System.String</span></span>

### <span data-ttu-id="7fac1-145">Microsoft. Azure. Commands. Network. model. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7fac1-145">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="7fac1-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fac1-146">OUTPUTS</span></span>

### <span data-ttu-id="7fac1-147">Microsoft. Azure. Commands. Network. model. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7fac1-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="7fac1-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fac1-148">NOTES</span></span>

## <span data-ttu-id="7fac1-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fac1-149">RELATED LINKS</span></span>
