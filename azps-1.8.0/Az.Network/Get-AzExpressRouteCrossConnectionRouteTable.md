---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 3fbfcc2ba78bb05eb64764be16bb84189afdd958
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760584"
---
# <span data-ttu-id="4f8b1-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4f8b1-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="4f8b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8b1-103">ExpressRoute çapraz bağlantısından bir yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="4f8b1-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="4f8b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f8b1-104">SYNTAX</span></span>

### <span data-ttu-id="4f8b1-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="4f8b1-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f8b1-106">Bir başvuru</span><span class="sxs-lookup"><span data-stu-id="4f8b1-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f8b1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f8b1-107">DESCRIPTION</span></span>
<span data-ttu-id="4f8b1-108">**Get-AzExpressRouteCrossConnectionRouteTable** cmdlet 'ı ExpressRoute devresi ayrıntılı bir yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="4f8b1-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="4f8b1-109">Yol tablosu tüm rotaları gösterir veya belirli bir eşleme türü için rotaları gösterecek şekilde filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="4f8b1-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="4f8b1-110">Yol tablosunu kullanarak, eşleme yapılandırmanızı ve bağlantınızı doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f8b1-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="4f8b1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f8b1-111">EXAMPLES</span></span>

### <span data-ttu-id="4f8b1-112">Örnek 1: birincil yolun yol tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="4f8b1-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="4f8b1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f8b1-113">PARAMETERS</span></span>

### <span data-ttu-id="4f8b1-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="4f8b1-114">-CrossConnectionName</span></span>
<span data-ttu-id="4f8b1-115">Hızlı yol çapraz bağlantı adı</span><span class="sxs-lookup"><span data-stu-id="4f8b1-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="4f8b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8b1-116">-DefaultProfile</span></span>
<span data-ttu-id="4f8b1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f8b1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f8b1-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="4f8b1-118">-DevicePath</span></span>
<span data-ttu-id="4f8b1-119">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="4f8b1-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="4f8b1-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="4f8b1-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="4f8b1-121">Hızlı rota çapraz bağlantısı</span><span class="sxs-lookup"><span data-stu-id="4f8b1-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="4f8b1-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4f8b1-122">-PeeringType</span></span>
<span data-ttu-id="4f8b1-123">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4f8b1-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4f8b1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f8b1-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f8b1-125">ExpressRoute çapraz bağlantısını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4f8b1-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="4f8b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8b1-126">CommonParameters</span></span>
<span data-ttu-id="4f8b1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f8b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8b1-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4f8b1-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8b1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f8b1-129">INPUTS</span></span>

### <span data-ttu-id="4f8b1-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4f8b1-130">None</span></span>
<span data-ttu-id="4f8b1-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4f8b1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f8b1-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f8b1-132">OUTPUTS</span></span>

### <span data-ttu-id="4f8b1-133">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Routestable</span><span class="sxs-lookup"><span data-stu-id="4f8b1-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="4f8b1-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f8b1-134">NOTES</span></span>

## <span data-ttu-id="4f8b1-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f8b1-135">RELATED LINKS</span></span>

[<span data-ttu-id="4f8b1-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="4f8b1-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="4f8b1-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4f8b1-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
