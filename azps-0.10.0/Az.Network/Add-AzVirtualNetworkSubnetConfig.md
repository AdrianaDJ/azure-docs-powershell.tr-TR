---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 01116d3a2ad2636776fe29a0e36e34568624f2c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935616"
---
# <span data-ttu-id="e8b3e-101">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e8b3e-101">Add-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="e8b3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b3e-103">Sanal ağa alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-103">Adds a subnet configuration to a virtual network.</span></span>

## <span data-ttu-id="e8b3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8b3e-104">SYNTAX</span></span>

### <span data-ttu-id="e8b3e-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8b3e-105">SetByResource (Default)</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b3e-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e8b3e-106">SetByResourceId</span></span>
```
Add-AzVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8b3e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8b3e-107">DESCRIPTION</span></span>
<span data-ttu-id="e8b3e-108">**Add-AzVirtualNetworkSubnetConfig** cmdlet 'i mevcut bir Azure sanal ağına alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-108">The **Add-AzVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="e8b3e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8b3e-109">EXAMPLES</span></span>

### <span data-ttu-id="e8b3e-110">1: var olan bir sanal ağa alt ağ ekleme</span><span class="sxs-lookup"><span data-stu-id="e8b3e-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzVirtualNetwork
```

  <span data-ttu-id="e8b3e-111">Bu örnek ilk olarak, oluşturulacak kaynakların kapsayıcısı olarak bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="e8b3e-112">Ardından bir alt ağ yapılandırması oluşturur ve sanal bir ağ oluşturmak için bu yapılandırmayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="e8b3e-113">Ardından Add-AzVirtualNetworkSubnetConfig sanal ağın bellekteki gösterimine alt ağ eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-113">The Add-AzVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="e8b3e-114">Set-AzVirtualNetwork komutu, varolan sanal ağı yeni alt ağla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-114">The Set-AzVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="e8b3e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8b3e-115">PARAMETERS</span></span>

### <span data-ttu-id="e8b3e-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e8b3e-116">-AddressPrefix</span></span>
<span data-ttu-id="e8b3e-117">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="e8b3e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b3e-118">-DefaultProfile</span></span>
<span data-ttu-id="e8b3e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8b3e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8b3e-120">-Name</span></span>
<span data-ttu-id="e8b3e-121">Eklenecek alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="e8b3e-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e8b3e-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="e8b3e-123">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="e8b3e-124">Bu cmdlet, bu parametrenin belirttiği nesneye sanal ağ alt ağı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="e8b3e-125">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="e8b3e-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e8b3e-126">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="e8b3e-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="e8b3e-127">-RouteTable</span></span>
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

### <span data-ttu-id="e8b3e-128">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="e8b3e-128">-RouteTableId</span></span>
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

### <span data-ttu-id="e8b3e-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8b3e-129">-ServiceEndpoint</span></span>
<span data-ttu-id="e8b3e-130">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="e8b3e-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="e8b3e-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e8b3e-131">-VirtualNetwork</span></span>
<span data-ttu-id="e8b3e-132">Alt ağ yapılandırmasının ekleneceği **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="e8b3e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b3e-133">CommonParameters</span></span>
<span data-ttu-id="e8b3e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8b3e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b3e-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8b3e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b3e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8b3e-136">INPUTS</span></span>

### <span data-ttu-id="e8b3e-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e8b3e-137">PSVirtualNetwork</span></span>
<span data-ttu-id="e8b3e-138">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e8b3e-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="e8b3e-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8b3e-139">OUTPUTS</span></span>

### <span data-ttu-id="e8b3e-140">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e8b3e-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="e8b3e-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8b3e-141">NOTES</span></span>

## <span data-ttu-id="e8b3e-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8b3e-142">RELATED LINKS</span></span>

[<span data-ttu-id="e8b3e-143">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e8b3e-143">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e8b3e-144">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e8b3e-144">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e8b3e-145">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e8b3e-145">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="e8b3e-146">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="e8b3e-146">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


