---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: cc3057582876dd3836f6b157a8ee31bb5b232539
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760596"
---
# <span data-ttu-id="b6512-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b6512-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="b6512-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6512-102">SYNOPSIS</span></span>
<span data-ttu-id="b6512-103">ExpressRoute devrenin yol tablosu özetini alır.</span><span class="sxs-lookup"><span data-stu-id="b6512-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="b6512-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6512-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6512-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6512-105">DESCRIPTION</span></span>
<span data-ttu-id="b6512-106">**Get-Azexpressroute, Routetablesummary** cmdlet 'i, belirli bir YÖNLENDIRME bağlamının BGP komşu bilgilerinin özetini alır.</span><span class="sxs-lookup"><span data-stu-id="b6512-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="b6512-107">Bu bilgiler, yönlendirme bağlamının ne kadar sürdüğünü ve eşleme yönlendiricisi tarafından tanıtılan yol öneklerinin sayısını belirlemek için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="b6512-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="b6512-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6512-108">EXAMPLES</span></span>

### <span data-ttu-id="b6512-109">Örnek 1: birincil yolun yol özetini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b6512-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="b6512-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6512-110">PARAMETERS</span></span>

### <span data-ttu-id="b6512-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6512-111">-DefaultProfile</span></span>
<span data-ttu-id="b6512-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6512-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6512-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="b6512-113">-DevicePath</span></span>
<span data-ttu-id="b6512-114">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="b6512-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="b6512-115">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="b6512-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="b6512-116">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="b6512-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="b6512-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b6512-117">-PeeringType</span></span>
<span data-ttu-id="b6512-118">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b6512-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b6512-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6512-119">-ResourceGroupName</span></span>
<span data-ttu-id="b6512-120">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b6512-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="b6512-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6512-121">CommonParameters</span></span>
<span data-ttu-id="b6512-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6512-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6512-123">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6512-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6512-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6512-124">INPUTS</span></span>

### <span data-ttu-id="b6512-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b6512-125">System.String</span></span>

## <span data-ttu-id="b6512-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6512-126">OUTPUTS</span></span>

### <span data-ttu-id="b6512-127">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Kabatestablesummary</span><span class="sxs-lookup"><span data-stu-id="b6512-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="b6512-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6512-128">NOTES</span></span>

## <span data-ttu-id="b6512-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6512-129">RELATED LINKS</span></span>

[<span data-ttu-id="b6512-130">Get-Azexpressroute, Arptable</span><span class="sxs-lookup"><span data-stu-id="b6512-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="b6512-131">Get-Azexpressroute, RouteTable</span><span class="sxs-lookup"><span data-stu-id="b6512-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b6512-132">Get-Azexpressroutedevresi Istatistiği</span><span class="sxs-lookup"><span data-stu-id="b6512-132">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)
