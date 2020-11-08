---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278346"
---
# <span data-ttu-id="89214-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="89214-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="89214-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89214-102">SYNOPSIS</span></span>
<span data-ttu-id="89214-103">ExpressRoute devresi kullanım istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="89214-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="89214-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89214-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89214-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89214-105">DESCRIPTION</span></span>
<span data-ttu-id="89214-106">**Get-Azexpressroute, stat** ,</span><span class="sxs-lookup"><span data-stu-id="89214-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="89214-107">İstatistikler, hem birincil hem de ikincil yolların içinde gönderilen ve alınan bayt sayısını içerir.</span><span class="sxs-lookup"><span data-stu-id="89214-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="89214-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89214-108">EXAMPLES</span></span>

### <span data-ttu-id="89214-109">Örnek 1: ExpressRoute eşi için trafik istatistiklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="89214-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="89214-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89214-110">PARAMETERS</span></span>

### <span data-ttu-id="89214-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89214-111">-DefaultProfile</span></span>
<span data-ttu-id="89214-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89214-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89214-113">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="89214-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="89214-114">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="89214-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="89214-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="89214-115">-PeeringType</span></span>
<span data-ttu-id="89214-116">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="89214-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="89214-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89214-117">-ResourceGroupName</span></span>
<span data-ttu-id="89214-118">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="89214-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="89214-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89214-119">CommonParameters</span></span>
<span data-ttu-id="89214-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89214-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89214-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="89214-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89214-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89214-122">INPUTS</span></span>

### <span data-ttu-id="89214-123">System. String</span><span class="sxs-lookup"><span data-stu-id="89214-123">System.String</span></span>

## <span data-ttu-id="89214-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89214-124">OUTPUTS</span></span>

### <span data-ttu-id="89214-125">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="89214-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="89214-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89214-126">NOTES</span></span>

## <span data-ttu-id="89214-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89214-127">RELATED LINKS</span></span>

[<span data-ttu-id="89214-128">Get-Azexpressroute, Arptable</span><span class="sxs-lookup"><span data-stu-id="89214-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="89214-129">Get-Azexpressroute, RouteTable</span><span class="sxs-lookup"><span data-stu-id="89214-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="89214-130">Get-Azexpressroute, Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="89214-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
