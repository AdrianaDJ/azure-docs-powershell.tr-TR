---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: cf15d39a8c1ec320b45e488ccaac7903c82e30f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939129"
---
# <span data-ttu-id="ca84c-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ca84c-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="ca84c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca84c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca84c-103">Azure 'dan bir Azure ExpressRoute devresi alır.</span><span class="sxs-lookup"><span data-stu-id="ca84c-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca84c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca84c-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca84c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca84c-105">DESCRIPTION</span></span>
<span data-ttu-id="ca84c-106">**Get-Azurermexpressroutedevresi** , aboneliğinizden bir ExpressRoute devresi nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ca84c-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="ca84c-107">Döndürülen devre nesnesi ExpressRoute devreleriyle çalışan diğer cmdlet 'ler için girdi olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ca84c-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="ca84c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca84c-108">EXAMPLES</span></span>

### <span data-ttu-id="ca84c-109">Örnek 1: silinecek ExpressRoute devresini alma</span><span class="sxs-lookup"><span data-stu-id="ca84c-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="ca84c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca84c-110">PARAMETERS</span></span>

### <span data-ttu-id="ca84c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca84c-111">-DefaultProfile</span></span>
<span data-ttu-id="ca84c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca84c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca84c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca84c-113">-Name</span></span>
<span data-ttu-id="ca84c-114">ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="ca84c-114">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca84c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca84c-115">-ResourceGroupName</span></span>
<span data-ttu-id="ca84c-116">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ca84c-116">The name of the resource group that contains the ExpressRoute circuit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca84c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca84c-117">CommonParameters</span></span>
<span data-ttu-id="ca84c-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca84c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca84c-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca84c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca84c-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca84c-120">INPUTS</span></span>

## <span data-ttu-id="ca84c-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca84c-121">OUTPUTS</span></span>

### <span data-ttu-id="ca84c-122">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="ca84c-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ca84c-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca84c-123">NOTES</span></span>

## <span data-ttu-id="ca84c-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca84c-124">RELATED LINKS</span></span>

[<span data-ttu-id="ca84c-125">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="ca84c-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ca84c-126">New-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="ca84c-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ca84c-127">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="ca84c-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="ca84c-128">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="ca84c-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
