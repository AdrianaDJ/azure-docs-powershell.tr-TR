---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098857"
---
# <span data-ttu-id="5f507-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="5f507-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="5f507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f507-102">SYNOPSIS</span></span>
<span data-ttu-id="5f507-103">ExpressRoute devresi eşleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="5f507-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="5f507-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f507-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f507-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f507-105">DESCRIPTION</span></span>
<span data-ttu-id="5f507-106">**Get-Azexpressroute, Peeringconfig** cmdlet 'ı ExpressRoute devresi için bir eşleme ilişkisinin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="5f507-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="5f507-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f507-107">EXAMPLES</span></span>

### <span data-ttu-id="5f507-108">Örnek 1: ExpressRoute devresi için eşleme yapılandırmasını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5f507-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="5f507-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f507-109">PARAMETERS</span></span>

### <span data-ttu-id="5f507-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f507-110">-DefaultProfile</span></span>
<span data-ttu-id="5f507-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f507-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f507-112">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="5f507-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5f507-113">Eşleme yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5f507-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="5f507-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f507-114">-Name</span></span>
<span data-ttu-id="5f507-115">Alınacak eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="5f507-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="5f507-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f507-116">CommonParameters</span></span>
<span data-ttu-id="5f507-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f507-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f507-118">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f507-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f507-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f507-119">INPUTS</span></span>

### <span data-ttu-id="5f507-120">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="5f507-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5f507-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f507-121">OUTPUTS</span></span>

### <span data-ttu-id="5f507-122">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="5f507-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="5f507-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f507-123">NOTES</span></span>

## <span data-ttu-id="5f507-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f507-124">RELATED LINKS</span></span>

[<span data-ttu-id="5f507-125">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="5f507-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5f507-126">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="5f507-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5f507-127">Remove-Azexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="5f507-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="5f507-128">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="5f507-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
