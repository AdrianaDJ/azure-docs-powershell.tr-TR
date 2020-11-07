---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9c52ff23d4e92af0d1f62cdfc5d5fda01b3221da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935550"
---
# <span data-ttu-id="349c3-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="349c3-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="349c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="349c3-102">SYNOPSIS</span></span>
<span data-ttu-id="349c3-103">ExpressRoute devresi eşleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="349c3-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="349c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="349c3-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="349c3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="349c3-105">DESCRIPTION</span></span>
<span data-ttu-id="349c3-106">**Get-Azexpressroute, Peeringconfig** cmdlet 'ı ExpressRoute devresi için bir eşleme ilişkisinin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="349c3-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="349c3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="349c3-107">EXAMPLES</span></span>

### <span data-ttu-id="349c3-108">Örnek 1: ExpressRoute devresi için eşleme yapılandırmasını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="349c3-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="349c3-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="349c3-109">PARAMETERS</span></span>

### <span data-ttu-id="349c3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349c3-110">-DefaultProfile</span></span>
<span data-ttu-id="349c3-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="349c3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="349c3-112">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="349c3-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="349c3-113">Eşleme yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="349c3-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="349c3-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="349c3-114">-Name</span></span>
<span data-ttu-id="349c3-115">Alınacak eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="349c3-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="349c3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349c3-116">CommonParameters</span></span>
<span data-ttu-id="349c3-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="349c3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349c3-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="349c3-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349c3-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="349c3-119">INPUTS</span></span>

### <span data-ttu-id="349c3-120">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="349c3-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="349c3-121">' Expressroutedevresi ' parametresi, ardışık düzenin ' Psexpressroutedevresi ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="349c3-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="349c3-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="349c3-122">OUTPUTS</span></span>

### <span data-ttu-id="349c3-123">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="349c3-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="349c3-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="349c3-124">NOTES</span></span>

## <span data-ttu-id="349c3-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="349c3-125">RELATED LINKS</span></span>

[<span data-ttu-id="349c3-126">Add-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="349c3-126">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="349c3-127">Yeni-Azexpressroute, Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="349c3-127">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="349c3-128">Remove-Azexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="349c3-128">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="349c3-129">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="349c3-129">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
