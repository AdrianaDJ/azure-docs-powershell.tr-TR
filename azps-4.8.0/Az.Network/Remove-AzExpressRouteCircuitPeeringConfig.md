---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274095"
---
# <span data-ttu-id="a83bb-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a83bb-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a83bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a83bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a83bb-103">ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a83bb-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a83bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a83bb-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a83bb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a83bb-105">DESCRIPTION</span></span>
<span data-ttu-id="a83bb-106">**Remove-Azexpressroute, Peeringconfig** cmdlet 'ı bir ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a83bb-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a83bb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a83bb-107">EXAMPLES</span></span>

### <span data-ttu-id="a83bb-108">Örnek 1: ExpressRoute devresi eşleme yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a83bb-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="a83bb-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a83bb-109">PARAMETERS</span></span>

### <span data-ttu-id="a83bb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a83bb-110">-DefaultProfile</span></span>
<span data-ttu-id="a83bb-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a83bb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a83bb-112">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a83bb-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a83bb-113">Kaldırılacak eşleme yapılandırmasını içeren ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="a83bb-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a83bb-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="a83bb-114">-Name</span></span>
<span data-ttu-id="a83bb-115">Kaldırılacak olan eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="a83bb-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="a83bb-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a83bb-116">-PeerAddressType</span></span>
<span data-ttu-id="a83bb-117">Eşün adres ailesi</span><span class="sxs-lookup"><span data-stu-id="a83bb-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a83bb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83bb-118">CommonParameters</span></span>
<span data-ttu-id="a83bb-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a83bb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83bb-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a83bb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83bb-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a83bb-121">INPUTS</span></span>

### <span data-ttu-id="a83bb-122">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a83bb-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a83bb-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a83bb-123">OUTPUTS</span></span>

### <span data-ttu-id="a83bb-124">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a83bb-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a83bb-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a83bb-125">NOTES</span></span>

## <span data-ttu-id="a83bb-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a83bb-126">RELATED LINKS</span></span>

[<span data-ttu-id="a83bb-127">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="a83bb-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a83bb-128">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a83bb-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a83bb-129">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="a83bb-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a83bb-130">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a83bb-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
