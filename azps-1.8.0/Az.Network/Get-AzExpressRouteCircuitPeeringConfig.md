---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c8e821408f3d65ace31ab2340f544a0a47e120e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760599"
---
# <span data-ttu-id="99106-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="99106-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="99106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99106-102">SYNOPSIS</span></span>
<span data-ttu-id="99106-103">ExpressRoute devresi eşleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="99106-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="99106-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99106-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99106-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99106-105">DESCRIPTION</span></span>
<span data-ttu-id="99106-106">**Get-Azexpressroute, Peeringconfig** cmdlet 'ı ExpressRoute devresi için bir eşleme ilişkisinin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="99106-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="99106-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99106-107">EXAMPLES</span></span>

### <span data-ttu-id="99106-108">Örnek 1: ExpressRoute devresi için eşleme yapılandırmasını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="99106-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="99106-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99106-109">PARAMETERS</span></span>

### <span data-ttu-id="99106-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99106-110">-DefaultProfile</span></span>
<span data-ttu-id="99106-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99106-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99106-112">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="99106-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="99106-113">Eşleme yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="99106-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="99106-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="99106-114">-Name</span></span>
<span data-ttu-id="99106-115">Alınacak eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="99106-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="99106-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99106-116">CommonParameters</span></span>
<span data-ttu-id="99106-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99106-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99106-118">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="99106-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99106-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99106-119">INPUTS</span></span>

### <span data-ttu-id="99106-120">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="99106-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="99106-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99106-121">OUTPUTS</span></span>

### <span data-ttu-id="99106-122">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="99106-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="99106-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99106-123">NOTES</span></span>

## <span data-ttu-id="99106-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99106-124">RELATED LINKS</span></span>

[<span data-ttu-id="99106-125">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="99106-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="99106-126">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="99106-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="99106-127">Remove-Azexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="99106-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="99106-128">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="99106-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
