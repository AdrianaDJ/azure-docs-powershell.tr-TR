---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5a7f842f172ac61722daaeb6f6f4c6d4ef6a33a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594629"
---
# <span data-ttu-id="68bca-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="68bca-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="68bca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68bca-102">SYNOPSIS</span></span>
<span data-ttu-id="68bca-103">ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68bca-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68bca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68bca-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68bca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="68bca-105">DESCRIPTION</span></span>
<span data-ttu-id="68bca-106">**Remove-Azurermexpressroutedevresi Peeringconfig** cmdlet 'ı bir ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="68bca-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="68bca-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68bca-107">EXAMPLES</span></span>

### <span data-ttu-id="68bca-108">Örnek 1: ExpressRoute devresi eşleme yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="68bca-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="68bca-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68bca-109">PARAMETERS</span></span>

### <span data-ttu-id="68bca-110">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="68bca-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="68bca-111">Kaldırılacak eşleme yapılandırmasını içeren ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="68bca-111">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="68bca-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="68bca-112">-Name</span></span>
<span data-ttu-id="68bca-113">Kaldırılacak olan eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="68bca-113">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="68bca-114">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="68bca-114">-PeerAddressType</span></span>
<span data-ttu-id="68bca-115">Eşün adres ailesi</span><span class="sxs-lookup"><span data-stu-id="68bca-115">The Address family of the peering</span></span>

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

### <span data-ttu-id="68bca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68bca-116">-DefaultProfile</span></span>
<span data-ttu-id="68bca-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68bca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68bca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68bca-118">CommonParameters</span></span>
<span data-ttu-id="68bca-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68bca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68bca-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68bca-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68bca-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68bca-121">INPUTS</span></span>

### <span data-ttu-id="68bca-122">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="68bca-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="68bca-123">' Expressroutedevresi ' parametresi, ardışık düzenin ' Psexpressroutedevresi ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="68bca-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="68bca-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68bca-124">OUTPUTS</span></span>

### <span data-ttu-id="68bca-125">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="68bca-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="68bca-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68bca-126">NOTES</span></span>

## <span data-ttu-id="68bca-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68bca-127">RELATED LINKS</span></span>

[<span data-ttu-id="68bca-128">Add-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="68bca-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="68bca-129">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="68bca-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="68bca-130">New-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="68bca-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="68bca-131">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="68bca-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
