---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzExpressRouteCircuitStat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 48136f033a75cfb49d05f5af76b1688ac6f68463
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935545"
---
# <span data-ttu-id="df762-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="df762-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="df762-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df762-102">SYNOPSIS</span></span>
<span data-ttu-id="df762-103">ExpressRoute devresi kullanım istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="df762-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="df762-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df762-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df762-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df762-105">DESCRIPTION</span></span>
<span data-ttu-id="df762-106">**Get-Azexpressroute, stat** ,</span><span class="sxs-lookup"><span data-stu-id="df762-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="df762-107">İstatistikler, hem birincil hem de ikincil yolların içinde gönderilen ve alınan bayt sayısını içerir.</span><span class="sxs-lookup"><span data-stu-id="df762-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="df762-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df762-108">EXAMPLES</span></span>

### <span data-ttu-id="df762-109">Örnek 1: ExpressRoute eşi için trafik istatistiklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="df762-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="df762-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df762-110">PARAMETERS</span></span>

### <span data-ttu-id="df762-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df762-111">-DefaultProfile</span></span>
<span data-ttu-id="df762-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df762-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df762-113">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="df762-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="df762-114">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="df762-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="df762-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="df762-115">-PeeringType</span></span>
<span data-ttu-id="df762-116">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="df762-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="df762-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df762-117">-ResourceGroupName</span></span>
<span data-ttu-id="df762-118">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="df762-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="df762-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df762-119">CommonParameters</span></span>
<span data-ttu-id="df762-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df762-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df762-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df762-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df762-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df762-122">INPUTS</span></span>

## <span data-ttu-id="df762-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df762-123">OUTPUTS</span></span>

### <span data-ttu-id="df762-124">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="df762-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="df762-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df762-125">NOTES</span></span>

## <span data-ttu-id="df762-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df762-126">RELATED LINKS</span></span>

[<span data-ttu-id="df762-127">Get-Azexpressroute, Arptable</span><span class="sxs-lookup"><span data-stu-id="df762-127">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="df762-128">Get-Azexpressroute, RouteTable</span><span class="sxs-lookup"><span data-stu-id="df762-128">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="df762-129">Get-Azexpressroute, Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="df762-129">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
