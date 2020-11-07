---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: f73a41d313ccd41c60c2e59292b570e50876bd3a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932079"
---
# <span data-ttu-id="bff6d-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bff6d-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="bff6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bff6d-102">SYNOPSIS</span></span>
<span data-ttu-id="bff6d-103">Yol filtresine bir yol filtresi kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="bff6d-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="bff6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bff6d-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bff6d-105">DESCRIPTION</span></span>
<span data-ttu-id="bff6d-106">Add-AzRouteFilterRuleConfig cmdlet 'i Azure yol filtresine bir yol filtresi kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="bff6d-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="bff6d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bff6d-107">EXAMPLES</span></span>

### <span data-ttu-id="bff6d-108">Örnek 1: yol filtresine yol filtresi kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="bff6d-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="bff6d-109">İlk komut, Get-AzRouteFilter cmdlet 'ini kullanarak routefilter01 adlı bir yol filtresi alır.</span><span class="sxs-lookup"><span data-stu-id="bff6d-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="bff6d-110">Komut, filtreyi $RouteFilter değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bff6d-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="bff6d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bff6d-111">PARAMETERS</span></span>

### <span data-ttu-id="bff6d-112">-Access</span><span class="sxs-lookup"><span data-stu-id="bff6d-112">-Access</span></span>
<span data-ttu-id="bff6d-113">Yol filtresi kuralının erişimini belirtir; geçerli değerler Reddet veya Izin ver.</span><span class="sxs-lookup"><span data-stu-id="bff6d-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff6d-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="bff6d-114">-CommunityList</span></span>
<span data-ttu-id="bff6d-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="bff6d-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff6d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff6d-116">-DefaultProfile</span></span>
<span data-ttu-id="bff6d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bff6d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff6d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bff6d-118">-Force</span></span>
<span data-ttu-id="bff6d-119">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="bff6d-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bff6d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bff6d-120">-Name</span></span>
<span data-ttu-id="bff6d-121">Yol filtresine eklenecek yol filtresi kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bff6d-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="bff6d-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bff6d-122">-RouteFilter</span></span>
<span data-ttu-id="bff6d-123">Bu cmdlet 'in yol filtresi kuralı eklediği yol filtresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bff6d-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="bff6d-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="bff6d-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="bff6d-125">Yol filtresi kural türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bff6d-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="bff6d-126">Geçerli değerler: topluluk</span><span class="sxs-lookup"><span data-stu-id="bff6d-126">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff6d-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="bff6d-127">-Confirm</span></span>
<span data-ttu-id="bff6d-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bff6d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff6d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff6d-129">-WhatIf</span></span>
<span data-ttu-id="bff6d-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bff6d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bff6d-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bff6d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff6d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff6d-132">CommonParameters</span></span>
<span data-ttu-id="bff6d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bff6d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff6d-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff6d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff6d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bff6d-135">INPUTS</span></span>

### <span data-ttu-id="bff6d-136">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bff6d-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bff6d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bff6d-137">OUTPUTS</span></span>

### <span data-ttu-id="bff6d-138">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bff6d-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bff6d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bff6d-139">NOTES</span></span>
<span data-ttu-id="bff6d-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="bff6d-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="bff6d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bff6d-141">RELATED LINKS</span></span>

[<span data-ttu-id="bff6d-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bff6d-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bff6d-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bff6d-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bff6d-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bff6d-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bff6d-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bff6d-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="bff6d-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bff6d-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="bff6d-147">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bff6d-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="bff6d-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bff6d-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="bff6d-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bff6d-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)