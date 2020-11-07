---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 16f73c81c13740037131e47d03945d475db12ee9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935345"
---
# <span data-ttu-id="19d8f-101">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19d8f-101">New-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="19d8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="19d8f-103">Sanal ağ alt ağı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19d8f-103">Creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="19d8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19d8f-104">SYNTAX</span></span>

### <span data-ttu-id="19d8f-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19d8f-105">SetByResource (Default)</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19d8f-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="19d8f-106">SetByResourceId</span></span>
```
New-AzVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19d8f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="19d8f-107">DESCRIPTION</span></span>
<span data-ttu-id="19d8f-108">**New-AzVirtualNetworkSubnetConfig** cmdlet 'i sanal ağ alt ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19d8f-108">**The New-AzVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="19d8f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19d8f-109">EXAMPLES</span></span>

### <span data-ttu-id="19d8f-110">1: iki alt ağ ve ağ güvenlik grubuyla sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="19d8f-110">1:  Create a virtual network with two subnets and a network security group</span></span>
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

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="19d8f-111">Bu örnek New-AzVirtualSubnetConfig cmdlet 'ini kullanarak iki yeni alt ağ yapılandırması oluşturur ve bunları sanal ağ oluşturmak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="19d8f-111">This example creates two new subnet configurations using the New-AzVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="19d8f-112">New-AzVirtualSubnetConfig şablonu, alt ağın bellekteki gösterimini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19d8f-112">The New-AzVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="19d8f-113">Bu örnekte, Frontenvseçsubnet CıDR 10.0.1.0/24 ve RDP erişimine izin veren bir ağ güvenlik grubuna başvurur.</span><span class="sxs-lookup"><span data-stu-id="19d8f-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="19d8f-114">BackendSubnet CıDR 10.0.2.0/24 ve aynı ağ güvenlik grubuna başvuru içerir.</span><span class="sxs-lookup"><span data-stu-id="19d8f-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="19d8f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19d8f-115">PARAMETERS</span></span>

### <span data-ttu-id="19d8f-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="19d8f-116">-AddressPrefix</span></span>
<span data-ttu-id="19d8f-117">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d8f-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="19d8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d8f-118">-DefaultProfile</span></span>
<span data-ttu-id="19d8f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19d8f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19d8f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="19d8f-120">-Name</span></span>
<span data-ttu-id="19d8f-121">Oluşturulacak alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d8f-121">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="19d8f-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="19d8f-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="19d8f-123">Bir NetworkSecurityGroup nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d8f-123">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="19d8f-124">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="19d8f-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="19d8f-125">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d8f-125">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="19d8f-126">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="19d8f-126">-RouteTable</span></span>
<span data-ttu-id="19d8f-127">Alt ağ yapılandırmasıyla ilişkili yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d8f-127">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="19d8f-128">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="19d8f-128">-RouteTableId</span></span>
<span data-ttu-id="19d8f-129">Alt ağ yapılandırmasıyla ilişkili yol tablosunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="19d8f-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="19d8f-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="19d8f-130">-ServiceEndpoint</span></span>
<span data-ttu-id="19d8f-131">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="19d8f-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="19d8f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d8f-132">CommonParameters</span></span>
<span data-ttu-id="19d8f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19d8f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d8f-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d8f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d8f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19d8f-135">INPUTS</span></span>

## <span data-ttu-id="19d8f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19d8f-136">OUTPUTS</span></span>

### <span data-ttu-id="19d8f-137">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="19d8f-137">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="19d8f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19d8f-138">NOTES</span></span>

## <span data-ttu-id="19d8f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19d8f-139">RELATED LINKS</span></span>

[<span data-ttu-id="19d8f-140">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19d8f-140">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="19d8f-141">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19d8f-141">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="19d8f-142">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19d8f-142">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="19d8f-143">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="19d8f-143">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


