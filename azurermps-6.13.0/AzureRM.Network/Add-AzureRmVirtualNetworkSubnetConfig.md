---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 1129b24c69dc362ea4d700be28a0823afa860885
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764347"
---
# <span data-ttu-id="81c46-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="81c46-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="81c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81c46-102">SYNOPSIS</span></span>
<span data-ttu-id="81c46-103">Sanal ağa alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="81c46-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81c46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81c46-104">SYNTAX</span></span>

### <span data-ttu-id="81c46-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="81c46-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81c46-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="81c46-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork>
 -AddressPrefix <System.Collections.Generic.List`1[System.String]> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-ServiceEndpointPolicy <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]>]
 [-Delegation <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81c46-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="81c46-107">DESCRIPTION</span></span>
<span data-ttu-id="81c46-108">**Add-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i mevcut bir Azure sanal ağına alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="81c46-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="81c46-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81c46-109">EXAMPLES</span></span>

### <span data-ttu-id="81c46-110">1: var olan bir sanal ağa alt ağ ekleme</span><span class="sxs-lookup"><span data-stu-id="81c46-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="81c46-111">Bu örnek ilk olarak, oluşturulacak kaynakların kapsayıcısı olarak bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81c46-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="81c46-112">Ardından bir alt ağ yapılandırması oluşturur ve sanal bir ağ oluşturmak için bu yapılandırmayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="81c46-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="81c46-113">Ardından Add-AzureRmVirtualNetworkSubnetConfig sanal ağın bellekteki gösterimine alt ağ eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="81c46-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="81c46-114">Set-AzureRmVirtualNetwork komutu, varolan sanal ağı yeni alt ağla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="81c46-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

### <span data-ttu-id="81c46-115">2: var olan sanal ağa eklenen bir alt ağa temsilci ekleme</span><span class="sxs-lookup"><span data-stu-id="81c46-115">2: Add a delegation to a subnet being added to an existing virtual network</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> Add-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.2.0/24" -Delegation $delegation | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="81c46-116">Bu örnek ilk olarak mevcut bir VNET alır.</span><span class="sxs-lookup"><span data-stu-id="81c46-116">This example first gets an existing vnet.</span></span>
<span data-ttu-id="81c46-117">Ardından bellekte bir temsilci nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81c46-117">Then, it creates a delegation object in memory.</span></span>
<span data-ttu-id="81c46-118">Son olarak, bu temsilciyle VNET 'e eklenen yeni bir alt ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="81c46-118">Finally, it creates a new subnet with that delegation that is added to the vnet.</span></span> <span data-ttu-id="81c46-119">Değiştirilen yapılandırma sunucuya gönderilir.</span><span class="sxs-lookup"><span data-stu-id="81c46-119">The modified configuration is then sent to the server.</span></span>

## <span data-ttu-id="81c46-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81c46-120">PARAMETERS</span></span>

### <span data-ttu-id="81c46-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="81c46-121">-AddressPrefix</span></span>
<span data-ttu-id="81c46-122">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c46-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c46-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c46-123">-DefaultProfile</span></span>
<span data-ttu-id="81c46-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81c46-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c46-125">-Temsilci</span><span class="sxs-lookup"><span data-stu-id="81c46-125">-Delegation</span></span>
<span data-ttu-id="81c46-126">Bu alt ağda işlemleri gerçekleştirme izni olan hizmetlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="81c46-126">List of services that have permission to perform operations on this subnet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSDelegation]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c46-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="81c46-127">-Name</span></span>
<span data-ttu-id="81c46-128">Eklenecek alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c46-128">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="81c46-129">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="81c46-129">-NetworkSecurityGroup</span></span>
<span data-ttu-id="81c46-130">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c46-130">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="81c46-131">Bu cmdlet, bu parametrenin belirttiği nesneye sanal ağ alt ağı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="81c46-131">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="81c46-132">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="81c46-132">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="81c46-133">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c46-133">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="81c46-134">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="81c46-134">-RouteTable</span></span>
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

### <span data-ttu-id="81c46-135">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="81c46-135">-RouteTableId</span></span>
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

### <span data-ttu-id="81c46-136">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="81c46-136">-ServiceEndpoint</span></span>
<span data-ttu-id="81c46-137">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="81c46-137">Service Endpoint Value</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c46-138">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="81c46-138">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="81c46-139">Hizmet uç noktası Ilkeleri</span><span class="sxs-lookup"><span data-stu-id="81c46-139">Service Endpoint Policies</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81c46-140">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81c46-140">-VirtualNetwork</span></span>
<span data-ttu-id="81c46-141">Alt ağ yapılandırmasının ekleneceği **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c46-141">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="81c46-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c46-142">CommonParameters</span></span>
<span data-ttu-id="81c46-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81c46-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c46-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c46-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c46-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81c46-145">INPUTS</span></span>

### <span data-ttu-id="81c46-146">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81c46-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="81c46-147">System. String</span><span class="sxs-lookup"><span data-stu-id="81c46-147">System.String</span></span>

### <span data-ttu-id="81c46-148">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="81c46-148">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="81c46-149">Microsoft. Azure. Commands. Network. modeller. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="81c46-149">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="81c46-150">System. Koleksiyonlar. Generic. LIST ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="81c46-150">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="81c46-151">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSServiceEndpointPolicy, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="81c46-151">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="81c46-152">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.Azure.Commands.Network.Models.PSDeleme, Microsoft. Azure. Commands. Network, Version = 6.7.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="81c46-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSDelegation, Microsoft.Azure.Commands.Network, Version=6.7.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="81c46-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81c46-153">OUTPUTS</span></span>

### <span data-ttu-id="81c46-154">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81c46-154">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="81c46-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81c46-155">NOTES</span></span>

## <span data-ttu-id="81c46-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81c46-156">RELATED LINKS</span></span>

[<span data-ttu-id="81c46-157">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="81c46-157">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="81c46-158">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="81c46-158">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="81c46-159">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="81c46-159">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="81c46-160">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="81c46-160">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


