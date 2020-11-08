---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionARPTable.md
ms.openlocfilehash: 30addde4594c7b67fd5ba9c1358d64ac206a4531
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098940"
---
# <span data-ttu-id="8997a-101">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8997a-101">Get-AzExpressRouteCrossConnectionArpTable</span></span>

## <span data-ttu-id="8997a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8997a-102">SYNOPSIS</span></span>
<span data-ttu-id="8997a-103">ExpressRoute çapraz bağlantısından ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="8997a-103">Gets the ARP table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="8997a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8997a-104">SYNTAX</span></span>

### <span data-ttu-id="8997a-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="8997a-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8997a-106">Bir başvuru</span><span class="sxs-lookup"><span data-stu-id="8997a-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionArpTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8997a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8997a-107">DESCRIPTION</span></span>
<span data-ttu-id="8997a-108">**Get-AzExpressRouteCrossConnectionARPTable** cmdlet 'i, bir ExpressRoute çapraz bağlantısının her IKI arabiriminden ARP tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="8997a-108">The **Get-AzExpressRouteCrossConnectionARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute cross connection.</span></span> <span data-ttu-id="8997a-109">ARP tablosu belirli bir eşleme için IPv4 adresini MAC adresine eşlemeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="8997a-109">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="8997a-110">Katman 2 yapılandırmasını ve bağlantısını doğrulamak için ARP tablosunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8997a-110">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="8997a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8997a-111">EXAMPLES</span></span>

### <span data-ttu-id="8997a-112">Örnek 1: ExpressRoute eşi için ARP tablosunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8997a-112">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCrossConnectionARPTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="8997a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8997a-113">PARAMETERS</span></span>

### <span data-ttu-id="8997a-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="8997a-114">-CrossConnectionName</span></span>
<span data-ttu-id="8997a-115">Hızlı yol çapraz bağlantı adı</span><span class="sxs-lookup"><span data-stu-id="8997a-115">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="8997a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8997a-116">-DefaultProfile</span></span>
<span data-ttu-id="8997a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8997a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8997a-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="8997a-118">-DevicePath</span></span>
<span data-ttu-id="8997a-119">Bu parametre için kabul edilebilir değerler: `Primary` veya `Secondary`</span><span class="sxs-lookup"><span data-stu-id="8997a-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="8997a-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8997a-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="8997a-121">Hızlı rota çapraz bağlantısı</span><span class="sxs-lookup"><span data-stu-id="8997a-121">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="8997a-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="8997a-122">-PeeringType</span></span>
<span data-ttu-id="8997a-123">Bu parametre için kabul edilebilir değerler: `AzurePrivatePeering` , `AzurePublicPeering` ve `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="8997a-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="8997a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8997a-124">-ResourceGroupName</span></span>
<span data-ttu-id="8997a-125">ExpressRoute çapraz bağlantısını içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8997a-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="8997a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8997a-126">CommonParameters</span></span>
<span data-ttu-id="8997a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8997a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8997a-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8997a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8997a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8997a-129">INPUTS</span></span>

### <span data-ttu-id="8997a-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8997a-130">None</span></span>
<span data-ttu-id="8997a-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8997a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8997a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8997a-132">OUTPUTS</span></span>

### <span data-ttu-id="8997a-133">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi Arptable</span><span class="sxs-lookup"><span data-stu-id="8997a-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="8997a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8997a-134">NOTES</span></span>

## <span data-ttu-id="8997a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8997a-135">RELATED LINKS</span></span>

[<span data-ttu-id="8997a-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8997a-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)

[<span data-ttu-id="8997a-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8997a-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
