---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 8ef7121e057759a6fbdb341d9d6bc137692a36cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594845"
---
# <span data-ttu-id="96dd7-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="96dd7-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="96dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="96dd7-103">ExpressRoute devresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="96dd7-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96dd7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96dd7-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96dd7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="96dd7-105">DESCRIPTION</span></span>
<span data-ttu-id="96dd7-106">**Set-Azurermexpressroutedevresi** cmdlet 'ı değiştirilmiş ExpressRoute devresini Azure 'a kaydeder.</span><span class="sxs-lookup"><span data-stu-id="96dd7-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="96dd7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96dd7-107">EXAMPLES</span></span>

### <span data-ttu-id="96dd7-108">Örnek 1: ExpressRoute devresi ServiceKey 'i değiştirme</span><span class="sxs-lookup"><span data-stu-id="96dd7-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="96dd7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96dd7-109">PARAMETERS</span></span>

### <span data-ttu-id="96dd7-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="96dd7-110">-AsJob</span></span>
<span data-ttu-id="96dd7-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="96dd7-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96dd7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96dd7-112">-DefaultProfile</span></span>
<span data-ttu-id="96dd7-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96dd7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96dd7-114">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="96dd7-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="96dd7-115">Bu cmdlet 'in değiştirdiği **Expressroutedevresi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="96dd7-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96dd7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96dd7-116">CommonParameters</span></span>
<span data-ttu-id="96dd7-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96dd7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96dd7-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96dd7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96dd7-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96dd7-119">INPUTS</span></span>

### <span data-ttu-id="96dd7-120">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="96dd7-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="96dd7-121">Parametreler: Expressroutedevresi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96dd7-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="96dd7-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96dd7-122">OUTPUTS</span></span>

### <span data-ttu-id="96dd7-123">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="96dd7-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="96dd7-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96dd7-124">NOTES</span></span>

## <span data-ttu-id="96dd7-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96dd7-125">RELATED LINKS</span></span>

[<span data-ttu-id="96dd7-126">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="96dd7-126">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="96dd7-127">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="96dd7-127">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="96dd7-128">New-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="96dd7-128">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="96dd7-129">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="96dd7-129">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
