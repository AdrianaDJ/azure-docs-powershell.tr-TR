---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: b4e93b89a11d4341b6a04de1b5625084e9348c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592604"
---
# <span data-ttu-id="e27d7-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="e27d7-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="e27d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e27d7-102">SYNOPSIS</span></span>
<span data-ttu-id="e27d7-103">ExpressRoute devrenin yol tablosu özetini alır.</span><span class="sxs-lookup"><span data-stu-id="e27d7-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e27d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e27d7-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e27d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e27d7-105">DESCRIPTION</span></span>
<span data-ttu-id="e27d7-106">**Get-Azurermexpressroutedevresi Routetablesummary** cmdlet 'i, belirli bir YÖNLENDIRME bağlamının BGP komşu bilgilerinin özetini alır.</span><span class="sxs-lookup"><span data-stu-id="e27d7-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="e27d7-107">Bu bilgiler, yönlendirme bağlamının ne kadar sürdüğünü ve eşleme yönlendiricisi tarafından tanıtılan yol öneklerinin sayısını belirlemek için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="e27d7-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="e27d7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e27d7-108">EXAMPLES</span></span>

### <span data-ttu-id="e27d7-109">Örnek 1: birincil yolun yol özetini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="e27d7-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="e27d7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e27d7-110">PARAMETERS</span></span>

### <span data-ttu-id="e27d7-111">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="e27d7-111">-DevicePath</span></span>
<span data-ttu-id="e27d7-112">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="e27d7-112">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="e27d7-113">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="e27d7-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="e27d7-114">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="e27d7-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="e27d7-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="e27d7-115">-PeeringType</span></span>
<span data-ttu-id="e27d7-116">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="e27d7-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="e27d7-118">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e27d7-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="e27d7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27d7-119">-DefaultProfile</span></span>
<span data-ttu-id="e27d7-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e27d7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e27d7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27d7-121">CommonParameters</span></span>
<span data-ttu-id="e27d7-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e27d7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27d7-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e27d7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27d7-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e27d7-124">INPUTS</span></span>

## <span data-ttu-id="e27d7-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e27d7-125">OUTPUTS</span></span>

### <span data-ttu-id="e27d7-126">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Kabatestablesummary</span><span class="sxs-lookup"><span data-stu-id="e27d7-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="e27d7-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e27d7-127">NOTES</span></span>

## <span data-ttu-id="e27d7-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e27d7-128">RELATED LINKS</span></span>

[<span data-ttu-id="e27d7-129">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="e27d7-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="e27d7-130">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="e27d7-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="e27d7-131">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="e27d7-131">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
