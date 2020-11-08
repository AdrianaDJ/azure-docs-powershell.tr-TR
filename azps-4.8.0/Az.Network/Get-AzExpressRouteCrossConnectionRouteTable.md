---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266565"
---
# <span data-ttu-id="535eb-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="535eb-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="535eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="535eb-102">SYNOPSIS</span></span>
<span data-ttu-id="535eb-103">ExpressRoute çapraz bağlantısından bir yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="535eb-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="535eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="535eb-104">SYNTAX</span></span>

### <span data-ttu-id="535eb-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="535eb-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="535eb-106">Bir başvuru</span><span class="sxs-lookup"><span data-stu-id="535eb-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="535eb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="535eb-107">DESCRIPTION</span></span>
<span data-ttu-id="535eb-108">**Get-AzExpressRouteCrossConnectionRouteTable** cmdlet 'ı ExpressRoute devresi ayrıntılı bir yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="535eb-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="535eb-109">Yol tablosu tüm rotaları gösterir veya belirli bir eşleme türü için rotaları gösterecek şekilde filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="535eb-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="535eb-110">Yol tablosunu kullanarak, eşleme yapılandırmanızı ve bağlantınızı doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="535eb-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="535eb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="535eb-111">EXAMPLES</span></span>

### <span data-ttu-id="535eb-112">Örnek 1: birincil yolun yol tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="535eb-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="535eb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="535eb-113">PARAMETERS</span></span>

### <span data-ttu-id="535eb-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="535eb-114">-CrossConnectionName</span></span>
<span data-ttu-id="535eb-115">Hızlı yol çapraz bağlantı adı</span><span class="sxs-lookup"><span data-stu-id="535eb-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535eb-116">-DefaultProfile</span></span>
<span data-ttu-id="535eb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="535eb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="535eb-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="535eb-118">-DevicePath</span></span>
<span data-ttu-id="535eb-119">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="535eb-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="535eb-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="535eb-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="535eb-121">Hızlı rota çapraz bağlantısı</span><span class="sxs-lookup"><span data-stu-id="535eb-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535eb-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="535eb-122">-PeeringType</span></span>
<span data-ttu-id="535eb-123">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="535eb-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="535eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="535eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="535eb-125">ExpressRoute çapraz bağlantısını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="535eb-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535eb-126">CommonParameters</span></span>
<span data-ttu-id="535eb-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="535eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535eb-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="535eb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535eb-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="535eb-129">INPUTS</span></span>

### <span data-ttu-id="535eb-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="535eb-130">None</span></span>
<span data-ttu-id="535eb-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="535eb-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="535eb-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="535eb-132">OUTPUTS</span></span>

### <span data-ttu-id="535eb-133">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Routestable</span><span class="sxs-lookup"><span data-stu-id="535eb-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="535eb-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="535eb-134">NOTES</span></span>

## <span data-ttu-id="535eb-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="535eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="535eb-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="535eb-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="535eb-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="535eb-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
