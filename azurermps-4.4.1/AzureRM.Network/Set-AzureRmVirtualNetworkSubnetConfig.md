---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D1D51DEF-05DE-45C4-9013-A02A5B248EAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 179bfced7b73113899f525940114abb342e61f8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764258"
---
# <span data-ttu-id="1ba04-101">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ba04-101">Set-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="1ba04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ba04-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba04-103">Sanal ağdaki bir alt ağ yapılandırmasının hedef durumunu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="1ba04-103">Configures the goal state for a subnet configuration in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ba04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ba04-104">SYNTAX</span></span>

### <span data-ttu-id="1ba04-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ba04-105">SetByResource (Default)</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ba04-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="1ba04-106">SetByResourceId</span></span>
```
Set-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ba04-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ba04-107">DESCRIPTION</span></span>
<span data-ttu-id="1ba04-108">**Set-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i, bir Azure sanal ağındaki alt ağ yapılandırması için hedef durumu yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="1ba04-108">The **Set-AzureRmVirtualNetworkSubnetConfig** cmdlet configures the goal state for a subnet configuration in an Azure virtual network.</span></span>

## <span data-ttu-id="1ba04-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ba04-109">EXAMPLES</span></span>

### <span data-ttu-id="1ba04-110">1: alt ağın adres önekini değiştirme</span><span class="sxs-lookup"><span data-stu-id="1ba04-110">1: Modify the address prefix of a subnet</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup    
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet

Set-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.3.0/23"

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="1ba04-111">Bu örnek, bir alt ağ içeren sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ba04-111">This example creates a virtual network with one subnet.</span></span> <span data-ttu-id="1ba04-112">Ardından, alt ağın Adresspredüzeltmesini değiştirmek için Set-AzureRmVirtualNetworkSubnetConfig çağrılarınız.</span><span class="sxs-lookup"><span data-stu-id="1ba04-112">Then is calls Set-AzureRmVirtualNetworkSubnetConfig to modify the AddressPrefix of the subnet.</span></span> <span data-ttu-id="1ba04-113">Bu yalnızca sanal ağın bellekteki gösterimini etkiler.</span><span class="sxs-lookup"><span data-stu-id="1ba04-113">This only impacts the in-memory representation of the virtual network.</span></span> <span data-ttu-id="1ba04-114">Azure 'daki sanal ağı değiştirmek için Set-AzureRmVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="1ba04-114">Set-AzureRmVirtualNetwork is then called to modify the virtual network in Azure.</span></span>

### <span data-ttu-id="1ba04-115">2: alt ağa ağ güvenlik grubu ekleme</span><span class="sxs-lookup"><span data-stu-id="1ba04-115">2: Add a network security group to a subnet</span></span>
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

<span data-ttu-id="1ba04-116">Bu örnek, tek bir alt ağ içeren bir sanal ağ içeren bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ba04-116">This example creates a resource group with one virtual network containing just one subnet.</span></span> <span data-ttu-id="1ba04-117">Ardından RDP trafiği için izin verme kuralıyla bir ağ güvenlik grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ba04-117">It then creates a network security group with an allow rule for RDP traffic.</span></span> <span data-ttu-id="1ba04-118">Set-AzureRmVirtualNetworkSubnetConfig cmdlet 'i, yeni oluşturulan ağ güvenlik grubuna işaret eden ön uç alt ağın bellekteki gösterimini değiştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1ba04-118">The Set-AzureRmVirtualNetworkSubnetConfig cmdlet is used to modify the in-memory representation of the frontend subnet so that it points to the newly created network security group.</span></span> <span data-ttu-id="1ba04-119">Ardından, değiştirilmiş durumu hizmete geri yazmak için Set-AzureRmVirtualNetwork cmdlet çağırılır.</span><span class="sxs-lookup"><span data-stu-id="1ba04-119">The Set-AzureRmVirtualNetwork cmdlet is then called to write the modified state back to the service.</span></span>

## <span data-ttu-id="1ba04-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ba04-120">PARAMETERS</span></span>

### <span data-ttu-id="1ba04-121">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1ba04-121">-AddressPrefix</span></span>
<span data-ttu-id="1ba04-122">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba04-122">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="1ba04-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ba04-123">-Name</span></span>
<span data-ttu-id="1ba04-124">Bu cmdlet 'in yapılandırdığı alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba04-124">Specifies the name of a subnet configuration that this cmdlet configures.</span></span>

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

### <span data-ttu-id="1ba04-125">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1ba04-125">-NetworkSecurityGroup</span></span>
<span data-ttu-id="1ba04-126">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba04-126">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="1ba04-127">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="1ba04-127">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="1ba04-128">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba04-128">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="1ba04-129">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="1ba04-129">-RouteTable</span></span>
<span data-ttu-id="1ba04-130">Ağ güvenlik grubuyla ilişkili yol tablosu nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba04-130">Specifies the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="1ba04-131">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="1ba04-131">-RouteTableId</span></span>
<span data-ttu-id="1ba04-132">Ağ güvenlik grubuyla ilişkili yol tablosu nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba04-132">Specifies the ID of the route table object that is associated with the network security group.</span></span>

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

### <span data-ttu-id="1ba04-133">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ba04-133">-ServiceEndpoint</span></span>
<span data-ttu-id="1ba04-134">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="1ba04-134">Service Endpoint Value</span></span>

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

### <span data-ttu-id="1ba04-135">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ba04-135">-VirtualNetwork</span></span>
<span data-ttu-id="1ba04-136">Alt ağ yapılandırmasını içeren **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ba04-136">Specifies the **VirtualNetwork** object that contains the subnet configuration.</span></span>

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

### <span data-ttu-id="1ba04-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba04-137">-DefaultProfile</span></span>
<span data-ttu-id="1ba04-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ba04-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ba04-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba04-139">CommonParameters</span></span>
<span data-ttu-id="1ba04-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ba04-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba04-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba04-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba04-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ba04-142">INPUTS</span></span>

### <span data-ttu-id="1ba04-143">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ba04-143">PSVirtualNetwork</span></span>
<span data-ttu-id="1ba04-144">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1ba04-144">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="1ba04-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ba04-145">OUTPUTS</span></span>

### <span data-ttu-id="1ba04-146">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ba04-146">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="1ba04-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ba04-147">NOTES</span></span>

## <span data-ttu-id="1ba04-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ba04-148">RELATED LINKS</span></span>

[<span data-ttu-id="1ba04-149">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ba04-149">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1ba04-150">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ba04-150">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1ba04-151">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ba04-151">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="1ba04-152">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="1ba04-152">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)


