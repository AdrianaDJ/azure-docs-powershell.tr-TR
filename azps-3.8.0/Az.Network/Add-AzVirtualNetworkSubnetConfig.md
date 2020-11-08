---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 4898c20a7771f3f320157085ba767fe44730b5c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098000"
---
# <span data-ttu-id="7d91d-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7d91d-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="7d91d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d91d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d91d-103">Sanal ağa alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="7d91d-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="7d91d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d91d-104">SYNTAX</span></span>

### <span data-ttu-id="7d91d-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d91d-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-InputObject <PSNatGateway>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d91d-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="7d91d-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ResourceId <String>]
 [-ServiceEndpoint <String[]>] [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>]
 [-Delegation <PSDelegation[]>] [-PrivateEndpointNetworkPoliciesFlag <String>]
 [-PrivateLinkServiceNetworkPoliciesFlag <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d91d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d91d-107">DESCRIPTION</span></span>
<span data-ttu-id="7d91d-108">**Add-AzVirtualNetworkSubnetConfig** cmdlet 'i mevcut bir Azure sanal ağına alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="7d91d-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="7d91d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d91d-109">EXAMPLES</span></span>

### <span data-ttu-id="7d91d-110">1: var olan bir sanal ağa alt ağ ekleme</span><span class="sxs-lookup"><span data-stu-id="7d91d-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="7d91d-111">Bu örnek ilk olarak, oluşturulacak kaynakların kapsayıcısı olarak bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d91d-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="7d91d-112">Ardından bir alt ağ yapılandırması oluşturur ve sanal bir ağ oluşturmak için bu yapılandırmayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="7d91d-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="7d91d-113">Ardından Add-AzVirtualNetworkSubnetConfig sanal ağın bellekteki gösterimine alt ağ eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7d91d-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="7d91d-114">Set-AzVirtualNetwork komutu, varolan sanal ağı yeni alt ağla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7d91d-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="7d91d-115">2: var olan sanal ağa eklenen bir alt ağa temsilci ekleme</span><span class="sxs-lookup"><span data-stu-id="7d91d-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="7d91d-116">Bu örnek ilk olarak mevcut bir VNET alır.</span><span class="sxs-lookup"><span data-stu-id="7d91d-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="7d91d-117">Ardından bellekte bir temsilci nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d91d-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="7d91d-118">Son olarak, bu temsilciyle VNET 'e eklenen yeni bir alt ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d91d-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="7d91d-119">Değiştirilen yapılandırma sunucuya gönderilir.</span><span class="sxs-lookup"><span data-stu-id="7d91d-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="7d91d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d91d-120">PARAMETERS</span></span>

### <span data-ttu-id="7d91d-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7d91d-121">-AddressPrefix</span></span>
<span data-ttu-id="7d91d-122">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d91d-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="7d91d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d91d-123">-DefaultProfile</span></span>
<span data-ttu-id="7d91d-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d91d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d91d-125">-Temsilci</span><span class="sxs-lookup"><span data-stu-id="7d91d-125">-Delegation</span></span>
<span data-ttu-id="7d91d-126">Bu alt ağda işlemleri gerçekleştirme izni olan hizmetlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="7d91d-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="7d91d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d91d-127">-InputObject</span></span>
<span data-ttu-id="7d91d-128">Alt ağ yapılandırmasıyla ilişkili NAT ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d91d-128">Specifies the nat gateway associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="7d91d-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d91d-129">-Name</span></span>
<span data-ttu-id="7d91d-130">Eklenecek alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d91d-130">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="7d91d-131">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d91d-131">-NetworkSecurityGroup</span></span>
<span data-ttu-id="7d91d-132">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d91d-132">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="7d91d-133">Bu cmdlet, bu parametrenin belirttiği nesneye sanal ağ alt ağı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="7d91d-133">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d91d-134">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="7d91d-134">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="7d91d-135">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d91d-135">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="7d91d-136">-PrivateEndpointNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="7d91d-136">-PrivateEndpointNetworkPoliciesFlag</span></span>
<span data-ttu-id="7d91d-137">Alt ağdaki özel uç noktada ağ ilkelerini uygulamayı etkinleştirmek veya devre dışı bırakmak için yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7d91d-137">Configure to enable or disable applying network policies on private endpoint in the subnet.</span></span>

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

### <span data-ttu-id="7d91d-138">-PrivateLinkServiceNetworkPoliciesFlag</span><span class="sxs-lookup"><span data-stu-id="7d91d-138">-PrivateLinkServiceNetworkPoliciesFlag</span></span>
<span data-ttu-id="7d91d-139">Alt ağdaki özel bağlantı hizmetinde ağ ilkelerini uygulamayı etkinleştirmek veya devre dışı bırakmak için yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7d91d-139">Configure to enable or disable applying network policies on private link service in the subnet.</span></span>

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

### <span data-ttu-id="7d91d-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7d91d-140">-ResourceId</span></span>
<span data-ttu-id="7d91d-141">Alt ağ yapılandırmasıyla ilişkili NAT ağ geçidi kaynağının kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d91d-141">Specifies the Id of NAT Gateway resource associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="7d91d-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="7d91d-142">-RouteTable</span></span>
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

### <span data-ttu-id="7d91d-143">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="7d91d-143">-RouteTableId</span></span>
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

### <span data-ttu-id="7d91d-144">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d91d-144">-ServiceEndpoint</span></span>
<span data-ttu-id="7d91d-145">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="7d91d-145">Service Endpoint Value</span></span>

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

### <span data-ttu-id="7d91d-146">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="7d91d-146">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="7d91d-147">Hizmet uç noktası Ilkeleri</span><span class="sxs-lookup"><span data-stu-id="7d91d-147">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="7d91d-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7d91d-148">-VirtualNetwork</span></span>
<span data-ttu-id="7d91d-149">Alt ağ yapılandırmasının ekleneceği **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d91d-149">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="7d91d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d91d-150">CommonParameters</span></span>
<span data-ttu-id="7d91d-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d91d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d91d-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7d91d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d91d-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d91d-153">INPUTS</span></span>

### <span data-ttu-id="7d91d-154">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7d91d-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="7d91d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7d91d-155">System.String</span></span>

### <span data-ttu-id="7d91d-156">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7d91d-156">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="7d91d-157">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="7d91d-157">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="7d91d-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="7d91d-158">System.String[]</span></span>

### <span data-ttu-id="7d91d-159">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="7d91d-159">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="7d91d-160">Microsoft.Azure.Commands.Network.Models.PSD.</span><span class="sxs-lookup"><span data-stu-id="7d91d-160">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="7d91d-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d91d-161">OUTPUTS</span></span>

### <span data-ttu-id="7d91d-162">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7d91d-162">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="7d91d-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d91d-163">NOTES</span></span>

## <span data-ttu-id="7d91d-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d91d-164">RELATED LINKS</span></span>

[<span data-ttu-id="7d91d-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7d91d-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7d91d-166">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7d91d-166">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7d91d-167">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7d91d-167">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="7d91d-168">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="7d91d-168">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)