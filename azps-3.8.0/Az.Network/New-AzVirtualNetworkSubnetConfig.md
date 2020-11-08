---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 144d04172f3169075a32c5e8111a90ff407532b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098707"
---
# <span data-ttu-id="7305a-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7305a-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="7305a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7305a-102">SYNOPSIS</span></span>
<span data-ttu-id="7305a-103">Sanal ağ alt ağı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7305a-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="7305a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7305a-104">SYNTAX</span></span>

### <span data-ttu-id="7305a-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7305a-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7305a-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="7305a-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String[]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ResourceId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-PrivateEndpointNetworkPoliciesFlag <String>] [-PrivateLinkServiceNetworkPoliciesFlag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7305a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7305a-107">DESCRIPTION</span></span>
<span data-ttu-id="7305a-108">**New-AzVirtualNetworkSubnetConfig** cmdlet 'i sanal ağ alt ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7305a-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="7305a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7305a-109">EXAMPLES</span></span>

### <span data-ttu-id="7305a-110">1: iki alt ağ ve ağ güvenlik grubuyla sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="7305a-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

$pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" `
   -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"

$natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" `
   -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip

$natGatewaySubnet = New-AzVirtualNetworkSubnetConfig -Name natGatewaySubnet `
   -AddressPrefix "10.0.3.0/24" -InputObject $natGateway

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet,$natGatewaySubnet
```

<span data-ttu-id="7305a-111">Bu örnek New-AzVirtualSubnetConfig cmdlet 'ini kullanarak iki yeni alt ağ yapılandırması oluşturur ve bunları sanal ağ oluşturmak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="7305a-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="7305a-112">New-AzVirtualSubnetConfig şablonu, alt ağın bellekteki gösterimini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7305a-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="7305a-113">Bu örnekte, Frontenvseçsubnet CıDR 10.0.1.0/24 ve RDP erişimine izin veren bir ağ güvenlik grubuna başvurur.</span><span class="sxs-lookup"><span data-stu-id="7305a-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="7305a-114">BackendSubnet CıDR 10.0.2.0/24 ve aynı ağ güvenlik grubuna başvuru içerir.</span><span class="sxs-lookup"><span data-stu-id="7305a-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="7305a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7305a-115">PARAMETERS</span></span>

### <span data-ttu-id="7305a-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7305a-116">-AddressPrefix</span></span>
<span data-ttu-id="7305a-117">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7305a-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="7305a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7305a-118">-DefaultProfile</span></span>
<span data-ttu-id="7305a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7305a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7305a-120">-Temsilci</span><span class="sxs-lookup"><span data-stu-id="7305a-120">-Delegation</span></span>
<span data-ttu-id="7305a-121">Bu alt ağda işlemleri gerçekleştirme izni olan hizmetlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="7305a-121">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="7305a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7305a-122">-InputObject</span></span>
<span data-ttu-id="7305a-123">Alt ağ yapılandırmasıyla ilişkili NAT ağ geçidini belirtir</span><span class="sxs-lookup"><span data-stu-id="7305a-123">Specifies the nat gateway associated with the subnet configuration</span></span>

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

### <span data-ttu-id="7305a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7305a-124">-Name</span></span>
<span data-ttu-id="7305a-125">Oluşturulacak alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7305a-125">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="7305a-126">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7305a-126">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7305a-127">Bir NetworkSecurityGroup nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7305a-127">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="7305a-128">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="7305a-128">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="7305a-129">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7305a-129">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="7305a-130">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="7305a-130">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="7305a-131">Alt ağdaki özel uç noktada ağ ilkelerini uygulamayı etkinleştirmek veya devre dışı bırakmak için yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7305a-131">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="7305a-132">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="7305a-132">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="7305a-133">Alt ağdaki özel bağlantı hizmetinde ağ ilkelerini uygulamayı etkinleştirmek veya devre dışı bırakmak için yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7305a-133">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="7305a-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7305a-134">-ResourceId</span></span>
<span data-ttu-id="7305a-135">Alt ağ yapılandırmasıyla ilişkili NAT ağ geçidi kaynağının kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7305a-135">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="7305a-136">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7305a-136">-RouteTable</span></span>
<span data-ttu-id="7305a-137">Alt ağ yapılandırmasıyla ilişkili yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7305a-137">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="7305a-138">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="7305a-138">-RouteTableId</span></span>
<span data-ttu-id="7305a-139">Alt ağ yapılandırmasıyla ilişkili yol tablosunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7305a-139">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="7305a-140">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7305a-140">-ServiceEndpoint</span></span>
<span data-ttu-id="7305a-141">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="7305a-141">Service Endpoint Value</span></span>

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

### <span data-ttu-id="7305a-142">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7305a-142">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="7305a-143">Hizmet uç noktası Ilkeleri</span><span class="sxs-lookup"><span data-stu-id="7305a-143">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="7305a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7305a-144">CommonParameters</span></span>
<span data-ttu-id="7305a-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7305a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7305a-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7305a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7305a-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7305a-147">INPUTS</span></span>

### <span data-ttu-id="7305a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="7305a-148">System.String</span></span>

### <span data-ttu-id="7305a-149">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7305a-149">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="7305a-150">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7305a-150">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="7305a-151">Microsoft. Azure. Commands. Network. modeller. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="7305a-151">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="7305a-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="7305a-152">System.String[]</span></span>

### <span data-ttu-id="7305a-153">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="7305a-153">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="7305a-154">Microsoft.Azure.Commands.Network.Models.PSD.</span><span class="sxs-lookup"><span data-stu-id="7305a-154">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="7305a-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7305a-155">OUTPUTS</span></span>

### <span data-ttu-id="7305a-156">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="7305a-156">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="7305a-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7305a-157">NOTES</span></span>

## <span data-ttu-id="7305a-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7305a-158">RELATED LINKS</span></span>

[<span data-ttu-id="7305a-159">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7305a-159">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7305a-160">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7305a-160">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7305a-161">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7305a-161">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7305a-162">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7305a-162">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)