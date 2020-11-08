---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098769"
---
# <span data-ttu-id="b34f3-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b34f3-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="b34f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b34f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b34f3-103">Yol filtresinde bir yol filtresi kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="b34f3-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="b34f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b34f3-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b34f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b34f3-105">DESCRIPTION</span></span>
<span data-ttu-id="b34f3-106">**Get-AzRouteFilterRuleConfig** cmdlet 'i, yol filtresi kuralı veya yol filtresindeki yol filtresi kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b34f3-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="b34f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b34f3-107">EXAMPLES</span></span>

### <span data-ttu-id="b34f3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b34f3-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="b34f3-109">İlk komut MyRouteFilter adlı yol filtresini alır ve bunu $rf değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b34f3-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="b34f3-110">İkinci komut, yol filtresi ile ilişkilendirilmiş Rule01 adındaki yol filtresi kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="b34f3-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="b34f3-111">Üçüncü komut, bu yol filtresiyle ilişkilendirilmiş yol filtresi kurallarının bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b34f3-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="b34f3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b34f3-112">PARAMETERS</span></span>

### <span data-ttu-id="b34f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34f3-113">-DefaultProfile</span></span>
<span data-ttu-id="b34f3-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b34f3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b34f3-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b34f3-115">-Name</span></span>
<span data-ttu-id="b34f3-116">Yol filtresi kuralının adı</span><span class="sxs-lookup"><span data-stu-id="b34f3-116">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34f3-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b34f3-117">-RouteFilter</span></span>
<span data-ttu-id="b34f3-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="b34f3-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b34f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34f3-119">CommonParameters</span></span>
<span data-ttu-id="b34f3-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b34f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34f3-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b34f3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34f3-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b34f3-122">INPUTS</span></span>

### <span data-ttu-id="b34f3-123">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b34f3-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b34f3-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b34f3-124">OUTPUTS</span></span>

### <span data-ttu-id="b34f3-125">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="b34f3-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="b34f3-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b34f3-126">NOTES</span></span>

## <span data-ttu-id="b34f3-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b34f3-127">RELATED LINKS</span></span>

[<span data-ttu-id="b34f3-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b34f3-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b34f3-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b34f3-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b34f3-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b34f3-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b34f3-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b34f3-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="b34f3-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b34f3-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="b34f3-133">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b34f3-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="b34f3-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b34f3-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="b34f3-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b34f3-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
