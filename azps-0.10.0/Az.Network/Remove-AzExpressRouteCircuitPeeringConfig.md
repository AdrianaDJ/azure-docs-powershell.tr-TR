---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5feeba4ffb4f73365e9b6df86a03e8920b74f88e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935301"
---
# <span data-ttu-id="70c1b-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="70c1b-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="70c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="70c1b-103">ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="70c1b-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="70c1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70c1b-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70c1b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70c1b-105">DESCRIPTION</span></span>
<span data-ttu-id="70c1b-106">**Remove-Azexpressroute, Peeringconfig** cmdlet 'ı bir ExpressRoute devresi eşleme yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="70c1b-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="70c1b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70c1b-107">EXAMPLES</span></span>

### <span data-ttu-id="70c1b-108">Örnek 1: ExpressRoute devresi eşleme yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="70c1b-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="70c1b-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70c1b-109">PARAMETERS</span></span>

### <span data-ttu-id="70c1b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c1b-110">-DefaultProfile</span></span>
<span data-ttu-id="70c1b-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70c1b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c1b-112">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="70c1b-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="70c1b-113">Kaldırılacak eşleme yapılandırmasını içeren ExpressRoute devresi.</span><span class="sxs-lookup"><span data-stu-id="70c1b-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70c1b-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="70c1b-114">-Name</span></span>
<span data-ttu-id="70c1b-115">Kaldırılacak olan eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="70c1b-115">The name of the peering configuration to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c1b-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="70c1b-116">-PeerAddressType</span></span>
<span data-ttu-id="70c1b-117">Eşün adres ailesi</span><span class="sxs-lookup"><span data-stu-id="70c1b-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c1b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c1b-118">CommonParameters</span></span>
<span data-ttu-id="70c1b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70c1b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c1b-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c1b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c1b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70c1b-121">INPUTS</span></span>

### <span data-ttu-id="70c1b-122">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="70c1b-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="70c1b-123">' Expressroutedevresi ' parametresi, ardışık düzenin ' Psexpressroutedevresi ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="70c1b-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="70c1b-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70c1b-124">OUTPUTS</span></span>

### <span data-ttu-id="70c1b-125">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="70c1b-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="70c1b-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70c1b-126">NOTES</span></span>

## <span data-ttu-id="70c1b-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70c1b-127">RELATED LINKS</span></span>

[<span data-ttu-id="70c1b-128">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="70c1b-128">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="70c1b-129">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="70c1b-129">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="70c1b-130">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="70c1b-130">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="70c1b-131">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="70c1b-131">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
