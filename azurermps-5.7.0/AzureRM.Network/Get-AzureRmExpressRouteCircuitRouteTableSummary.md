---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 849fb653308537a3d37740a21ba8b488903406ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590982"
---
# <span data-ttu-id="00970-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="00970-101">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="00970-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00970-102">SYNOPSIS</span></span>
<span data-ttu-id="00970-103">ExpressRoute devrenin yol tablosu özetini alır.</span><span class="sxs-lookup"><span data-stu-id="00970-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00970-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00970-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00970-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00970-105">DESCRIPTION</span></span>
<span data-ttu-id="00970-106">**Get-Azurermexpressroutedevresi Routetablesummary** cmdlet 'i, belirli bir YÖNLENDIRME bağlamının BGP komşu bilgilerinin özetini alır.</span><span class="sxs-lookup"><span data-stu-id="00970-106">The **Get-AzureRmExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="00970-107">Bu bilgiler, yönlendirme bağlamının ne kadar sürdüğünü ve eşleme yönlendiricisi tarafından tanıtılan yol öneklerinin sayısını belirlemek için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="00970-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="00970-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00970-108">EXAMPLES</span></span>

### <span data-ttu-id="00970-109">Örnek 1: birincil yolun yol özetini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="00970-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzureRmExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="00970-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00970-110">PARAMETERS</span></span>

### <span data-ttu-id="00970-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00970-111">-DefaultProfile</span></span>
<span data-ttu-id="00970-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00970-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00970-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="00970-113">-DevicePath</span></span>
<span data-ttu-id="00970-114">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="00970-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="00970-115">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="00970-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="00970-116">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="00970-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="00970-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="00970-117">-PeeringType</span></span>
<span data-ttu-id="00970-118">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="00970-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="00970-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00970-119">-ResourceGroupName</span></span>
<span data-ttu-id="00970-120">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="00970-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="00970-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00970-121">CommonParameters</span></span>
<span data-ttu-id="00970-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00970-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00970-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00970-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00970-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00970-124">INPUTS</span></span>

### <span data-ttu-id="00970-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="00970-125">None</span></span>
<span data-ttu-id="00970-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="00970-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00970-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00970-127">OUTPUTS</span></span>

### <span data-ttu-id="00970-128">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Kabatestablesummary</span><span class="sxs-lookup"><span data-stu-id="00970-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="00970-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00970-129">NOTES</span></span>

## <span data-ttu-id="00970-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00970-130">RELATED LINKS</span></span>

[<span data-ttu-id="00970-131">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="00970-131">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="00970-132">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="00970-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="00970-133">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="00970-133">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
