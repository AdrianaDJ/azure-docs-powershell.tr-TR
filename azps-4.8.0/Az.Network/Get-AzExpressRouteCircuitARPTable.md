---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: 1c59ef12964ddd022add01ae296b8ecac9ad0acd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266060"
---
# <span data-ttu-id="ff1e0-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ff1e0-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="ff1e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1e0-103">ExpressRoute devresi ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="ff1e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff1e0-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff1e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff1e0-105">DESCRIPTION</span></span>
<span data-ttu-id="ff1e0-106">**Get-Azexpressroute, arptable** cmdlet 'ı ExpressRoute devresi 'in her IKI arabiriminden ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="ff1e0-107">ARP tablosu belirli bir eşleme için IPv4 adresini MAC adresine eşlemeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="ff1e0-108">Katman 2 yapılandırmasını ve bağlantısını doğrulamak için ARP tablosunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="ff1e0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff1e0-109">EXAMPLES</span></span>

### <span data-ttu-id="ff1e0-110">Örnek 1: ExpressRoute eşi için ARP tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ff1e0-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="ff1e0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff1e0-111">PARAMETERS</span></span>

### <span data-ttu-id="ff1e0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff1e0-112">-DefaultProfile</span></span>
<span data-ttu-id="ff1e0-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff1e0-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="ff1e0-114">-DevicePath</span></span>
<span data-ttu-id="ff1e0-115">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="ff1e0-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="ff1e0-116">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="ff1e0-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="ff1e0-117">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="ff1e0-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ff1e0-118">-PeeringType</span></span>
<span data-ttu-id="ff1e0-119">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ff1e0-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ff1e0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff1e0-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff1e0-121">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="ff1e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1e0-122">CommonParameters</span></span>
<span data-ttu-id="ff1e0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1e0-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ff1e0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1e0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff1e0-125">INPUTS</span></span>

### <span data-ttu-id="ff1e0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ff1e0-126">System.String</span></span>

## <span data-ttu-id="ff1e0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff1e0-127">OUTPUTS</span></span>

### <span data-ttu-id="ff1e0-128">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="ff1e0-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="ff1e0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff1e0-129">NOTES</span></span>

## <span data-ttu-id="ff1e0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff1e0-130">RELATED LINKS</span></span>

[<span data-ttu-id="ff1e0-131">Get-Azexpressroute, RouteTable</span><span class="sxs-lookup"><span data-stu-id="ff1e0-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="ff1e0-132">Get-Azexpressroute, Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="ff1e0-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="ff1e0-133">Get-Azexpressroute, stat</span><span class="sxs-lookup"><span data-stu-id="ff1e0-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
