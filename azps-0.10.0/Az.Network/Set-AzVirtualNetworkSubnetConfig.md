---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 73649f0f04cf1de07d991cb454b44308c4ff6443
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936498"
---
# <span data-ttu-id="759d5-101">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="759d5-101">Set-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="759d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="759d5-102">SYNOPSIS</span></span>
<span data-ttu-id="759d5-103">Sanal ağdaki bir alt ağ yapılandırmasının hedef durumunu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="759d5-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

## <span data-ttu-id="759d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="759d5-104">SYNTAX</span></span>

### <span data-ttu-id="759d5-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="759d5-105">SetByResource (Default)</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="759d5-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="759d5-106">SetByResourceId</span></span>
```
Set-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="759d5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="759d5-107">DESCRIPTION</span></span>
<span data-ttu-id="759d5-108">**Set-AzVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağındaki alt ağ yapılandırması için hedef durumu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="759d5-108">The **Set-AzVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="759d5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="759d5-109">EXAMPLES</span></span>

### <span data-ttu-id="759d5-110">1: alt ağın adres önekini değiştirme</span><span class="sxs-lookup"><span data-stu-id="759d5-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="759d5-111">Bu örnek, bir alt ağ içeren sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="759d5-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="759d5-112">Ardından, alt ağın Adresspredüzeltmesini değiştirmek için Set-AzVirtualNetworkSubnetConfig çağrılarınız.</span><span class="sxs-lookup"><span data-stu-id="759d5-112">Then is calls Set-AzVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="759d5-113">Bu yalnızca sanal ağın bellekteki gösterimini etkiler.</span><span class="sxs-lookup"><span data-stu-id="759d5-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="759d5-114">Azure 'daki sanal ağı değiştirmek için Set-AzVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="759d5-114">Set-AzVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="759d5-115">2: alt ağa ağ güvenlik grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="759d5-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="759d5-116">Bu örnek, tek bir alt ağ içeren bir sanal ağ içeren bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="759d5-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="759d5-117">Ardından RDP trafiği için izin verme kuralıyla bir ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="759d5-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="759d5-118">Set-AzVirtualNetworkSubnetConfig cmdlet 'i, yeni oluşturulan ağ güvenlik grubuna işaret eden ön uç alt ağın bellekteki gösterimini değiştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="759d5-118">The Set-AzVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="759d5-119">Ardından, değiştirilmiş durumu hizmete geri yazmak için Set-AzVirtualNetwork cmdlet çağırılır.</span><span class="sxs-lookup"><span data-stu-id="759d5-119">The Set-AzVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="759d5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="759d5-120">PARAMETERS</span></span>

### <span data-ttu-id="759d5-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="759d5-121">-AddressPrefix</span></span>
<span data-ttu-id="759d5-122">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="759d5-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="759d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759d5-123">-DefaultProfile</span></span>
<span data-ttu-id="759d5-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="759d5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="759d5-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="759d5-125">-Name</span></span>
<span data-ttu-id="759d5-126">Bu cmdlet 'in yapılandırdığı alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="759d5-126">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="759d5-127">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="759d5-127">-NetworkSecurityGroup</span></span>
<span data-ttu-id="759d5-128">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="759d5-128">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="759d5-129">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="759d5-129">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="759d5-130">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="759d5-130">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="759d5-131">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="759d5-131">-RouteTable</span></span>
<span data-ttu-id="759d5-132">Ağ güvenlik grubuyla ilişkili yol tablosu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="759d5-132">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="759d5-133">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="759d5-133">-RouteTableId</span></span>
<span data-ttu-id="759d5-134">Ağ güvenlik grubuyla ilişkili yol tablosu nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="759d5-134">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="759d5-135">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="759d5-135">-ServiceEndpoint</span></span>
<span data-ttu-id="759d5-136">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="759d5-136">Service Endpoint Value</span></span>

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

### <span data-ttu-id="759d5-137">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="759d5-137">-VirtualNetwork</span></span>
<span data-ttu-id="759d5-138">Alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="759d5-138">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="759d5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759d5-139">CommonParameters</span></span>
<span data-ttu-id="759d5-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="759d5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759d5-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="759d5-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759d5-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="759d5-142">INPUTS</span></span>

### <span data-ttu-id="759d5-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="759d5-143">PSVirtualNetwork</span></span>
<span data-ttu-id="759d5-144">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="759d5-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="759d5-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="759d5-145">OUTPUTS</span></span>

### <span data-ttu-id="759d5-146">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="759d5-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="759d5-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="759d5-147">NOTES</span></span>

## <span data-ttu-id="759d5-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="759d5-148">RELATED LINKS</span></span>

[<span data-ttu-id="759d5-149">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="759d5-149">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="759d5-150">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="759d5-150">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="759d5-151">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="759d5-151">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="759d5-152">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="759d5-152">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)


