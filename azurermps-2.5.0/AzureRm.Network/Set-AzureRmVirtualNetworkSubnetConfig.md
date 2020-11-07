---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: b13a06fbc2bd7f071888dcd0504d3e1963cbedd8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939868"
---
# <span data-ttu-id="1a778-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1a778-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="1a778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a778-102">SYNOPSIS</span></span>
<span data-ttu-id="1a778-103">Sanal ağdaki bir alt ağ yapılandırmasının hedef durumunu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="1a778-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a778-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a778-104">SYNTAX</span></span>

### <span data-ttu-id="1a778-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a778-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a778-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="1a778-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a778-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a778-107">DESCRIPTION</span></span>
<span data-ttu-id="1a778-108">**Set-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağındaki alt ağ yapılandırması için hedef durumu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="1a778-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="1a778-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a778-109">EXAMPLES</span></span>

### <span data-ttu-id="1a778-110">1: alt ağın adres önekini değiştirme</span><span class="sxs-lookup"><span data-stu-id="1a778-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="1a778-111">Bu örnek, bir alt ağ içeren sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a778-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="1a778-112">Ardından, alt ağın Adresspredüzeltmesini değiştirmek için Set-AzureRmVirtualNetworkSubnetConfig çağrılarınız.</span><span class="sxs-lookup"><span data-stu-id="1a778-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="1a778-113">Bu yalnızca sanal ağın bellekteki gösterimini etkiler.</span><span class="sxs-lookup"><span data-stu-id="1a778-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="1a778-114">Azure 'daki sanal ağı değiştirmek için Set-AzureRmVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="1a778-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="1a778-115">2: alt ağa ağ güvenlik grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="1a778-115">2: Add a network security group to a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow 
    -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName 
    TestResourceGroup -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix 
    "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="1a778-116">Bu örnek, tek bir alt ağ içeren bir sanal ağ içeren bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a778-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="1a778-117">Ardından RDP trafiği için izin verme kuralıyla bir ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a778-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="1a778-118">Set-AzureRmVirtualNetworkSubnetConfig cmdlet 'i, yeni oluşturulan ağ güvenlik grubuna işaret eden ön uç alt ağın bellekteki gösterimini değiştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a778-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="1a778-119">Ardından, değiştirilmiş durumu hizmete geri yazmak için Set-AzureRmVirtualNetwork cmdlet çağırılır.</span><span class="sxs-lookup"><span data-stu-id="1a778-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="1a778-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a778-120">PARAMETERS</span></span>

### <span data-ttu-id="1a778-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1a778-121">-AddressPrefix</span></span>
<span data-ttu-id="1a778-122">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a778-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="1a778-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a778-123">-DefaultProfile</span></span>
<span data-ttu-id="1a778-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a778-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a778-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a778-125">-Name</span></span>
<span data-ttu-id="1a778-126">Bu cmdlet 'in yapılandırdığı alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a778-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="1a778-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1a778-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1a778-128">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a778-128">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a778-129">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="1a778-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="1a778-130">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a778-130">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a778-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1a778-131">-RouteTable</span></span>
<span data-ttu-id="1a778-132">Ağ güvenlik grubuyla ilişkili yol tablosu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a778-132">Specifies the route table object that is associated with the network security group.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a778-133">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="1a778-133">-RouteTableId</span></span>
<span data-ttu-id="1a778-134">Ağ güvenlik grubuyla ilişkili yol tablosu nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a778-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a778-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1a778-135">-ServiceEndpoint</span></span>
<span data-ttu-id="1a778-136">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="1a778-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="1a778-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1a778-137">-VirtualNetwork</span></span>
<span data-ttu-id="1a778-138">Alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a778-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a778-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a778-139">CommonParameters</span></span>
<span data-ttu-id="1a778-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a778-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a778-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a778-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a778-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a778-142">INPUTS</span></span>

### <span data-ttu-id="1a778-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1a778-143">PSVirtualNetwork</span></span>
<span data-ttu-id="1a778-144">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1a778-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="1a778-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a778-145">OUTPUTS</span></span>

### <span data-ttu-id="1a778-146">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1a778-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="1a778-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a778-147">NOTES</span></span>

## <span data-ttu-id="1a778-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a778-148">RELATED LINKS</span></span>

[<span data-ttu-id="1a778-149">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1a778-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1a778-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1a778-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1a778-151">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1a778-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1a778-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1a778-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


