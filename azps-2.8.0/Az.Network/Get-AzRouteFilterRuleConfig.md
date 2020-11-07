---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 5d83678d26804c97a0e21da4dcbff3f5af75d409
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931975"
---
# <span data-ttu-id="8e7f0-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e7f0-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8e7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7f0-103">Yol filtresinde bir yol filtresi kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="8e7f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e7f0-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e7f0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e7f0-105">DESCRIPTION</span></span>
<span data-ttu-id="8e7f0-106">**Get-AzRouteFilterRuleConfig** cmdlet 'i, yol filtresi kuralı veya yol filtresindeki yol filtresi kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="8e7f0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e7f0-107">EXAMPLES</span></span>

### <span data-ttu-id="8e7f0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8e7f0-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="8e7f0-109">İlk komut MyRouteFilter adlı yol filtresini alır ve bunu $rf değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="8e7f0-110">İkinci komut, yol filtresi ile ilişkilendirilmiş Rule01 adındaki yol filtresi kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="8e7f0-111">Üçüncü komut, bu yol filtresiyle ilişkilendirilmiş yol filtresi kurallarının bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="8e7f0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e7f0-112">PARAMETERS</span></span>

### <span data-ttu-id="8e7f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7f0-113">-DefaultProfile</span></span>
<span data-ttu-id="8e7f0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e7f0-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e7f0-115">-Name</span></span>
<span data-ttu-id="8e7f0-116">Yol filtresi kuralının adı</span><span class="sxs-lookup"><span data-stu-id="8e7f0-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="8e7f0-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e7f0-117">-RouteFilter</span></span>
<span data-ttu-id="8e7f0-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e7f0-118">The RouteFilter</span></span>

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

### <span data-ttu-id="8e7f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7f0-119">CommonParameters</span></span>
<span data-ttu-id="8e7f0-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7f0-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8e7f0-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7f0-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e7f0-122">INPUTS</span></span>

### <span data-ttu-id="8e7f0-123">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e7f0-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8e7f0-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e7f0-124">OUTPUTS</span></span>

### <span data-ttu-id="8e7f0-125">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="8e7f0-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="8e7f0-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e7f0-126">NOTES</span></span>

## <span data-ttu-id="8e7f0-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e7f0-127">RELATED LINKS</span></span>

[<span data-ttu-id="8e7f0-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e7f0-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8e7f0-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e7f0-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8e7f0-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e7f0-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8e7f0-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8e7f0-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8e7f0-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e7f0-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="8e7f0-133">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e7f0-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="8e7f0-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e7f0-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="8e7f0-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8e7f0-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
