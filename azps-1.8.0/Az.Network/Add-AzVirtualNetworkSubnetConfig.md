---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1df94cc14191fcb95e271bf5fef6b1a09fa77060
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760682"
---
# <span data-ttu-id="dad80-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dad80-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="dad80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad80-102">SYNOPSIS</span></span>
<span data-ttu-id="dad80-103">Sanal ağa alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="dad80-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="dad80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dad80-104">SYNTAX</span></span>

### <span data-ttu-id="dad80-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dad80-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dad80-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="dad80-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String[]>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>] [-ServiceEndpoint <String[]>]
 [-ServiceEndpointPolicy <PSServiceEndpointPolicy[]>] [-Delegation <PSDelegation[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dad80-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dad80-107">DESCRIPTION</span></span>
<span data-ttu-id="dad80-108">**Add-AzVirtualNetworkSubnetConfig** cmdlet 'i mevcut bir Azure sanal ağına alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="dad80-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="dad80-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dad80-109">EXAMPLES</span></span>

### <span data-ttu-id="dad80-110">1: var olan bir sanal ağa alt ağ ekleme</span><span class="sxs-lookup"><span data-stu-id="dad80-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="dad80-111">Bu örnek ilk olarak, oluşturulacak kaynakların kapsayıcısı olarak bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dad80-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="dad80-112">Ardından bir alt ağ yapılandırması oluşturur ve sanal bir ağ oluşturmak için bu yapılandırmayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="dad80-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="dad80-113">Ardından Add-AzVirtualNetworkSubnetConfig sanal ağın bellekteki gösterimine alt ağ eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dad80-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="dad80-114">Set-AzVirtualNetwork komutu, varolan sanal ağı yeni alt ağla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dad80-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="dad80-115">2: var olan sanal ağa eklenen bir alt ağa temsilci ekleme</span><span class="sxs-lookup"><span data-stu-id="dad80-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzVirtualNetwork
```

<span data-ttu-id="dad80-116">Bu örnek ilk olarak mevcut bir VNET alır.</span><span class="sxs-lookup"><span data-stu-id="dad80-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="dad80-117">Ardından bellekte bir temsilci nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dad80-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="dad80-118">Son olarak, bu temsilciyle VNET 'e eklenen yeni bir alt ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dad80-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="dad80-119">Değiştirilen yapılandırma sunucuya gönderilir.</span><span class="sxs-lookup"><span data-stu-id="dad80-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="dad80-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dad80-120">PARAMETERS</span></span>

### <span data-ttu-id="dad80-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="dad80-121">-AddressPrefix</span></span>
<span data-ttu-id="dad80-122">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dad80-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="dad80-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad80-123">-DefaultProfile</span></span>
<span data-ttu-id="dad80-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dad80-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dad80-125">-Temsilci</span><span class="sxs-lookup"><span data-stu-id="dad80-125">-Delegation</span></span>
<span data-ttu-id="dad80-126">Bu alt ağda işlemleri gerçekleştirme izni olan hizmetlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="dad80-126">List of services that have permission to perform operations on this subnet.</span></span>

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

### <span data-ttu-id="dad80-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="dad80-127">-Name</span></span>
<span data-ttu-id="dad80-128">Eklenecek alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dad80-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="dad80-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dad80-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="dad80-130">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dad80-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="dad80-131">Bu cmdlet, bu parametrenin belirttiği nesneye sanal ağ alt ağı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="dad80-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="dad80-132">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="dad80-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="dad80-133">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dad80-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="dad80-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="dad80-134">-RouteTable</span></span>
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

### <span data-ttu-id="dad80-135">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="dad80-135">-RouteTableId</span></span>
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

### <span data-ttu-id="dad80-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="dad80-136">-ServiceEndpoint</span></span>
<span data-ttu-id="dad80-137">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="dad80-137">Service Endpoint Value</span></span>

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

### <span data-ttu-id="dad80-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="dad80-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="dad80-139">Hizmet uç noktası Ilkeleri</span><span class="sxs-lookup"><span data-stu-id="dad80-139">Service Endpoint Policies</span></span>

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

### <span data-ttu-id="dad80-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dad80-140">-VirtualNetwork</span></span>
<span data-ttu-id="dad80-141">Alt ağ yapılandırmasının ekleneceği **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dad80-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="dad80-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad80-142">CommonParameters</span></span>
<span data-ttu-id="dad80-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dad80-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad80-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad80-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad80-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dad80-145">INPUTS</span></span>

### <span data-ttu-id="dad80-146">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dad80-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="dad80-147">System. String</span><span class="sxs-lookup"><span data-stu-id="dad80-147">System.String</span></span>

### <span data-ttu-id="dad80-148">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dad80-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="dad80-149">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="dad80-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="dad80-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="dad80-150">System.String[]</span></span>

### <span data-ttu-id="dad80-151">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy []</span><span class="sxs-lookup"><span data-stu-id="dad80-151">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy[]</span></span>

### <span data-ttu-id="dad80-152">Microsoft.Azure.Commands.Network.Models.PSD.</span><span class="sxs-lookup"><span data-stu-id="dad80-152">Microsoft.Azure.Commands.Network.Models.PSDelegation[]</span></span>

## <span data-ttu-id="dad80-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dad80-153">OUTPUTS</span></span>

### <span data-ttu-id="dad80-154">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dad80-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="dad80-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dad80-155">NOTES</span></span>

## <span data-ttu-id="dad80-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dad80-156">RELATED LINKS</span></span>

[<span data-ttu-id="dad80-157">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dad80-157">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dad80-158">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dad80-158">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dad80-159">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dad80-159">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dad80-160">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dad80-160">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
