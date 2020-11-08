---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 3067df10f3cd1d49b519d6c83defe304fbcf0296
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266057"
---
# <span data-ttu-id="eb36a-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="eb36a-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="eb36a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb36a-102">SYNOPSIS</span></span>
<span data-ttu-id="eb36a-103">ExpressRoute devresi bir yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="eb36a-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="eb36a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb36a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb36a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb36a-105">DESCRIPTION</span></span>
<span data-ttu-id="eb36a-106">**Get-Azexpressroute, RouteTable** cmdlet 'ı ExpressRoute devresi ayrıntılı bir yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="eb36a-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="eb36a-107">Yol tablosu tüm rotaları gösterir veya belirli bir eşleme türü için rotaları gösterecek şekilde filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="eb36a-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="eb36a-108">Yol tablosunu kullanarak, eşleme yapılandırmanızı ve bağlantınızı doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eb36a-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="eb36a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb36a-109">EXAMPLES</span></span>

### <span data-ttu-id="eb36a-110">Örnek 1: birincil yolun yol tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="eb36a-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="eb36a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb36a-111">PARAMETERS</span></span>

### <span data-ttu-id="eb36a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb36a-112">-DefaultProfile</span></span>
<span data-ttu-id="eb36a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eb36a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb36a-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="eb36a-114">-DevicePath</span></span>
<span data-ttu-id="eb36a-115">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="eb36a-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="eb36a-116">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="eb36a-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="eb36a-117">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="eb36a-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="eb36a-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="eb36a-118">-PeeringType</span></span>
<span data-ttu-id="eb36a-119">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="eb36a-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="eb36a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb36a-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb36a-121">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="eb36a-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="eb36a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb36a-122">CommonParameters</span></span>
<span data-ttu-id="eb36a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb36a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb36a-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eb36a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb36a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb36a-125">INPUTS</span></span>

### <span data-ttu-id="eb36a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="eb36a-126">System.String</span></span>

## <span data-ttu-id="eb36a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb36a-127">OUTPUTS</span></span>

### <span data-ttu-id="eb36a-128">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Routestable</span><span class="sxs-lookup"><span data-stu-id="eb36a-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="eb36a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb36a-129">NOTES</span></span>

## <span data-ttu-id="eb36a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb36a-130">RELATED LINKS</span></span>

[<span data-ttu-id="eb36a-131">Get-Azexpressroute, Arptable</span><span class="sxs-lookup"><span data-stu-id="eb36a-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="eb36a-132">Get-Azexpressroute, Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="eb36a-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="eb36a-133">Get-Azexpressroute, stat</span><span class="sxs-lookup"><span data-stu-id="eb36a-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
