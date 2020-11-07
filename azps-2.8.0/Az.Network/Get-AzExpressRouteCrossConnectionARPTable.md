---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 3d7068eaa469779c3a7b02095f30d4ea3178dd6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931762"
---
# <span data-ttu-id="0136c-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0136c-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="0136c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0136c-102">SYNOPSIS</span></span>
<span data-ttu-id="0136c-103">ExpressRoute çapraz bağlantısından ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="0136c-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="0136c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0136c-104">SYNTAX</span></span>

### <span data-ttu-id="0136c-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="0136c-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0136c-106">Bir başvuru</span><span class="sxs-lookup"><span data-stu-id="0136c-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0136c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0136c-107">DESCRIPTION</span></span>
<span data-ttu-id="0136c-108">**Get-AzExpressRouteCrossConnectionARPTable** cmdlet 'i, bir ExpressRoute çapraz bağlantısının her IKI arabiriminden ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="0136c-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="0136c-109">ARP tablosu belirli bir eşleme için IPv4 adresini MAC adresine eşlemeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="0136c-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="0136c-110">Katman 2 yapılandırmasını ve bağlantısını doğrulamak için ARP tablosunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0136c-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="0136c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0136c-111">EXAMPLES</span></span>

### <span data-ttu-id="0136c-112">Örnek 1: ExpressRoute eşi için ARP tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="0136c-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="0136c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0136c-113">PARAMETERS</span></span>

### <span data-ttu-id="0136c-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="0136c-114">-CrossConnectionName</span></span>
<span data-ttu-id="0136c-115">Hızlı yol çapraz bağlantı adı</span><span class="sxs-lookup"><span data-stu-id="0136c-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="0136c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0136c-116">-DefaultProfile</span></span>
<span data-ttu-id="0136c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0136c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0136c-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="0136c-118">-DevicePath</span></span>
<span data-ttu-id="0136c-119">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="0136c-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="0136c-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0136c-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="0136c-121">Hızlı rota çapraz bağlantısı</span><span class="sxs-lookup"><span data-stu-id="0136c-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="0136c-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="0136c-122">-PeeringType</span></span>
<span data-ttu-id="0136c-123">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="0136c-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="0136c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0136c-124">-ResourceGroupName</span></span>
<span data-ttu-id="0136c-125">ExpressRoute çapraz bağlantısını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0136c-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="0136c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0136c-126">CommonParameters</span></span>
<span data-ttu-id="0136c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0136c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0136c-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0136c-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0136c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0136c-129">INPUTS</span></span>

### <span data-ttu-id="0136c-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0136c-130">None</span></span>
<span data-ttu-id="0136c-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0136c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0136c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0136c-132">OUTPUTS</span></span>

### <span data-ttu-id="0136c-133">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="0136c-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="0136c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0136c-134">NOTES</span></span>

## <span data-ttu-id="0136c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0136c-135">RELATED LINKS</span></span>

[<span data-ttu-id="0136c-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0136c-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="0136c-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0136c-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)