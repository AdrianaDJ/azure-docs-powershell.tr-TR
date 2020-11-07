---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: b223cf62b536479b4c39d5852974698f2f38becf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764260"
---
# <span data-ttu-id="51add-101">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="51add-101">Set-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="51add-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51add-102">SYNOPSIS</span></span>
<span data-ttu-id="51add-103">ExpressRoute devresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="51add-103">Modifies an ExpressRoute circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51add-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51add-104">SYNTAX</span></span>

```
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51add-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="51add-105">DESCRIPTION</span></span>
<span data-ttu-id="51add-106">**Set-Azurermexpressroutedevresi** cmdlet 'ı değiştirilmiş ExpressRoute devresini Azure 'a kaydeder.</span><span class="sxs-lookup"><span data-stu-id="51add-106">The **Set-AzureRmExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="51add-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51add-107">EXAMPLES</span></span>

### <span data-ttu-id="51add-108">Örnek 1: ExpressRoute devresi ServiceKey 'i değiştirme</span><span class="sxs-lookup"><span data-stu-id="51add-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="51add-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51add-109">PARAMETERS</span></span>

### <span data-ttu-id="51add-110">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="51add-110">-ExpressRouteCircuit</span></span>
<span data-ttu-id="51add-111">Bu cmdlet 'in değiştirdiği **Expressroutedevresi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51add-111">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="51add-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51add-112">-DefaultProfile</span></span>
<span data-ttu-id="51add-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51add-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51add-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51add-114">CommonParameters</span></span>
<span data-ttu-id="51add-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51add-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51add-116">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51add-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51add-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51add-117">INPUTS</span></span>

### <span data-ttu-id="51add-118">Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="51add-118">PSExpressRouteCircuit</span></span>
<span data-ttu-id="51add-119">' Expressroutedevresi ' parametresi, ardışık düzenin ' Psexpressroutedevresi ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="51add-119">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="51add-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51add-120">OUTPUTS</span></span>

### <span data-ttu-id="51add-121">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="51add-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="51add-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51add-122">NOTES</span></span>

## <span data-ttu-id="51add-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51add-123">RELATED LINKS</span></span>

[<span data-ttu-id="51add-124">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="51add-124">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="51add-125">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="51add-125">Move-AzureRmExpressRouteCircuit</span></span>](./Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="51add-126">New-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="51add-126">New-AzureRmExpressRouteCircuit</span></span>](./New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="51add-127">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="51add-127">Remove-AzureRmExpressRouteCircuit</span></span>](./Remove-AzureRmExpressRouteCircuit.md)
