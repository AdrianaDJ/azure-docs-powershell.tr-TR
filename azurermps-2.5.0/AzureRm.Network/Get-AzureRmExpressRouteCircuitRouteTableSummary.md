---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
ms.openlocfilehash: bf358159ef7f8895fa2f801435716ac13635a5d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939123"
---
# <span data-ttu-id="31fc6-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="31fc6-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="31fc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31fc6-102">SYNOPSIS</span></span>
<span data-ttu-id="31fc6-103">ExpressRoute devrenin yol tablosu özetini alır.</span><span class="sxs-lookup"><span data-stu-id="31fc6-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31fc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31fc6-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31fc6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31fc6-105">DESCRIPTION</span></span>
<span data-ttu-id="31fc6-106">**Get-Azurermexpressroutedevresi Routetablesummary** cmdlet 'i, belirli bir YÖNLENDIRME bağlamının BGP komşu bilgilerinin özetini alır.</span><span class="sxs-lookup"><span data-stu-id="31fc6-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="31fc6-107">Bu bilgiler, yönlendirme bağlamının ne kadar sürdüğünü ve eşleme yönlendiricisi tarafından tanıtılan yol öneklerinin sayısını belirlemek için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="31fc6-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="31fc6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31fc6-108">EXAMPLES</span></span>

### <span data-ttu-id="31fc6-109">Örnek 1: birincil yolun yol özetini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="31fc6-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="31fc6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31fc6-110">PARAMETERS</span></span>

### <span data-ttu-id="31fc6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31fc6-111">-DefaultProfile</span></span>
<span data-ttu-id="31fc6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31fc6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31fc6-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="31fc6-113">-DevicePath</span></span>
<span data-ttu-id="31fc6-114">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="31fc6-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="31fc6-115">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="31fc6-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="31fc6-116">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="31fc6-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="31fc6-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="31fc6-117">-PeeringType</span></span>
<span data-ttu-id="31fc6-118">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="31fc6-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="31fc6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31fc6-119">-ResourceGroupName</span></span>
<span data-ttu-id="31fc6-120">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="31fc6-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="31fc6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31fc6-121">CommonParameters</span></span>
<span data-ttu-id="31fc6-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31fc6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31fc6-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31fc6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31fc6-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31fc6-124">INPUTS</span></span>

## <span data-ttu-id="31fc6-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31fc6-125">OUTPUTS</span></span>

### <span data-ttu-id="31fc6-126">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Kabatestablesummary</span><span class="sxs-lookup"><span data-stu-id="31fc6-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="31fc6-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31fc6-127">NOTES</span></span>

## <span data-ttu-id="31fc6-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31fc6-128">RELATED LINKS</span></span>

[<span data-ttu-id="31fc6-129">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="31fc6-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="31fc6-130">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="31fc6-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="31fc6-131">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="31fc6-131">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
