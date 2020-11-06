---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 3cd01d2e9bb3673e2c0e42ea43418c9601796a08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593077"
---
# <span data-ttu-id="af849-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af849-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="af849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af849-102">SYNOPSIS</span></span>
<span data-ttu-id="af849-103">Yol filtresine bir yol filtresi kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="af849-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af849-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af849-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af849-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af849-105">DESCRIPTION</span></span>
<span data-ttu-id="af849-106">Add-AzureRmRouteFilterRuleConfig cmdlet 'i Azure yol filtresine bir yol filtresi kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="af849-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="af849-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af849-107">EXAMPLES</span></span>

### <span data-ttu-id="af849-108">--------------------------Örnek 1: yol filtresine yol filtresi kuralı ekleme--------------------------</span><span class="sxs-lookup"><span data-stu-id="af849-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
<span data-ttu-id="af849-109">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="af849-109">@{paragraph=PS C:\\\>}</span></span>















```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="af849-110">İlk komut, Get-AzureRmRouteFilter cmdlet 'ini kullanarak routefilter01 adlı bir yol filtresi alır.</span><span class="sxs-lookup"><span data-stu-id="af849-110">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="af849-111">Komut, filtreyi $RouteFilter değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="af849-111">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="af849-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af849-112">PARAMETERS</span></span>

### <span data-ttu-id="af849-113">-Access</span><span class="sxs-lookup"><span data-stu-id="af849-113">-Access</span></span>
<span data-ttu-id="af849-114">Yol filtresi kuralının erişimini belirtir; geçerli değerler Reddet veya Izin ver.</span><span class="sxs-lookup"><span data-stu-id="af849-114">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="af849-115">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="af849-115">-CommunityList</span></span>
<span data-ttu-id="af849-116">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="af849-116">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af849-117">-Force</span><span class="sxs-lookup"><span data-stu-id="af849-117">-Force</span></span>
<span data-ttu-id="af849-118">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="af849-118">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="af849-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="af849-119">-Name</span></span>
<span data-ttu-id="af849-120">Yol filtresine eklenecek yol filtresi kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af849-120">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="af849-121">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="af849-121">-RouteFilter</span></span>
<span data-ttu-id="af849-122">Bu cmdlet 'in yol filtresi kuralı eklediği yol filtresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af849-122">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="af849-123">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="af849-123">-RouteFilterRuleType</span></span>
<span data-ttu-id="af849-124">Yol filtresi kural türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="af849-124">Specifies the route filter rule type.</span></span>
<span data-ttu-id="af849-125">Geçerli değerler: topluluk</span><span class="sxs-lookup"><span data-stu-id="af849-125">Valid values are: Community</span></span>

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

### <span data-ttu-id="af849-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="af849-126">-Confirm</span></span>
<span data-ttu-id="af849-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af849-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af849-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af849-128">-WhatIf</span></span>
<span data-ttu-id="af849-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af849-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af849-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af849-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af849-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af849-131">-DefaultProfile</span></span>
<span data-ttu-id="af849-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af849-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af849-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af849-133">CommonParameters</span></span>
<span data-ttu-id="af849-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af849-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af849-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af849-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af849-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af849-136">INPUTS</span></span>

### <span data-ttu-id="af849-137">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="af849-137">PSRouteFilter</span></span>
<span data-ttu-id="af849-138">' RouteFilter ' parametresi ardışık düzenin ' PSRouteFilter ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="af849-138">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="af849-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af849-139">OUTPUTS</span></span>

### <span data-ttu-id="af849-140">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="af849-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="af849-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af849-141">NOTES</span></span>
<span data-ttu-id="af849-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="af849-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="af849-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af849-143">RELATED LINKS</span></span>

[<span data-ttu-id="af849-144">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="af849-144">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="af849-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="af849-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="af849-146">Yeni-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="af849-146">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="af849-147">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="af849-147">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="af849-148">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="af849-148">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="af849-149">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="af849-149">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

