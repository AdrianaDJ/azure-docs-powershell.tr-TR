---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C9954E3D-8645-473E-A6D4-86278C2F6BC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 90814e90b4d4951a9e899fd8cf50f365b646f497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589266"
---
# <span data-ttu-id="b206b-101">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b206b-101">Get-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="b206b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b206b-102">SYNOPSIS</span></span>
<span data-ttu-id="b206b-103">Azure 'dan bir Azure ExpressRoute devresi alır.</span><span class="sxs-lookup"><span data-stu-id="b206b-103">Gets an Azure ExpressRoute circuit from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b206b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b206b-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuit [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b206b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b206b-105">DESCRIPTION</span></span>
<span data-ttu-id="b206b-106">**Get-Azurermexpressroutedevresi** , aboneliğinizden bir ExpressRoute devresi nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b206b-106">The **Get-AzureRmExpressRouteCircuit** cmdlet is used to retrieve an ExpressRoute circuit object from your subscription.</span></span> <span data-ttu-id="b206b-107">Döndürülen devre nesnesi ExpressRoute devreleriyle çalışan diğer cmdlet 'ler için girdi olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b206b-107">The circuit object returned can be used as input to other cmdlets that operate on ExpressRoute circuits.</span></span>

## <span data-ttu-id="b206b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b206b-108">EXAMPLES</span></span>

### <span data-ttu-id="b206b-109">Örnek 1: silinecek ExpressRoute devresini alma</span><span class="sxs-lookup"><span data-stu-id="b206b-109">Example 1: Get the ExpressRoute circuit to be deleted</span></span>
```
Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg | Remove-AzureRmExpressRouteCircuit
```

## <span data-ttu-id="b206b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b206b-110">PARAMETERS</span></span>

### <span data-ttu-id="b206b-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="b206b-111">-Name</span></span>
<span data-ttu-id="b206b-112">ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="b206b-112">The name of the ExpressRoute circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b206b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b206b-113">-ResourceGroupName</span></span>
<span data-ttu-id="b206b-114">ExpressRoute devresini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b206b-114">The name of the resource group that contains the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="b206b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b206b-115">-DefaultProfile</span></span>
<span data-ttu-id="b206b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b206b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b206b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b206b-117">CommonParameters</span></span>
<span data-ttu-id="b206b-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b206b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b206b-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b206b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b206b-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b206b-120">INPUTS</span></span>

## <span data-ttu-id="b206b-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b206b-121">OUTPUTS</span></span>

### <span data-ttu-id="b206b-122">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b206b-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b206b-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b206b-123">NOTES</span></span>

## <span data-ttu-id="b206b-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b206b-124">RELATED LINKS</span></span>

[<span data-ttu-id="b206b-125">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b206b-125">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b206b-126">New-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b206b-126">New-AzureRmExpressRouteCircuit</span></span>](New-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b206b-127">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b206b-127">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="b206b-128">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="b206b-128">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
