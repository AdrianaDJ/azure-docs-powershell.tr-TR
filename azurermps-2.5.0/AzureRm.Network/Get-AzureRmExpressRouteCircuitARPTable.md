---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
ms.openlocfilehash: bdfb86eb53221466beca2566d8ea446072ea33d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939128"
---
# <span data-ttu-id="6a8a2-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6a8a2-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="6a8a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a8a2-102">SYNOPSIS</span></span>
<span data-ttu-id="6a8a2-103">ExpressRoute devresi ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="6a8a2-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a8a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a8a2-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a8a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a8a2-105">DESCRIPTION</span></span>
<span data-ttu-id="6a8a2-106">**Get-Azurermexpressroutedevresi arptable** cmdlet 'ı ExpressRoute devresi 'in her IKI arabiriminden ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="6a8a2-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="6a8a2-107">ARP tablosu belirli bir eşleme için IPv4 adresini MAC adresine eşlemeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="6a8a2-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="6a8a2-108">Katman 2 yapılandırmasını ve bağlantısını doğrulamak için ARP tablosunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a8a2-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="6a8a2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a8a2-109">EXAMPLES</span></span>

### <span data-ttu-id="6a8a2-110">Örnek 1: ExpressRoute eşi için ARP tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="6a8a2-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="6a8a2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a8a2-111">PARAMETERS</span></span>

### <span data-ttu-id="6a8a2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a8a2-112">-DefaultProfile</span></span>
<span data-ttu-id="6a8a2-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a8a2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a8a2-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="6a8a2-114">-DevicePath</span></span>
<span data-ttu-id="6a8a2-115">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="6a8a2-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="6a8a2-116">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="6a8a2-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="6a8a2-117">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="6a8a2-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="6a8a2-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="6a8a2-118">-PeeringType</span></span>
<span data-ttu-id="6a8a2-119">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="6a8a2-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="6a8a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a8a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="6a8a2-121">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6a8a2-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="6a8a2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a8a2-122">CommonParameters</span></span>
<span data-ttu-id="6a8a2-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a8a2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a8a2-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a8a2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a8a2-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a8a2-125">INPUTS</span></span>

## <span data-ttu-id="6a8a2-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a8a2-126">OUTPUTS</span></span>

### <span data-ttu-id="6a8a2-127">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="6a8a2-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="6a8a2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a8a2-128">NOTES</span></span>

## <span data-ttu-id="6a8a2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a8a2-129">RELATED LINKS</span></span>

[<span data-ttu-id="6a8a2-130">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="6a8a2-130">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="6a8a2-131">Get-Azurermexpressroutedevresi Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="6a8a2-131">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="6a8a2-132">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="6a8a2-132">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
