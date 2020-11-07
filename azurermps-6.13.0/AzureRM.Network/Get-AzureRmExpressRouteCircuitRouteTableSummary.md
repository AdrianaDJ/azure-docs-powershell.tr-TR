---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: aa3d229ec14118b87c960e234a00cf82f85754c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764627"
---
# <span data-ttu-id="679f4-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="679f4-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="679f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679f4-102">SYNOPSIS</span></span>
<span data-ttu-id="679f4-103">ExpressRoute devrenin yol tablosu özetini alır.</span><span class="sxs-lookup"><span data-stu-id="679f4-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="679f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="679f4-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="679f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="679f4-105">DESCRIPTION</span></span>
<span data-ttu-id="679f4-106">**Get-Azurermexpressroutedevresi Routetablesummary** cmdlet 'i, belirli bir YÖNLENDIRME bağlamının BGP komşu bilgilerinin özetini alır.</span><span class="sxs-lookup"><span data-stu-id="679f4-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="679f4-107">Bu bilgiler, yönlendirme bağlamının ne kadar sürdüğünü ve eşleme yönlendiricisi tarafından tanıtılan yol öneklerinin sayısını belirlemek için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="679f4-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="679f4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="679f4-108">EXAMPLES</span></span>

### <span data-ttu-id="679f4-109">Örnek 1: birincil yolun yol özetini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="679f4-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="679f4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="679f4-110">PARAMETERS</span></span>

### <span data-ttu-id="679f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679f4-111">-DefaultProfile</span></span>
<span data-ttu-id="679f4-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="679f4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="679f4-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="679f4-113">-DevicePath</span></span>
<span data-ttu-id="679f4-114">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="679f4-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679f4-115">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="679f4-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="679f4-116">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="679f4-116">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="679f4-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="679f4-117">-PeeringType</span></span>
<span data-ttu-id="679f4-118">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="679f4-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679f4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679f4-119">-ResourceGroupName</span></span>
<span data-ttu-id="679f4-120">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="679f4-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="679f4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679f4-121">CommonParameters</span></span>
<span data-ttu-id="679f4-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="679f4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679f4-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="679f4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679f4-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="679f4-124">INPUTS</span></span>

### <span data-ttu-id="679f4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="679f4-125">System.String</span></span>

## <span data-ttu-id="679f4-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="679f4-126">OUTPUTS</span></span>

### <span data-ttu-id="679f4-127">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Kabatestablesummary</span><span class="sxs-lookup"><span data-stu-id="679f4-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="679f4-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="679f4-128">NOTES</span></span>

## <span data-ttu-id="679f4-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="679f4-129">RELATED LINKS</span></span>

[<span data-ttu-id="679f4-130">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="679f4-130">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="679f4-131">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="679f4-131">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="679f4-132">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="679f4-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
