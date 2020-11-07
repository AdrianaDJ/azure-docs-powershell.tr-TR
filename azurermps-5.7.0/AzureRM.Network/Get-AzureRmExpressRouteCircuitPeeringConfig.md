---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 223f2a02dcf6d2310109b41587126f374a6733b1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765202"
---
# <span data-ttu-id="8443d-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="8443d-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="8443d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8443d-102">SYNOPSIS</span></span>
<span data-ttu-id="8443d-103">ExpressRoute devresi eşleme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="8443d-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8443d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8443d-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8443d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8443d-105">DESCRIPTION</span></span>
<span data-ttu-id="8443d-106">**Get-Azurermexpressroutedevresi Peeringconfig** cmdlet 'ı ExpressRoute devresi için bir eşleme ilişkisinin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="8443d-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="8443d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8443d-107">EXAMPLES</span></span>

### <span data-ttu-id="8443d-108">Örnek 1: ExpressRoute devresi için eşleme yapılandırmasını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8443d-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="8443d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8443d-109">PARAMETERS</span></span>

### <span data-ttu-id="8443d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8443d-110">-DefaultProfile</span></span>
<span data-ttu-id="8443d-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8443d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8443d-112">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="8443d-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8443d-113">Eşleme yapılandırmasını içeren ExpressRoute devresi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8443d-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="8443d-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="8443d-114">-Name</span></span>
<span data-ttu-id="8443d-115">Alınacak eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="8443d-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="8443d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8443d-116">CommonParameters</span></span>
<span data-ttu-id="8443d-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8443d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8443d-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8443d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8443d-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8443d-119">INPUTS</span></span>

### <span data-ttu-id="8443d-120">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="8443d-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="8443d-121">' Expressroutedevresi ' parametresi, ardışık düzenin ' Psexpressroutedevresi ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8443d-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="8443d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8443d-122">OUTPUTS</span></span>

### <span data-ttu-id="8443d-123">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="8443d-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="8443d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8443d-124">NOTES</span></span>

## <span data-ttu-id="8443d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8443d-125">RELATED LINKS</span></span>

[<span data-ttu-id="8443d-126">Add-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="8443d-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8443d-127">New-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="8443d-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8443d-128">Remove-Azurermexpressroutedevresi Peeringconfig</span><span class="sxs-lookup"><span data-stu-id="8443d-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="8443d-129">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="8443d-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
