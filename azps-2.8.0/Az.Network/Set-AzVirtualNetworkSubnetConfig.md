---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: ecaf236c04c24241cf285e3d8ca379d3bc52645a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932726"
---
# <span data-ttu-id="5468d-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5468d-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="5468d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5468d-102">SYNOPSIS</span></span>
<span data-ttu-id="5468d-103">Sanal ağın alt ağ yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5468d-103">Updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="5468d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5468d-104">SYNTAX</span></span>

### <span data-ttu-id="5468d-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5468d-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5468d-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="5468d-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5468d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5468d-107">DESCRIPTION</span></span>
<span data-ttu-id="5468d-108">**Set-AzVirtualNetworkSubnetConfig** cmdlet 'i sanal ağın alt ağ yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5468d-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet updates a subnet configuration for a virtual network.</span></span>

## <span data-ttu-id="5468d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5468d-109">EXAMPLES</span></span>

### <span data-ttu-id="5468d-110">1: alt ağın adres önekini değiştirme</span><span class="sxs-lookup"><span data-stu-id="5468d-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="5468d-111">Bu örnek, bir alt ağ içeren sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5468d-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="5468d-112">Ardından, alt ağın Adresspredüzeltmesini değiştirmek için Set-AzVirtualNetworkSubnetConfig çağrılarınız.</span><span class="sxs-lookup"><span data-stu-id="5468d-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="5468d-113">Bu yalnızca sanal ağın bellekteki gösterimini etkiler.</span><span class="sxs-lookup"><span data-stu-id="5468d-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="5468d-114">Azure 'daki sanal ağı değiştirmek için Set-AzVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="5468d-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="5468d-115">2: alt ağa ağ güvenlik grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="5468d-115">2: Add a network security group to a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="5468d-116">Bu örnek, tek bir alt ağ içeren bir sanal ağ içeren bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5468d-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="5468d-117">Ardından RDP trafiği için izin verme kuralıyla bir ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5468d-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="5468d-118">Set-AzVirtualNetworkSubnetConfig cmdlet 'i, yeni oluşturulan ağ güvenlik grubuna işaret eden ön uç alt ağın bellekteki gösterimini değiştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5468d-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="5468d-119">Ardından, değiştirilmiş durumu hizmete geri yazmak için Set-AzVirtualNetwork cmdlet çağırılır.</span><span class="sxs-lookup"><span data-stu-id="5468d-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

### <span data-ttu-id="5468d-120">3: bir alt ağa NAT ağ geçidi ekleme</span><span class="sxs-lookup"><span data-stu-id="5468d-120">3: Attach a Nat Gateway to a subnet</span></span>
```
$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natGateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" 

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -InputObject $natGateway 

$virtualNetwork | Set-AzVirtualNetwork
```

## <span data-ttu-id="5468d-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5468d-121">PARAMETERS</span></span>

### <span data-ttu-id="5468d-122">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5468d-122">-AddressPrefix</span></span>
<span data-ttu-id="5468d-123">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5468d-123">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5468d-124">-DefaultProfile</span></span>
<span data-ttu-id="5468d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5468d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5468d-126">-Temsilci</span><span class="sxs-lookup"><span data-stu-id="5468d-126">-Delegation</span></span>
<span data-ttu-id="5468d-127">Bu alt ağda işlemleri gerçekleştirme izni olan hizmetlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="5468d-127">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSDelegation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5468d-128">-InputObject</span></span>
<span data-ttu-id="5468d-129">Alt ağ yapılandırmasıyla ilişkili NAT ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5468d-129">Specifies the nat gateway associated with the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: SetByResource
Aliases: NatGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="5468d-130">-Name</span></span>
<span data-ttu-id="5468d-131">Bu cmdlet 'in yapılandırdığı alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5468d-131">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-132">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5468d-132">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5468d-133">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5468d-133">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-134">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="5468d-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="5468d-135">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5468d-135">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="5468d-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="5468d-137">Alt ağdaki özel uç noktada ağ ilkelerini uygulamayı etkinleştirmek veya devre dışı bırakmak için yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5468d-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="5468d-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="5468d-139">Alt ağdaki özel bağlantı hizmetinde ağ ilkelerini uygulamayı etkinleştirmek veya devre dışı bırakmak için yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5468d-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5468d-140">-ResourceId</span></span>
<span data-ttu-id="5468d-141">Alt ağ yapılandırmasıyla ilişkili NAT ağ geçidi kaynağının kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5468d-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: NatGatewayId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="5468d-142">-RouteTable</span></span>
<span data-ttu-id="5468d-143">Ağ güvenlik grubuyla ilişkili yol tablosu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5468d-143">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-144">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="5468d-144">-RouteTableId</span></span>
<span data-ttu-id="5468d-145">Ağ güvenlik grubuyla ilişkili yol tablosu nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5468d-145">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-146">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5468d-146">-ServiceEndpoint</span></span>
<span data-ttu-id="5468d-147">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="5468d-147">Service Endpoint Value</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-148">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5468d-148">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="5468d-149">Hizmet uç noktası Ilkeleri</span><span class="sxs-lookup"><span data-stu-id="5468d-149">Service Endpoint Policies</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-150">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5468d-150">-VirtualNetwork</span></span>
<span data-ttu-id="5468d-151">Alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5468d-151">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5468d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5468d-152">CommonParameters</span></span>
<span data-ttu-id="5468d-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5468d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5468d-154">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5468d-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5468d-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5468d-155">INPUTS</span></span>

### <span data-ttu-id="5468d-156">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5468d-156">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="5468d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5468d-157">System.String</span></span>

### <span data-ttu-id="5468d-158">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5468d-158">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="5468d-159">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="5468d-159">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="5468d-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="5468d-160">System.String[]</span></span>

### <span data-ttu-id="5468d-161">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="5468d-161">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="5468d-162">Microsoft.Azure.Commands.Network.Models.PSD.</span><span class="sxs-lookup"><span data-stu-id="5468d-162">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="5468d-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5468d-163">OUTPUTS</span></span>

### <span data-ttu-id="5468d-164">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5468d-164">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="5468d-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5468d-165">NOTES</span></span>

## <span data-ttu-id="5468d-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5468d-166">RELATED LINKS</span></span>

[<span data-ttu-id="5468d-167">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5468d-167">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5468d-168">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5468d-168">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5468d-169">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5468d-169">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="5468d-170">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="5468d-170">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)