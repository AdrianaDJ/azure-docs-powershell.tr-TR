---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 9d221f5ff25e43a750f939f80eae7a7878eacc44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590420"
---
# <span data-ttu-id="5a839-101">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a839-101">Get-AzureRmExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="5a839-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a839-102">SYNOPSIS</span></span>
<span data-ttu-id="5a839-103">ExpressRoute devresi bir yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="5a839-103">Gets a route table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a839-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a839-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a839-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a839-105">DESCRIPTION</span></span>
<span data-ttu-id="5a839-106">**Get-Azurermexpressroutedevresi** bir ExpressRoute devresi ayrıntılı yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="5a839-106">The **Get-AzureRmExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="5a839-107">Yol tablosu tüm rotaları gösterir veya belirli bir eşleme türü için rotaları gösterecek şekilde filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="5a839-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="5a839-108">Yol tablosunu kullanarak, eşleme yapılandırmanızı ve bağlantınızı doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a839-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="5a839-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a839-109">EXAMPLES</span></span>

### <span data-ttu-id="5a839-110">Örnek 1: birincil yolun yol tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="5a839-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="5a839-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a839-111">PARAMETERS</span></span>

### <span data-ttu-id="5a839-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a839-112">-DefaultProfile</span></span>
<span data-ttu-id="5a839-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a839-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a839-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="5a839-114">-DevicePath</span></span>
<span data-ttu-id="5a839-115">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="5a839-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="5a839-116">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="5a839-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="5a839-117">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="5a839-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="5a839-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="5a839-118">-PeeringType</span></span>
<span data-ttu-id="5a839-119">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="5a839-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="5a839-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a839-120">-ResourceGroupName</span></span>
<span data-ttu-id="5a839-121">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5a839-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="5a839-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a839-122">CommonParameters</span></span>
<span data-ttu-id="5a839-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a839-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a839-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a839-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a839-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a839-125">INPUTS</span></span>

### <span data-ttu-id="5a839-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5a839-126">None</span></span>
<span data-ttu-id="5a839-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5a839-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a839-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a839-128">OUTPUTS</span></span>

### <span data-ttu-id="5a839-129">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Routestable</span><span class="sxs-lookup"><span data-stu-id="5a839-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="5a839-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a839-130">NOTES</span></span>

## <span data-ttu-id="5a839-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a839-131">RELATED LINKS</span></span>

[<span data-ttu-id="5a839-132">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="5a839-132">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="5a839-133">Get-Azurermexpressroutedevresi Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="5a839-133">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="5a839-134">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="5a839-134">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)