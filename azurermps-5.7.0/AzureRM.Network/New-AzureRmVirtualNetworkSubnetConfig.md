---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 901FD38B-67FA-40D5-8D23-51E5544C25D8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: be1b0f81aa33fb0f1368e5730e80f41b9fdcabb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592067"
---
# <span data-ttu-id="fd023-101">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd023-101">New-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="fd023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd023-102">SYNOPSIS</span></span>
<span data-ttu-id="fd023-103">Sanal ağ alt ağı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fd023-103">Creates a virtual network subnet configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd023-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd023-104">SYNTAX</span></span>

### <span data-ttu-id="fd023-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd023-105">SetByResource (Default)</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd023-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="fd023-106">SetByResourceId</span></span>
```
New-AzureRmVirtualNetworkSubnetConfig -Name <String> -AddressPrefix <String> [-NetworkSecurityGroupId <String>]
 [-RouteTableId <String>] [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd023-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd023-107">DESCRIPTION</span></span>
<span data-ttu-id="fd023-108">**Yeni-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i sanal ağ alt ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fd023-108">**The New-AzureRmVirtualNetworkSubnetConfig** cmdlet creates a virtual network subnet configuration.</span></span>

## <span data-ttu-id="fd023-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd023-109">EXAMPLES</span></span>

### <span data-ttu-id="fd023-110">1: iki alt ağ ve ağ güvenlik grubuyla sanal ağ oluşturma</span><span class="sxs-lookup"><span data-stu-id="fd023-110">1:  Create a virtual network with two subnets and a network security group</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus

$rdpRule = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" `
   -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 `
   -SourceAddressPrefix Internet -SourcePortRange * `
   -DestinationAddressPrefix * -DestinationPortRange 3389 
    
$networkSecurityGroup = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestResourceGroup `
  -Location centralus -Name "NSG-FrontEnd" -SecurityRules $rdpRule

$frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet `
    -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet `
    -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup `
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
```

<span data-ttu-id="fd023-111">Bu örnek New-AzureRmVirtualSubnetConfig cmdlet 'ini kullanarak iki yeni alt ağ yapılandırması oluşturur ve bunları sanal ağ oluşturmak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="fd023-111">This example creates two new subnet configurations using the New-AzureRmVirtualSubnetConfig cmdlet, and then uses them to create a virtual network.</span></span> <span data-ttu-id="fd023-112">New-AzureRmVirtualSubnetConfig şablonu, alt ağın bellekteki gösterimini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fd023-112">The New-AzureRmVirtualSubnetConfig template only creates an in-memory representation of the subnet.</span></span> <span data-ttu-id="fd023-113">Bu örnekte, Frontenvseçsubnet CıDR 10.0.1.0/24 ve RDP erişimine izin veren bir ağ güvenlik grubuna başvurur.</span><span class="sxs-lookup"><span data-stu-id="fd023-113">In this example, the frontendSubnet has CIDR 10.0.1.0/24 and references a network security group that allows RDP access.</span></span> <span data-ttu-id="fd023-114">BackendSubnet CıDR 10.0.2.0/24 ve aynı ağ güvenlik grubuna başvuru içerir.</span><span class="sxs-lookup"><span data-stu-id="fd023-114">The backendSubnet has CIDR 10.0.2.0/24 and references the same network security group.</span></span>

## <span data-ttu-id="fd023-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd023-115">PARAMETERS</span></span>

### <span data-ttu-id="fd023-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fd023-116">-AddressPrefix</span></span>
<span data-ttu-id="fd023-117">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd023-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="fd023-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd023-118">-DefaultProfile</span></span>
<span data-ttu-id="fd023-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd023-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd023-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd023-120">-Name</span></span>
<span data-ttu-id="fd023-121">Oluşturulacak alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd023-121">Specifies the name of the subnet configuration to create.</span></span>

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

### <span data-ttu-id="fd023-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fd023-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="fd023-123">Bir NetworkSecurityGroup nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd023-123">Specifies a NetworkSecurityGroup object.</span></span>

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

### <span data-ttu-id="fd023-124">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="fd023-124">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="fd023-125">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd023-125">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="fd023-126">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="fd023-126">-RouteTable</span></span>
<span data-ttu-id="fd023-127">Alt ağ yapılandırmasıyla ilişkili yol tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd023-127">Specifies the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="fd023-128">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="fd023-128">-RouteTableId</span></span>
<span data-ttu-id="fd023-129">Alt ağ yapılandırmasıyla ilişkili yol tablosunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd023-129">Specifies the ID of the route table associated with the subnet configuration.</span></span>

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

### <span data-ttu-id="fd023-130">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="fd023-130">-ServiceEndpoint</span></span>
<span data-ttu-id="fd023-131">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="fd023-131">Service Endpoint Value</span></span>

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

### <span data-ttu-id="fd023-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd023-132">CommonParameters</span></span>
<span data-ttu-id="fd023-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd023-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd023-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd023-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd023-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd023-135">INPUTS</span></span>

### <span data-ttu-id="fd023-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fd023-136">None</span></span>
<span data-ttu-id="fd023-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fd023-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd023-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd023-138">OUTPUTS</span></span>

### <span data-ttu-id="fd023-139">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="fd023-139">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="fd023-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd023-140">NOTES</span></span>

## <span data-ttu-id="fd023-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd023-141">RELATED LINKS</span></span>

[<span data-ttu-id="fd023-142">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd023-142">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="fd023-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd023-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="fd023-144">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd023-144">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="fd023-145">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="fd023-145">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


