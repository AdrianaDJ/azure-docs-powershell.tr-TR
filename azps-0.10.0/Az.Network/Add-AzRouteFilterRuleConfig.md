---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 910b432382eb24f6c5eaf77d3e0c7fe3dc547413
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935620"
---
# <span data-ttu-id="fd801-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fd801-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="fd801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd801-102">SYNOPSIS</span></span>
<span data-ttu-id="fd801-103">Yol filtresine bir yol filtresi kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="fd801-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="fd801-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd801-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd801-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd801-105">DESCRIPTION</span></span>
<span data-ttu-id="fd801-106">Add-AzRouteFilterRuleConfig cmdlet 'i Azure yol filtresine bir yol filtresi kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="fd801-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="fd801-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd801-107">EXAMPLES</span></span>

### <span data-ttu-id="fd801-108">--------------------------Örnek 1: yol filtresine yol filtresi kuralı ekleme--------------------------</span><span class="sxs-lookup"><span data-stu-id="fd801-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="fd801-109">İlk komut, Get-AzRouteFilter cmdlet 'ini kullanarak routefilter01 adlı bir yol filtresi alır.</span><span class="sxs-lookup"><span data-stu-id="fd801-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="fd801-110">Komut, filtreyi $RouteFilter değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fd801-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="fd801-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd801-111">PARAMETERS</span></span>

### <span data-ttu-id="fd801-112">-Access</span><span class="sxs-lookup"><span data-stu-id="fd801-112">-Access</span></span>
<span data-ttu-id="fd801-113">Yol filtresi kuralının erişimini belirtir; geçerli değerler Reddet veya Izin ver.</span><span class="sxs-lookup"><span data-stu-id="fd801-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd801-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="fd801-114">-CommunityList</span></span>
<span data-ttu-id="fd801-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="fd801-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="fd801-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd801-116">-DefaultProfile</span></span>
<span data-ttu-id="fd801-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd801-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd801-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fd801-118">-Force</span></span>
<span data-ttu-id="fd801-119">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="fd801-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd801-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd801-120">-Name</span></span>
<span data-ttu-id="fd801-121">Yol filtresine eklenecek yol filtresi kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd801-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd801-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="fd801-122">-RouteFilter</span></span>
<span data-ttu-id="fd801-123">Bu cmdlet 'in yol filtresi kuralı eklediği yol filtresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd801-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd801-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="fd801-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="fd801-125">Yol filtresi kural türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd801-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="fd801-126">Geçerli değerler: topluluk</span><span class="sxs-lookup"><span data-stu-id="fd801-126">Valid values are: Community</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd801-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd801-127">-Confirm</span></span>
<span data-ttu-id="fd801-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd801-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd801-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd801-129">-WhatIf</span></span>
<span data-ttu-id="fd801-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd801-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd801-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd801-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd801-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd801-132">CommonParameters</span></span>
<span data-ttu-id="fd801-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd801-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd801-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd801-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd801-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd801-135">INPUTS</span></span>

### <span data-ttu-id="fd801-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fd801-136">PSRouteFilter</span></span>
<span data-ttu-id="fd801-137">' RouteFilter ' parametresi ardışık düzenin ' PSRouteFilter ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fd801-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="fd801-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd801-138">OUTPUTS</span></span>

### <span data-ttu-id="fd801-139">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fd801-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="fd801-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd801-140">NOTES</span></span>
<span data-ttu-id="fd801-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="fd801-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="fd801-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd801-142">RELATED LINKS</span></span>

[<span data-ttu-id="fd801-143">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fd801-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="fd801-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fd801-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="fd801-145">New-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="fd801-145">New-AzRouteFilterRuleConfigConfig</span></span>](./New-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="fd801-146">Remove-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="fd801-146">Remove-AzRouteFilterRuleConfigConfig</span></span>](./Remove-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="fd801-147">Set-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="fd801-147">Set-AzRouteFilterRuleConfigConfig</span></span>](./Set-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="fd801-148">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="fd801-148">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

