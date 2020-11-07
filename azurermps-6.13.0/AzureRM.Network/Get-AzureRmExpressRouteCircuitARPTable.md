---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitARPTable.md
ms.openlocfilehash: 046337478afe07d2b62a41259edd407476c15df2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764635"
---
# <span data-ttu-id="520e1-101">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="520e1-101">Get-AzureRmExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="520e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="520e1-102">SYNOPSIS</span></span>
<span data-ttu-id="520e1-103">ExpressRoute devresi ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="520e1-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="520e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="520e1-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="520e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="520e1-105">DESCRIPTION</span></span>
<span data-ttu-id="520e1-106">**Get-Azurermexpressroutedevresi arptable** cmdlet 'ı ExpressRoute devresi 'in her IKI arabiriminden ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="520e1-106">The **Get-AzureRmExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="520e1-107">ARP tablosu belirli bir eşleme için IPv4 adresini MAC adresine eşlemeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="520e1-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="520e1-108">Katman 2 yapılandırmasını ve bağlantısını doğrulamak için ARP tablosunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="520e1-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="520e1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="520e1-109">EXAMPLES</span></span>

### <span data-ttu-id="520e1-110">Örnek 1: ExpressRoute eşi için ARP tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="520e1-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzureRmExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="520e1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="520e1-111">PARAMETERS</span></span>

### <span data-ttu-id="520e1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520e1-112">-DefaultProfile</span></span>
<span data-ttu-id="520e1-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="520e1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="520e1-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="520e1-114">-DevicePath</span></span>
<span data-ttu-id="520e1-115">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="520e1-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="520e1-116">-Expressroutedevresi adı</span><span class="sxs-lookup"><span data-stu-id="520e1-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="520e1-117">İncelenen ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="520e1-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="520e1-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="520e1-118">-PeeringType</span></span>
<span data-ttu-id="520e1-119">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="520e1-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="520e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="520e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="520e1-121">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="520e1-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="520e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520e1-122">CommonParameters</span></span>
<span data-ttu-id="520e1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="520e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520e1-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="520e1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520e1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="520e1-125">INPUTS</span></span>

### <span data-ttu-id="520e1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="520e1-126">System.String</span></span>

## <span data-ttu-id="520e1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="520e1-127">OUTPUTS</span></span>

### <span data-ttu-id="520e1-128">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="520e1-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="520e1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="520e1-129">NOTES</span></span>

## <span data-ttu-id="520e1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="520e1-130">RELATED LINKS</span></span>

[<span data-ttu-id="520e1-131">Get-Azurermexpressroutedevresi RouteTable</span><span class="sxs-lookup"><span data-stu-id="520e1-131">Get-AzureRmExpressRouteCircuitRouteTable</span></span>](Get-AzureRmExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="520e1-132">Get-Azurermexpressroutedevresi Routetablesummary</span><span class="sxs-lookup"><span data-stu-id="520e1-132">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>](Get-AzureRmExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="520e1-133">Get-Azurermexpressroutedevresi stats</span><span class="sxs-lookup"><span data-stu-id="520e1-133">Get-AzureRmExpressRouteCircuitStats</span></span>](Get-AzureRmExpressRouteCircuitStats.md)
