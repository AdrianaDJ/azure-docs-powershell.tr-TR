---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 9c36025f6de4ef6e6168bf5578d09d577cc4f46b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918012"
---
# <span data-ttu-id="67ff7-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="67ff7-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="67ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="67ff7-103">Sanal ağ ağ geçidinden IP yapılandırmasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="67ff7-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="67ff7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67ff7-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67ff7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="67ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="67ff7-106">Sanal ağ ağ geçidinden IP yapılandırmasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="67ff7-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="67ff7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67ff7-107">EXAMPLES</span></span>

### <span data-ttu-id="67ff7-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="67ff7-108">Example 1:</span></span>
```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

Name                   : myGateway
ResourceGroupName      : myRG
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft
                         .Network/virtualNetworkGateways/VNet8GW
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
IpConfigurations       : [
                           {
                             "PrivateIpAllocationMethod": "Dynamic",
                             "Subnet": {
                               "Id": "/subscriptions/800000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/virtualNetworks/VNet8/subnets/GatewaySubnet"
                             },
                             "PublicIpAddress": {
                               "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provid
                         ers/Microsoft.Network/publicIPAddresses/VNet8GWIP"
                             },
                             "Name": "gwipconfig1",
                             "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/provider
                         s/Microsoft.Network/virtualNetworkGateways/VNet8GW/ipConfigurations/gwipconfig1"
                           }
                         ]
GatewayType            : Vpn
VpnType                : RouteBased
EnableBgp              : False
ActiveActive           : True
GatewayDefaultSite     : null
Sku                    : {
                           "Capacity": 2,
                           "Name": "VpnGw1",
                           "Tier": "VpnGw1"
                         }
VpnClientConfiguration : null
BgpSettings            : {
                           "Asn": 65515,
                           "BgpPeeringAddress": "192.0.2.4,192.0.2.5",
                           "PeerWeight": 0
                         }
```

## <span data-ttu-id="67ff7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67ff7-109">PARAMETERS</span></span>

### <span data-ttu-id="67ff7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ff7-110">-DefaultProfile</span></span>
<span data-ttu-id="67ff7-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67ff7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67ff7-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="67ff7-112">-Name</span></span>
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

### <span data-ttu-id="67ff7-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67ff7-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="67ff7-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="67ff7-114">-Confirm</span></span>
<span data-ttu-id="67ff7-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67ff7-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ff7-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ff7-116">-WhatIf</span></span>
<span data-ttu-id="67ff7-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67ff7-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ff7-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67ff7-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ff7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ff7-119">CommonParameters</span></span>
<span data-ttu-id="67ff7-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67ff7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ff7-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ff7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ff7-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67ff7-122">INPUTS</span></span>

### <span data-ttu-id="67ff7-123">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67ff7-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="67ff7-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67ff7-124">OUTPUTS</span></span>

### <span data-ttu-id="67ff7-125">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="67ff7-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="67ff7-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67ff7-126">NOTES</span></span>

## <span data-ttu-id="67ff7-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67ff7-127">RELATED LINKS</span></span>

[<span data-ttu-id="67ff7-128">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="67ff7-128">Add-AzVirtualNetworkGatewayIpConfig</span></span>](./Add-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="67ff7-129">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="67ff7-129">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)