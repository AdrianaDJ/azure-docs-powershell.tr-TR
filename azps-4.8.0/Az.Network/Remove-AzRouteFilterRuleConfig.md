---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: e596ea3092cd5fda045c20f80c9208015b57a42d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267012"
---
# <span data-ttu-id="31b5a-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31b5a-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="31b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="31b5a-103">Yol filtresi 'nden bir yol filtresi kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="31b5a-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="31b5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31b5a-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b5a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="31b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="31b5a-106">**Remove-AzRouteFilterRuleConfig** cmdlet 'i, yol filtresi 'nden bir yol filtresi kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="31b5a-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="31b5a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="31b5a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31b5a-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="31b5a-109">İlk komut, ResourceGroup01 adındaki kaynak grubuna ait RouteFilter01 adlı bir yol filtresi alır ve $rf değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="31b5a-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="31b5a-110">İkinci komut, $rf depolanan yol filtresindeki Rule01 adındaki yol filtresi kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="31b5a-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="31b5a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31b5a-111">PARAMETERS</span></span>

### <span data-ttu-id="31b5a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b5a-112">-DefaultProfile</span></span>
<span data-ttu-id="31b5a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31b5a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b5a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="31b5a-114">-Force</span></span>
<span data-ttu-id="31b5a-115">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="31b5a-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="31b5a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="31b5a-116">-Name</span></span>
<span data-ttu-id="31b5a-117">Yol filtresi kuralının adı</span><span class="sxs-lookup"><span data-stu-id="31b5a-117">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b5a-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="31b5a-118">-RouteFilter</span></span>
<span data-ttu-id="31b5a-119">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="31b5a-119">The RouteFilter</span></span>

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

### <span data-ttu-id="31b5a-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="31b5a-120">-Confirm</span></span>
<span data-ttu-id="31b5a-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31b5a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b5a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b5a-122">-WhatIf</span></span>
<span data-ttu-id="31b5a-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31b5a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31b5a-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31b5a-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b5a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b5a-125">CommonParameters</span></span>
<span data-ttu-id="31b5a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31b5a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b5a-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b5a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b5a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31b5a-128">INPUTS</span></span>

### <span data-ttu-id="31b5a-129">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="31b5a-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="31b5a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31b5a-130">OUTPUTS</span></span>

### <span data-ttu-id="31b5a-131">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="31b5a-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="31b5a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31b5a-132">NOTES</span></span>

## <span data-ttu-id="31b5a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31b5a-133">RELATED LINKS</span></span>

[<span data-ttu-id="31b5a-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31b5a-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="31b5a-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31b5a-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="31b5a-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31b5a-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="31b5a-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="31b5a-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="31b5a-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="31b5a-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="31b5a-139">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="31b5a-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="31b5a-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="31b5a-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="31b5a-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="31b5a-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
