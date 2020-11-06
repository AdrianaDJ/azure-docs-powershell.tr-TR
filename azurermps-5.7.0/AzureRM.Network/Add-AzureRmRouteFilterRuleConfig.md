---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 5daf0c5f764a095906e31167d6ddbc764ae68d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592094"
---
# <span data-ttu-id="4712a-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4712a-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="4712a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4712a-102">SYNOPSIS</span></span>
<span data-ttu-id="4712a-103">Yol filtresine bir yol filtresi kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="4712a-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4712a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4712a-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4712a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4712a-105">DESCRIPTION</span></span>
<span data-ttu-id="4712a-106">Add-AzureRmRouteFilterRuleConfig cmdlet 'i Azure yol filtresine bir yol filtresi kuralı ekler.</span><span class="sxs-lookup"><span data-stu-id="4712a-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="4712a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4712a-107">EXAMPLES</span></span>

### <span data-ttu-id="4712a-108">--------------------------Örnek 1: yol filtresine yol filtresi kuralı ekleme--------------------------</span><span class="sxs-lookup"><span data-stu-id="4712a-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="4712a-109">İlk komut, Get-AzureRmRouteFilter cmdlet 'ini kullanarak routefilter01 adlı bir yol filtresi alır.</span><span class="sxs-lookup"><span data-stu-id="4712a-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="4712a-110">Komut, filtreyi $RouteFilter değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4712a-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="4712a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4712a-111">PARAMETERS</span></span>

### <span data-ttu-id="4712a-112">-Access</span><span class="sxs-lookup"><span data-stu-id="4712a-112">-Access</span></span>
<span data-ttu-id="4712a-113">Yol filtresi kuralının erişimini belirtir; geçerli değerler Reddet veya Izin ver.</span><span class="sxs-lookup"><span data-stu-id="4712a-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="4712a-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="4712a-114">-CommunityList</span></span>
<span data-ttu-id="4712a-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="4712a-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="4712a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4712a-116">-DefaultProfile</span></span>
<span data-ttu-id="4712a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4712a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4712a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4712a-118">-Force</span></span>
<span data-ttu-id="4712a-119">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="4712a-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="4712a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4712a-120">-Name</span></span>
<span data-ttu-id="4712a-121">Yol filtresine eklenecek yol filtresi kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4712a-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="4712a-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4712a-122">-RouteFilter</span></span>
<span data-ttu-id="4712a-123">Bu cmdlet 'in yol filtresi kuralı eklediği yol filtresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4712a-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="4712a-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="4712a-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="4712a-125">Yol filtresi kural türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4712a-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="4712a-126">Geçerli değerler: topluluk</span><span class="sxs-lookup"><span data-stu-id="4712a-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="4712a-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="4712a-127">-Confirm</span></span>
<span data-ttu-id="4712a-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4712a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4712a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4712a-129">-WhatIf</span></span>
<span data-ttu-id="4712a-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4712a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4712a-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4712a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4712a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4712a-132">CommonParameters</span></span>
<span data-ttu-id="4712a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4712a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4712a-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4712a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4712a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4712a-135">INPUTS</span></span>

### <span data-ttu-id="4712a-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4712a-136">PSRouteFilter</span></span>
<span data-ttu-id="4712a-137">' RouteFilter ' parametresi ardışık düzenin ' PSRouteFilter ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4712a-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="4712a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4712a-138">OUTPUTS</span></span>

### <span data-ttu-id="4712a-139">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4712a-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4712a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4712a-140">NOTES</span></span>
<span data-ttu-id="4712a-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="4712a-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4712a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4712a-142">RELATED LINKS</span></span>

[<span data-ttu-id="4712a-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4712a-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="4712a-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4712a-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="4712a-145">Yeni-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="4712a-145">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="4712a-146">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="4712a-146">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="4712a-147">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="4712a-147">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="4712a-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4712a-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

