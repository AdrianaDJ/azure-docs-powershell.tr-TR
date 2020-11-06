---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitStats.md
ms.openlocfilehash: 3230a9e9d8bb70cc80125258cca7d2eaef973e4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592603"
---
# <span data-ttu-id="95f6c-101">Get-AzureRmExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="95f6c-101">Get-AzureRmExpressRouteCircuitStats</span></span>

## <span data-ttu-id="95f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="95f6c-103">ExpressRoute devresi kullanım istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="95f6c-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95f6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95f6c-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f6c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="95f6c-106">**Get-Azurermexpressroutedevcmdlet** 'ı ExpressRoute devresi için trafik istatistiklerini getirir.</span><span class="sxs-lookup"><span data-stu-id="95f6c-106">The **Get-AzureRmExpressRouteCircuitStats** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="95f6c-107">İstatistikler, hem birincil hem de ikincil yolların içinde gönderilen ve alınan bayt sayısını içerir.</span><span class="sxs-lookup"><span data-stu-id="95f6c-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="95f6c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95f6c-108">EXAMPLES</span></span>

### <span data-ttu-id="95f6c-109">Örnek 1: ExpressRoute eşi için trafik istatistiklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="95f6c-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitStats -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="95f6c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95f6c-110">PARAMETERS</span></span>

### <span data-ttu-id="95f6c-111">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="95f6c-111">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="95f6c-112">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="95f6c-112">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="95f6c-113">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="95f6c-113">-PeeringType</span></span>
<span data-ttu-id="95f6c-114">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="95f6c-114">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="95f6c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95f6c-115">-ResourceGroupName</span></span>
<span data-ttu-id="95f6c-116">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="95f6c-116">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="95f6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f6c-117">-DefaultProfile</span></span>
<span data-ttu-id="95f6c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95f6c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95f6c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f6c-119">CommonParameters</span></span>
<span data-ttu-id="95f6c-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95f6c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f6c-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f6c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f6c-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95f6c-122">INPUTS</span></span>

## <span data-ttu-id="95f6c-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95f6c-123">OUTPUTS</span></span>

### <span data-ttu-id="95f6c-124">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="95f6c-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="95f6c-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95f6c-125">NOTES</span></span>

## <span data-ttu-id="95f6c-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95f6c-126">RELATED LINKS</span></span>

[<span data-ttu-id="95f6c-127">Get-Azurermexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="95f6c-127">Get-AzureRmExpressRouteCircuitARPTable</span></span>](Get-AzureRmExpressRouteCircuitARPTable.md)

[<span data-ttu-id="95f6c-128">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="95f6c-128">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="95f6c-129">Get-Azurermexpressroutedevresi Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="95f6c-129">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)
