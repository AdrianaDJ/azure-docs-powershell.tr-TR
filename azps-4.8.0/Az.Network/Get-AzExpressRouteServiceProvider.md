---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274150"
---
# <span data-ttu-id="95eb4-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="95eb4-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="95eb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="95eb4-103">List ExpressRoute hizmet sağlayıcılarını ve özniteliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="95eb4-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="95eb4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95eb4-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95eb4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="95eb4-106">**Get-AzExpressRouteServiceProvider** cmdlet 'i, bir List ExpressRoute hizmet sağlayıcılarını ve özniteliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="95eb4-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="95eb4-107">Öznitelik, konum ve bant genişliği seçeneklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="95eb4-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="95eb4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95eb4-108">EXAMPLES</span></span>

### <span data-ttu-id="95eb4-109">Örnek 1: "Silicon Valley" içindeki konumlara sahip hizmet sağlayıcısının listesini alma</span><span class="sxs-lookup"><span data-stu-id="95eb4-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="95eb4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95eb4-110">PARAMETERS</span></span>

### <span data-ttu-id="95eb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95eb4-111">-DefaultProfile</span></span>
<span data-ttu-id="95eb4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95eb4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95eb4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95eb4-113">CommonParameters</span></span>
<span data-ttu-id="95eb4-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95eb4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95eb4-115">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="95eb4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95eb4-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95eb4-116">INPUTS</span></span>

### <span data-ttu-id="95eb4-117">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="95eb4-117">None</span></span>

## <span data-ttu-id="95eb4-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95eb4-118">OUTPUTS</span></span>

### <span data-ttu-id="95eb4-119">Microsoft. Azure. Commands. Network. model. PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="95eb4-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="95eb4-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95eb4-120">NOTES</span></span>

## <span data-ttu-id="95eb4-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95eb4-121">RELATED LINKS</span></span>

[<span data-ttu-id="95eb4-122">Get-Azexpressroute, Arptable</span><span class="sxs-lookup"><span data-stu-id="95eb4-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="95eb4-123">Get-Azexpressroute, RouteTable</span><span class="sxs-lookup"><span data-stu-id="95eb4-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="95eb4-124">Get-Azexpressroute, Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="95eb4-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="95eb4-125">Get-Azexpressroute, stat</span><span class="sxs-lookup"><span data-stu-id="95eb4-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
