---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 09a3457127646c28c96007532f0e83d1dc1232f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589432"
---
# <span data-ttu-id="482a1-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="482a1-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="482a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="482a1-102">SYNOPSIS</span></span>
<span data-ttu-id="482a1-103">Sanal ağ ağ geçidinden IP yapılandırmasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="482a1-103">Removes an IP Configuration from a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="482a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="482a1-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="482a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="482a1-105">DESCRIPTION</span></span>
<span data-ttu-id="482a1-106">Sanal ağ ağ geçidinden IP yapılandırmasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="482a1-106">Removes an IP Configuration from a Virtual Network Gateway</span></span>

## <span data-ttu-id="482a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="482a1-107">EXAMPLES</span></span>

### <span data-ttu-id="482a1-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="482a1-108">Example 1:</span></span>
```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway $gateway -Name ActiveActive

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

## <span data-ttu-id="482a1-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="482a1-109">PARAMETERS</span></span>

### <span data-ttu-id="482a1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482a1-110">-DefaultProfile</span></span>
<span data-ttu-id="482a1-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="482a1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="482a1-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="482a1-112">-Name</span></span>
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

### <span data-ttu-id="482a1-113">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="482a1-113">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="482a1-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="482a1-114">-Confirm</span></span>
<span data-ttu-id="482a1-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="482a1-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="482a1-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="482a1-116">-WhatIf</span></span>
<span data-ttu-id="482a1-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="482a1-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="482a1-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="482a1-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="482a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482a1-119">CommonParameters</span></span>
<span data-ttu-id="482a1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="482a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482a1-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="482a1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482a1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="482a1-122">INPUTS</span></span>

### <span data-ttu-id="482a1-123">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="482a1-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="482a1-124">Parametreler: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="482a1-124">Parameters: VirtualNetworkGateway (ByValue)</span></span>

## <span data-ttu-id="482a1-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="482a1-125">OUTPUTS</span></span>

### <span data-ttu-id="482a1-126">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="482a1-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="482a1-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="482a1-127">NOTES</span></span>

## <span data-ttu-id="482a1-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="482a1-128">RELATED LINKS</span></span>
