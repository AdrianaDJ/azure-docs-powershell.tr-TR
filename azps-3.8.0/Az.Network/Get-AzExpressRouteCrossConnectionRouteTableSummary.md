---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 7479d18660ede3f70ac5e62f614b8a815b86433c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098840"
---
# <span data-ttu-id="b6d1e-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b6d1e-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="b6d1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d1e-103">ExpressRoute çapraz bağlantısının yol tablosu özetini alır.</span><span class="sxs-lookup"><span data-stu-id="b6d1e-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="b6d1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6d1e-104">SYNTAX</span></span>

### <span data-ttu-id="b6d1e-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="b6d1e-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6d1e-106">Bir başvuru</span><span class="sxs-lookup"><span data-stu-id="b6d1e-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6d1e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6d1e-107">DESCRIPTION</span></span>
<span data-ttu-id="b6d1e-108">**Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet 'i, belirli bir YÖNLENDIRME bağlamının BGP komşu bilgilerinin özetini alır.</span><span class="sxs-lookup"><span data-stu-id="b6d1e-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="b6d1e-109">Bu bilgiler, yönlendirme bağlamının ne kadar sürdüğünü ve eşleme yönlendiricisi tarafından tanıtılan yol öneklerinin sayısını belirlemek için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="b6d1e-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="b6d1e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6d1e-110">EXAMPLES</span></span>

### <span data-ttu-id="b6d1e-111">Örnek 1: birincil yolun yol özetini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b6d1e-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="b6d1e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6d1e-112">PARAMETERS</span></span>

### <span data-ttu-id="b6d1e-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="b6d1e-113">-CrossConnectionName</span></span>
<span data-ttu-id="b6d1e-114">Hızlı yol çapraz bağlantı adı</span><span class="sxs-lookup"><span data-stu-id="b6d1e-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="b6d1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d1e-115">-DefaultProfile</span></span>
<span data-ttu-id="b6d1e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6d1e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6d1e-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="b6d1e-117">-DevicePath</span></span>
<span data-ttu-id="b6d1e-118">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="b6d1e-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="b6d1e-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b6d1e-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="b6d1e-120">Hızlı rota çapraz bağlantısı</span><span class="sxs-lookup"><span data-stu-id="b6d1e-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="b6d1e-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="b6d1e-121">-PeeringType</span></span>
<span data-ttu-id="b6d1e-122">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="b6d1e-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="b6d1e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6d1e-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6d1e-124">ExpressRoute çapraz bağlantısını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b6d1e-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="b6d1e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d1e-125">CommonParameters</span></span>
<span data-ttu-id="b6d1e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6d1e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d1e-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6d1e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d1e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6d1e-128">INPUTS</span></span>

### <span data-ttu-id="b6d1e-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b6d1e-129">None</span></span>
<span data-ttu-id="b6d1e-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b6d1e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6d1e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6d1e-131">OUTPUTS</span></span>

### <span data-ttu-id="b6d1e-132">Microsoft. Azure. Commands. Network. model. Psexpressroutecrossconnectionkabatestablesummary</span><span class="sxs-lookup"><span data-stu-id="b6d1e-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="b6d1e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6d1e-133">NOTES</span></span>

## <span data-ttu-id="b6d1e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6d1e-134">RELATED LINKS</span></span>

[<span data-ttu-id="b6d1e-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="b6d1e-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="b6d1e-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b6d1e-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)