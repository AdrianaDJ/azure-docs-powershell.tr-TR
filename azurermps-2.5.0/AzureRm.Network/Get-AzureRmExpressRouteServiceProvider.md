---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
ms.openlocfilehash: 7e4febe620b8a440d1f9a5eb0c9432da9ff47c74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939330"
---
# <span data-ttu-id="99efb-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="99efb-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="99efb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99efb-102">SYNOPSIS</span></span>
<span data-ttu-id="99efb-103">List ExpressRoute hizmet sağlayıcılarını ve özniteliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="99efb-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99efb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99efb-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99efb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99efb-105">DESCRIPTION</span></span>
<span data-ttu-id="99efb-106">**Get-AzureRmExpressRouteServiceProvider** cmdlet 'i, bir List ExpressRoute hizmet sağlayıcılarını ve özniteliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="99efb-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="99efb-107">Öznitelik, konum ve bant genişliği seçeneklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="99efb-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="99efb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99efb-108">EXAMPLES</span></span>

### <span data-ttu-id="99efb-109">Örnek 1: "Silicon Valley" içindeki konumlara sahip hizmet sağlayıcısının listesini alma</span><span class="sxs-lookup"><span data-stu-id="99efb-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="99efb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99efb-110">PARAMETERS</span></span>

### <span data-ttu-id="99efb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99efb-111">-DefaultProfile</span></span>
<span data-ttu-id="99efb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99efb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99efb-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99efb-113">CommonParameters</span></span>
<span data-ttu-id="99efb-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99efb-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99efb-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99efb-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99efb-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99efb-116">INPUTS</span></span>

## <span data-ttu-id="99efb-117">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99efb-117">OUTPUTS</span></span>

### <span data-ttu-id="99efb-118">Microsoft. Azure. Commands. Network. model. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="99efb-118">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="99efb-119">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99efb-119">NOTES</span></span>

## <span data-ttu-id="99efb-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99efb-120">RELATED LINKS</span></span>

[<span data-ttu-id="99efb-121">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="99efb-121">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="99efb-122">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="99efb-122">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="99efb-123">Get-Azurermexpressroutedevresi Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="99efb-123">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="99efb-124">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="99efb-124">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)