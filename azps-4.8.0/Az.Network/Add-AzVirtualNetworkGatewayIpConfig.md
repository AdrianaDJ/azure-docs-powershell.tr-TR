---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: f8de9ce0aab60aad729d990c233acfaf75ae50b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268527"
---
# <span data-ttu-id="d46ef-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d46ef-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="d46ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d46ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d46ef-103">Sanal ağ geçidine IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="d46ef-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="d46ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d46ef-104">SYNTAX</span></span>

### <span data-ttu-id="d46ef-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d46ef-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d46ef-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d46ef-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46ef-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d46ef-107">DESCRIPTION</span></span>
<span data-ttu-id="d46ef-108">**Add-AzVirtualNetworkGatewayIpConfig** cmdlet 'i sanal ağ GEÇIDINE bir IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="d46ef-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="d46ef-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d46ef-109">EXAMPLES</span></span>

### <span data-ttu-id="d46ef-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d46ef-110">Example 1</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gw -Name GWIPConfig2 -Subnet $subnet -PublicIpAddress $gwpip2


Name                   : VNet7GW
ResourceGroupName      : VPNGatewayV3
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW
Etag                   : W/"d27a784f-3c3f-4150-863d-764649b6e8e7"
ResourceGuid           : 3c2478a7-d5d4-4e80-8532-7ea2ad577598
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworks/Vnet7/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/VNet7GW_IP"
                             },
                             "Name": "default",
                             "Etag": "W/\"d27a784f-3c3f-4150-863d-764649b6e8e7\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/virtualNetworkGateways/VNet7GW/ipConfigurations/default"
                           },
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VPNGatewayV3/providers/Microsoft.Network/publicIPAddresses/delIPConfig"
                             },
                             "Name": "GWIPConfig2",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroupNotSet/providers/Microsoft.Network/virtualNetworkGateways/VirtualNetworkGatewayNameNotSet/virtualNetworkGatewayIpConfiguration/GWIPConfig2"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : True
ActiveActive           : False
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65534,
                           "BgpPeeringAddress": "10.7.255.254",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="d46ef-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d46ef-111">PARAMETERS</span></span>

### <span data-ttu-id="d46ef-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46ef-112">-DefaultProfile</span></span>
<span data-ttu-id="d46ef-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d46ef-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d46ef-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="d46ef-114">-Name</span></span>
<span data-ttu-id="d46ef-115">Eklenecek ağ geçidi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d46ef-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="d46ef-116">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="d46ef-116">-PrivateIpAddress</span></span>
<span data-ttu-id="d46ef-117">Özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d46ef-117">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ef-118">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="d46ef-118">-PublicIpAddress</span></span>
<span data-ttu-id="d46ef-119">Genel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d46ef-119">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ef-120">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="d46ef-120">-PublicIpAddressId</span></span>
<span data-ttu-id="d46ef-121">Genel IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d46ef-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ef-122">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="d46ef-122">-Subnet</span></span>
<span data-ttu-id="d46ef-123">**Pssubnet** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d46ef-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ef-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d46ef-124">-SubnetId</span></span>
<span data-ttu-id="d46ef-125">Alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d46ef-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ef-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d46ef-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d46ef-127">**Psvirtualnetworkgateway** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d46ef-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="d46ef-128">Bu cmdlet belirttiğiniz **Psvirtualnetworkgateway** nesnesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d46ef-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="d46ef-129">**Psvirtualnetworkgateway** nesnesini almak için Get-AzVirtualNetworkGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d46ef-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d46ef-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="d46ef-130">-Confirm</span></span>
<span data-ttu-id="d46ef-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d46ef-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46ef-132">-WhatIf</span></span>
<span data-ttu-id="d46ef-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d46ef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46ef-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d46ef-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d46ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46ef-135">CommonParameters</span></span>
<span data-ttu-id="d46ef-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d46ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46ef-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46ef-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46ef-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d46ef-138">INPUTS</span></span>

### <span data-ttu-id="d46ef-139">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d46ef-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d46ef-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d46ef-140">OUTPUTS</span></span>

### <span data-ttu-id="d46ef-141">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d46ef-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d46ef-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d46ef-142">NOTES</span></span>

## <span data-ttu-id="d46ef-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d46ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="d46ef-144">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d46ef-144">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d46ef-145">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d46ef-145">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="d46ef-146">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="d46ef-146">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)
