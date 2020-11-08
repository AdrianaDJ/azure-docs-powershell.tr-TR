---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279638"
---
# <span data-ttu-id="92b98-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="92b98-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="92b98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b98-102">SYNOPSIS</span></span>
<span data-ttu-id="92b98-103">ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="92b98-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="92b98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92b98-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92b98-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92b98-105">DESCRIPTION</span></span>
<span data-ttu-id="92b98-106">**Remove-Azexpressroute, Peeringconfig** cmdlet 'ı bir ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="92b98-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="92b98-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92b98-107">EXAMPLES</span></span>

### <span data-ttu-id="92b98-108">Örnek 1: ExpressRoute devresi eşleme yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="92b98-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="92b98-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92b98-109">PARAMETERS</span></span>

### <span data-ttu-id="92b98-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b98-110">-DefaultProfile</span></span>
<span data-ttu-id="92b98-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92b98-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b98-112">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="92b98-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="92b98-113">Kaldırılacak eşleme yapılandırmasını içeren ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="92b98-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="92b98-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="92b98-114">-Name</span></span>
<span data-ttu-id="92b98-115">Kaldırılacak olan eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="92b98-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="92b98-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="92b98-116">-PeerAddressType</span></span>
<span data-ttu-id="92b98-117">Eşün adres ailesi</span><span class="sxs-lookup"><span data-stu-id="92b98-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="92b98-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b98-118">CommonParameters</span></span>
<span data-ttu-id="92b98-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92b98-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b98-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b98-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b98-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92b98-121">INPUTS</span></span>

### <span data-ttu-id="92b98-122">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="92b98-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="92b98-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92b98-123">OUTPUTS</span></span>

### <span data-ttu-id="92b98-124">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="92b98-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="92b98-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92b98-125">NOTES</span></span>

## <span data-ttu-id="92b98-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92b98-126">RELATED LINKS</span></span>

[<span data-ttu-id="92b98-127">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="92b98-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="92b98-128">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="92b98-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="92b98-129">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="92b98-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="92b98-130">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="92b98-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
