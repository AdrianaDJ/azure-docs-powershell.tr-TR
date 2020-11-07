---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B8B632B5-9D3B-4352-B4C8-49C00472B3A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworksubnetconfig
schema: 2.0.0
ms.openlocfilehash: 9f1f4f916ea0756ebf034c12e1e9f92f3cd3c865
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940111"
---
# <span data-ttu-id="61883-101">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="61883-101">Add-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="61883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61883-102">SYNOPSIS</span></span>
<span data-ttu-id="61883-103">Sanal ağa alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="61883-103">Adds a subnet configuration to a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61883-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61883-104">SYNTAX</span></span>

### <span data-ttu-id="61883-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61883-105">SetByResource (Default)</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-RouteTable <PSRouteTable>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61883-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="61883-106">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkSubnetConfig -Name <String> -VirtualNetwork <PSVirtualNetwork> -AddressPrefix <String>
 [-NetworkSecurityGroupId <String>] [-RouteTableId <String>]
 [-ServiceEndpoint <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61883-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="61883-107">DESCRIPTION</span></span>
<span data-ttu-id="61883-108">**Add-AzureRmVirtualNetworkSubnetConfig** cmdlet 'i mevcut bir Azure sanal ağına alt ağ yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="61883-108">The **Add-AzureRmVirtualNetworkSubnetConfig** cmdlet adds a subnet configuration to an existing Azure virtual network.</span></span>

## <span data-ttu-id="61883-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61883-109">EXAMPLES</span></span>

### <span data-ttu-id="61883-110">1: var olan bir sanal ağa alt ağ ekleme</span><span class="sxs-lookup"><span data-stu-id="61883-110">1: Add a subnet to an existing virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Add-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork -AddressPrefix "10.0.2.0/24"
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

  <span data-ttu-id="61883-111">Bu örnek ilk olarak, oluşturulacak kaynakların kapsayıcısı olarak bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61883-111">This example first creates a resource group as a container of the resources to be created.</span></span> <span data-ttu-id="61883-112">Ardından bir alt ağ yapılandırması oluşturur ve sanal bir ağ oluşturmak için bu yapılandırmayı kullanır.</span><span class="sxs-lookup"><span data-stu-id="61883-112">It then creates a subnet configuration and uses it to create a virtual network.</span></span> <span data-ttu-id="61883-113">Ardından Add-AzureRmVirtualNetworkSubnetConfig sanal ağın bellekteki gösterimine alt ağ eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="61883-113">The Add-AzureRmVirtualNetworkSubnetConfig is then used to add a subnet to the in-memory representation of the virtual network.</span></span> <span data-ttu-id="61883-114">Set-AzureRmVirtualNetwork komutu, varolan sanal ağı yeni alt ağla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="61883-114">The Set-AzureRmVirtualNetwork command updates the existing virtual network with the new subnet.</span></span>

## <span data-ttu-id="61883-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61883-115">PARAMETERS</span></span>

### <span data-ttu-id="61883-116">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="61883-116">-AddressPrefix</span></span>
<span data-ttu-id="61883-117">Alt ağ yapılandırması için IP adresi aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61883-117">Specifies a range of IP addresses for a subnet configuration.</span></span>

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

### <span data-ttu-id="61883-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61883-118">-DefaultProfile</span></span>
<span data-ttu-id="61883-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61883-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61883-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="61883-120">-Name</span></span>
<span data-ttu-id="61883-121">Eklenecek alt ağ yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61883-121">Specifies the name of the subnet configuration to add.</span></span>

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

### <span data-ttu-id="61883-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="61883-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="61883-123">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61883-123">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="61883-124">Bu cmdlet, bu parametrenin belirttiği nesneye sanal ağ alt ağı yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="61883-124">This cmdlet adds a virtual network subnet configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="61883-125">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="61883-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="61883-126">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="61883-126">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="61883-127">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="61883-127">-RouteTable</span></span>
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

### <span data-ttu-id="61883-128">-Routetableıd</span><span class="sxs-lookup"><span data-stu-id="61883-128">-RouteTableId</span></span>
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

### <span data-ttu-id="61883-129">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="61883-129">-ServiceEndpoint</span></span>
<span data-ttu-id="61883-130">Hizmet uç noktası değeri</span><span class="sxs-lookup"><span data-stu-id="61883-130">Service Endpoint Value</span></span>

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

### <span data-ttu-id="61883-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="61883-131">-VirtualNetwork</span></span>
<span data-ttu-id="61883-132">Alt ağ yapılandırmasının ekleneceği **VirtualNetwork** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61883-132">Specifies the **VirtualNetwork** object in which to add a subnet configuration.</span></span>

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

### <span data-ttu-id="61883-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61883-133">CommonParameters</span></span>
<span data-ttu-id="61883-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61883-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61883-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61883-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61883-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61883-136">INPUTS</span></span>

### <span data-ttu-id="61883-137">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="61883-137">PSVirtualNetwork</span></span>
<span data-ttu-id="61883-138">' VirtualNetwork ' parametresi ardışık düzen için ' PSVirtualNetwork ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="61883-138">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="61883-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61883-139">OUTPUTS</span></span>

### <span data-ttu-id="61883-140">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="61883-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="61883-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61883-141">NOTES</span></span>

## <span data-ttu-id="61883-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61883-142">RELATED LINKS</span></span>

[<span data-ttu-id="61883-143">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="61883-143">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="61883-144">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="61883-144">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="61883-145">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="61883-145">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="61883-146">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="61883-146">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


