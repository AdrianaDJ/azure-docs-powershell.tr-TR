---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCircuit.md
ms.openlocfilehash: 58df8e57a225d1ee003da317ca24c71b1db34f5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274789"
---
# <span data-ttu-id="548f7-101">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="548f7-101">Set-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="548f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="548f7-102">SYNOPSIS</span></span>
<span data-ttu-id="548f7-103">ExpressRoute devresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="548f7-103">Modifies an ExpressRoute circuit.</span></span>

## <span data-ttu-id="548f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="548f7-104">SYNTAX</span></span>

```
Set-AzExpressRouteCircuit -ExpressRouteCircuit <PSExpressRouteCircuit> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="548f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="548f7-105">DESCRIPTION</span></span>
<span data-ttu-id="548f7-106">**Set-Azexpressroutedevresi** cmdlet 'ı değiştirilmiş ExpressRoute devresini Azure 'a kaydeder.</span><span class="sxs-lookup"><span data-stu-id="548f7-106">The **Set-AzExpressRouteCircuit** cmdlet saves the modified ExpressRoute circuit to Azure.</span></span>

## <span data-ttu-id="548f7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="548f7-107">EXAMPLES</span></span>

### <span data-ttu-id="548f7-108">Örnek 1: ExpressRoute devresi ServiceKey 'i değiştirme</span><span class="sxs-lookup"><span data-stu-id="548f7-108">Example 1: Change the ServiceKey of an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
$ckt.ServiceKey = '64ce99dd-ee70-4e74-b6b8-91c6307433a0'
Set-AzExpressRouteCircuit -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="548f7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="548f7-109">PARAMETERS</span></span>

### <span data-ttu-id="548f7-110">-Iş</span><span class="sxs-lookup"><span data-stu-id="548f7-110">-AsJob</span></span>
<span data-ttu-id="548f7-111">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="548f7-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="548f7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548f7-112">-DefaultProfile</span></span>
<span data-ttu-id="548f7-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="548f7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="548f7-114">-Expressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="548f7-114">-ExpressRouteCircuit</span></span>
<span data-ttu-id="548f7-115">Bu cmdlet 'in değiştirdiği **Expressroutedevresi** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="548f7-115">Specifies the **ExpressRouteCircuit** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="548f7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548f7-116">CommonParameters</span></span>
<span data-ttu-id="548f7-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="548f7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548f7-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548f7-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548f7-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="548f7-119">INPUTS</span></span>

### <span data-ttu-id="548f7-120">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="548f7-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="548f7-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="548f7-121">OUTPUTS</span></span>

### <span data-ttu-id="548f7-122">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="548f7-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="548f7-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="548f7-123">NOTES</span></span>

## <span data-ttu-id="548f7-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="548f7-124">RELATED LINKS</span></span>

[<span data-ttu-id="548f7-125">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="548f7-125">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="548f7-126">Taşıma-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="548f7-126">Move-AzExpressRouteCircuit</span></span>](./Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="548f7-127">Yeni-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="548f7-127">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="548f7-128">Remove-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="548f7-128">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)
