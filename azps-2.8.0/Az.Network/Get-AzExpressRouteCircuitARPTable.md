---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: ce1e05106350adda37ffa5877585ff37337dad87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932034"
---
# <span data-ttu-id="9d0b9-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="9d0b9-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="9d0b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0b9-103">ExpressRoute devresi ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="9d0b9-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="9d0b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d0b9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d0b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d0b9-105">DESCRIPTION</span></span>
<span data-ttu-id="9d0b9-106">**Get-Azexpressroute, arptable** cmdlet 'ı ExpressRoute devresi 'in her IKI arabiriminden ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="9d0b9-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="9d0b9-107">ARP tablosu belirli bir eşleme için IPv4 adresini MAC adresine eşlemeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9d0b9-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="9d0b9-108">Katman 2 yapılandırmasını ve bağlantısını doğrulamak için ARP tablosunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d0b9-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="9d0b9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d0b9-109">EXAMPLES</span></span>

### <span data-ttu-id="9d0b9-110">Örnek 1: ExpressRoute eşi için ARP tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9d0b9-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="9d0b9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d0b9-111">PARAMETERS</span></span>

### <span data-ttu-id="9d0b9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d0b9-112">-DefaultProfile</span></span>
<span data-ttu-id="9d0b9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d0b9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d0b9-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="9d0b9-114">-DevicePath</span></span>
<span data-ttu-id="9d0b9-115">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="9d0b9-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="9d0b9-116">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="9d0b9-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="9d0b9-117">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="9d0b9-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="9d0b9-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="9d0b9-118">-PeeringType</span></span>
<span data-ttu-id="9d0b9-119">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="9d0b9-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="9d0b9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0b9-120">-ResourceGroupName</span></span>
<span data-ttu-id="9d0b9-121">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9d0b9-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="9d0b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0b9-122">CommonParameters</span></span>
<span data-ttu-id="9d0b9-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d0b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0b9-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9d0b9-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0b9-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d0b9-125">INPUTS</span></span>

### <span data-ttu-id="9d0b9-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9d0b9-126">System.String</span></span>

## <span data-ttu-id="9d0b9-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d0b9-127">OUTPUTS</span></span>

### <span data-ttu-id="9d0b9-128">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="9d0b9-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="9d0b9-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d0b9-129">NOTES</span></span>

## <span data-ttu-id="9d0b9-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d0b9-130">RELATED LINKS</span></span>

[<span data-ttu-id="9d0b9-131">Get-Azexpressroute, RouteTable</span><span class="sxs-lookup"><span data-stu-id="9d0b9-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="9d0b9-132">Get-Azexpressroute, Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="9d0b9-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="9d0b9-133">Get-Azexpressroutedevresi Istatistiği</span><span class="sxs-lookup"><span data-stu-id="9d0b9-133">Get-AzExpressRouteCircuitStats</span></span>](Get-AzExpressRouteCircuitStats.md)