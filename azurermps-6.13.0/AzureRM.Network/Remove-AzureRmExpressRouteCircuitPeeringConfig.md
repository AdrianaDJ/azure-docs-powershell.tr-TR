---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 965ebd3fe81ced04aee88a6f5a9bbd427017a4e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594849"
---
# <span data-ttu-id="93ef9-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="93ef9-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="93ef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="93ef9-103">ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93ef9-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93ef9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="93ef9-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93ef9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="93ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="93ef9-106">**Remove-Azurermexpressroutedevresi Peeringconfig** cmdlet 'ı bir ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="93ef9-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="93ef9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="93ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="93ef9-108">Örnek 1: ExpressRoute devresi eşleme yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="93ef9-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="93ef9-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="93ef9-109">PARAMETERS</span></span>

### <span data-ttu-id="93ef9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ef9-110">-DefaultProfile</span></span>
<span data-ttu-id="93ef9-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="93ef9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93ef9-112">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="93ef9-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="93ef9-113">Kaldırılacak eşleme yapılandırmasını içeren ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="93ef9-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="93ef9-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="93ef9-114">-Name</span></span>
<span data-ttu-id="93ef9-115">Kaldırılacak olan eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="93ef9-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="93ef9-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="93ef9-116">-PeerAddressType</span></span>
<span data-ttu-id="93ef9-117">Eşün adres ailesi</span><span class="sxs-lookup"><span data-stu-id="93ef9-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="93ef9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ef9-118">CommonParameters</span></span>
<span data-ttu-id="93ef9-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="93ef9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ef9-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ef9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ef9-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="93ef9-121">INPUTS</span></span>

### <span data-ttu-id="93ef9-122">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="93ef9-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="93ef9-123">Parametreler: Expressroutedevresi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="93ef9-123">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="93ef9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="93ef9-124">OUTPUTS</span></span>

### <span data-ttu-id="93ef9-125">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="93ef9-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="93ef9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="93ef9-126">NOTES</span></span>

## <span data-ttu-id="93ef9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="93ef9-127">RELATED LINKS</span></span>

[<span data-ttu-id="93ef9-128">Add-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="93ef9-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="93ef9-129">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="93ef9-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="93ef9-130">New-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="93ef9-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="93ef9-131">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="93ef9-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
