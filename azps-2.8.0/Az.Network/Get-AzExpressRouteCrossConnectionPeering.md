---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 99142e3dd33d84e11f326258450d92a58fe70e20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932025"
---
# <span data-ttu-id="7d36d-101">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="7d36d-101">Get-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="7d36d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d36d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d36d-103">ExpressRoute çapraz bağlantı eşlemesi yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="7d36d-103">Gets an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="7d36d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d36d-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnectionPeering [-Name <String>]
 -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d36d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d36d-105">DESCRIPTION</span></span>
<span data-ttu-id="7d36d-106">**Get-Azexpressroutecrossconnectioneşlemecmdlet** 'ı bir ExpressRoute çapraz bağlantı için eşleme ilişkisinin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="7d36d-106">The **Get-AzExpressRouteCrossConnectionPeering** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="7d36d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d36d-107">EXAMPLES</span></span>

### <span data-ttu-id="7d36d-108">Örnek 1: ExpressRoute çapraz bağlantı için eşleme yapılandırmasını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="7d36d-108">Example 1: Display the peering configuration for an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $RG
Get-AzExpressRouteCrossConnectionPeering -Name "AzurePrivatePeering" -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="7d36d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d36d-109">PARAMETERS</span></span>

### <span data-ttu-id="7d36d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d36d-110">-DefaultProfile</span></span>
<span data-ttu-id="7d36d-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d36d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d36d-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7d36d-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7d36d-113">Eşleme yapılandırmasını içeren ExpressRoute çapraz bağlantı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7d36d-113">The ExpressRoute cross connection object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d36d-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d36d-114">-Name</span></span>
<span data-ttu-id="7d36d-115">Alınacak eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="7d36d-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d36d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d36d-116">CommonParameters</span></span>
<span data-ttu-id="7d36d-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d36d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d36d-118">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7d36d-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d36d-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d36d-119">INPUTS</span></span>

### <span data-ttu-id="7d36d-120">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7d36d-120">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="7d36d-121">' ExpressRouteCrossConnection ' parametresi ardışık düzenin ' PSExpressRouteCrossConnection ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7d36d-121">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="7d36d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d36d-122">OUTPUTS</span></span>

### <span data-ttu-id="7d36d-123">Microsoft. Azure. Commands. Network. model. pspe,</span><span class="sxs-lookup"><span data-stu-id="7d36d-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="7d36d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d36d-124">NOTES</span></span>

## <span data-ttu-id="7d36d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d36d-125">RELATED LINKS</span></span>

[<span data-ttu-id="7d36d-126">Add-azexpressroutecrossconnectioneşleme</span><span class="sxs-lookup"><span data-stu-id="7d36d-126">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7d36d-127">Remove-azexpressroutecrossconnectioneşleme</span><span class="sxs-lookup"><span data-stu-id="7d36d-127">Remove-AzExpressRouteCrossConnectionPeering</span></span>](Remove-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="7d36d-128">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7d36d-128">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="7d36d-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7d36d-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
