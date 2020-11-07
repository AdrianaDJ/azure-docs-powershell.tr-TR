---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteServiceProvider.md
ms.openlocfilehash: d8d5abedd0deaf5af341995552ad72bef4703058
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762150"
---
# <span data-ttu-id="56ebe-101">Get-AzureRmExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="56ebe-101">Get-AzureRmExpressRouteServiceProvider</span></span>

## <span data-ttu-id="56ebe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="56ebe-103">List ExpressRoute hizmet sağlayıcılarını ve özniteliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="56ebe-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56ebe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56ebe-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56ebe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56ebe-105">DESCRIPTION</span></span>
<span data-ttu-id="56ebe-106">**Get-AzureRmExpressRouteServiceProvider** cmdlet 'i, bir List ExpressRoute hizmet sağlayıcılarını ve özniteliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="56ebe-106">The **Get-AzureRmExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="56ebe-107">Öznitelik, konum ve bant genişliği seçeneklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="56ebe-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="56ebe-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56ebe-108">EXAMPLES</span></span>

### <span data-ttu-id="56ebe-109">Örnek 1: "Silicon Valley" içindeki konumlara sahip hizmet sağlayıcısının listesini alma</span><span class="sxs-lookup"><span data-stu-id="56ebe-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzureRmExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="56ebe-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56ebe-110">PARAMETERS</span></span>

### <span data-ttu-id="56ebe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ebe-111">-DefaultProfile</span></span>
<span data-ttu-id="56ebe-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56ebe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56ebe-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ebe-113">CommonParameters</span></span>
<span data-ttu-id="56ebe-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56ebe-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ebe-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ebe-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ebe-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56ebe-116">INPUTS</span></span>

### <span data-ttu-id="56ebe-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="56ebe-117">None</span></span>
<span data-ttu-id="56ebe-118">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="56ebe-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56ebe-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56ebe-119">OUTPUTS</span></span>

### <span data-ttu-id="56ebe-120">Microsoft. Azure. Commands. Network. model. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="56ebe-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="56ebe-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56ebe-121">NOTES</span></span>

## <span data-ttu-id="56ebe-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56ebe-122">RELATED LINKS</span></span>

[<span data-ttu-id="56ebe-123">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="56ebe-123">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="56ebe-124">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="56ebe-124">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="56ebe-125">Get-Azurermexpressroutedevresi Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="56ebe-125">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="56ebe-126">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="56ebe-126">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
