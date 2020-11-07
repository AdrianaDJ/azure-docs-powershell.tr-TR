---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
ms.openlocfilehash: 883d2ae51046f3dc1ee6c8350d996fedbfff083e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939530"
---
# <span data-ttu-id="c49e5-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c49e5-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="c49e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c49e5-102">SYNOPSIS</span></span>
<span data-ttu-id="c49e5-103">ExpressRoute devresi bir yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="c49e5-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c49e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c49e5-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c49e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c49e5-105">DESCRIPTION</span></span>
<span data-ttu-id="c49e5-106">**Get-Azurermexpressroutedevresi** bir ExpressRoute devresi ayrıntılı yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="c49e5-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="c49e5-107">Yol tablosu tüm rotaları gösterir veya belirli bir eşleme türü için rotaları gösterecek şekilde filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="c49e5-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="c49e5-108">Yol tablosunu kullanarak, eşleme yapılandırmanızı ve bağlantınızı doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c49e5-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="c49e5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c49e5-109">EXAMPLES</span></span>

### <span data-ttu-id="c49e5-110">Örnek 1: birincil yolun yol tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="c49e5-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="c49e5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c49e5-111">PARAMETERS</span></span>

### <span data-ttu-id="c49e5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49e5-112">-DefaultProfile</span></span>
<span data-ttu-id="c49e5-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c49e5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c49e5-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="c49e5-114">-DevicePath</span></span>
<span data-ttu-id="c49e5-115">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="c49e5-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: DevicePathEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c49e5-116">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="c49e5-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="c49e5-117">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="c49e5-117">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c49e5-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c49e5-118">-PeeringType</span></span>
<span data-ttu-id="c49e5-119">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c49e5-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c49e5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49e5-120">-ResourceGroupName</span></span>
<span data-ttu-id="c49e5-121">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c49e5-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c49e5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49e5-122">CommonParameters</span></span>
<span data-ttu-id="c49e5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c49e5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49e5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c49e5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49e5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c49e5-125">INPUTS</span></span>

## <span data-ttu-id="c49e5-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c49e5-126">OUTPUTS</span></span>

### <span data-ttu-id="c49e5-127">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Routestable</span><span class="sxs-lookup"><span data-stu-id="c49e5-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="c49e5-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c49e5-128">NOTES</span></span>

## <span data-ttu-id="c49e5-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c49e5-129">RELATED LINKS</span></span>

[<span data-ttu-id="c49e5-130">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="c49e5-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="c49e5-131">Get-Azurermexpressroutedevresi Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="c49e5-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="c49e5-132">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="c49e5-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
