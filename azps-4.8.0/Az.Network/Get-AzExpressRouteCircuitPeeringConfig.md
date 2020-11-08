---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266583"
---
# <span data-ttu-id="ec320-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="ec320-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="ec320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec320-102">SYNOPSIS</span></span>
<span data-ttu-id="ec320-103">ExpressRoute devresi eşleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ec320-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="ec320-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec320-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec320-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec320-105">DESCRIPTION</span></span>
<span data-ttu-id="ec320-106">**Get-Azexpressroute, Peeringconfig** cmdlet 'ı ExpressRoute devresi için bir eşleme ilişkisinin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ec320-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ec320-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec320-107">EXAMPLES</span></span>

### <span data-ttu-id="ec320-108">Örnek 1: ExpressRoute devresi için eşleme yapılandırmasını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ec320-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="ec320-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec320-109">PARAMETERS</span></span>

### <span data-ttu-id="ec320-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec320-110">-DefaultProfile</span></span>
<span data-ttu-id="ec320-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec320-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec320-112">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="ec320-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ec320-113">Eşleme yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ec320-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="ec320-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec320-114">-Name</span></span>
<span data-ttu-id="ec320-115">Alınacak eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ec320-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="ec320-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec320-116">CommonParameters</span></span>
<span data-ttu-id="ec320-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec320-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec320-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec320-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec320-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec320-119">INPUTS</span></span>

### <span data-ttu-id="ec320-120">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="ec320-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ec320-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec320-121">OUTPUTS</span></span>

### <span data-ttu-id="ec320-122">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="ec320-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="ec320-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec320-123">NOTES</span></span>

## <span data-ttu-id="ec320-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec320-124">RELATED LINKS</span></span>

[<span data-ttu-id="ec320-125">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="ec320-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ec320-126">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="ec320-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ec320-127">Remove-Azexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="ec320-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="ec320-128">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="ec320-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
