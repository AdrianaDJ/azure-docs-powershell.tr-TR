---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitstats
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: 4577eb4f105bca235e7b5e9feb0b0ef308298881
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762259"
---
# <span data-ttu-id="017d0-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="017d0-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="017d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="017d0-102">SYNOPSIS</span></span>
<span data-ttu-id="017d0-103">ExpressRoute devresi kullanım istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="017d0-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="017d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="017d0-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="017d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="017d0-105">DESCRIPTION</span></span>
<span data-ttu-id="017d0-106">**Get-Azurermexpressroutedevcmdlet** 'ı ExpressRoute devresi için trafik istatistiklerini getirir.</span><span class="sxs-lookup"><span data-stu-id="017d0-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="017d0-107">İstatistikler, hem birincil hem de ikincil yolların içinde gönderilen ve alınan bayt sayısını içerir.</span><span class="sxs-lookup"><span data-stu-id="017d0-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="017d0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="017d0-108">EXAMPLES</span></span>

### <span data-ttu-id="017d0-109">Örnek 1: ExpressRoute eşi için trafik istatistiklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="017d0-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="017d0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="017d0-110">PARAMETERS</span></span>

### <span data-ttu-id="017d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="017d0-111">-DefaultProfile</span></span>
<span data-ttu-id="017d0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="017d0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="017d0-113">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="017d0-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="017d0-114">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="017d0-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="017d0-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="017d0-115">-PeeringType</span></span>
<span data-ttu-id="017d0-116">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="017d0-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="017d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="017d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="017d0-118">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="017d0-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="017d0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="017d0-119">CommonParameters</span></span>
<span data-ttu-id="017d0-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="017d0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="017d0-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="017d0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="017d0-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="017d0-122">INPUTS</span></span>

### <span data-ttu-id="017d0-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="017d0-123">None</span></span>
<span data-ttu-id="017d0-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="017d0-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="017d0-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="017d0-125">OUTPUTS</span></span>

### <span data-ttu-id="017d0-126">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="017d0-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="017d0-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="017d0-127">NOTES</span></span>

## <span data-ttu-id="017d0-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="017d0-128">RELATED LINKS</span></span>

[<span data-ttu-id="017d0-129">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="017d0-129">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="017d0-130">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="017d0-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="017d0-131">Get-Azurermexpressroutedevresi Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="017d0-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
