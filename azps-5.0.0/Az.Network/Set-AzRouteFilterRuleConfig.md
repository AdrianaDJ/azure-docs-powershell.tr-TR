---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278293"
---
# <span data-ttu-id="c6f4b-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6f4b-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c6f4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6f4b-103">Yol filtresinin yol filtresi kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="c6f4b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6f4b-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6f4b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="c6f4b-106">**Set-AzRouteFilterRuleConfig** cmdlet 'i, yol filtresinin yol filtresi kuralını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="c6f4b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6f4b-107">EXAMPLES</span></span>

### <span data-ttu-id="c6f4b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c6f4b-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="c6f4b-109">İlk komut, RouteFilter01 adındaki yol filtresini alır ve $rf değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="c6f4b-110">İkinci komut Rule01 adındaki yol filtresi kuralını değiştirir ve $rf değişkeninde güncelleştirilen yol filtresini depolar.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="c6f4b-111">Üçüncü komut güncelleştirilmiş yol filtresini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="c6f4b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6f4b-112">PARAMETERS</span></span>

### <span data-ttu-id="c6f4b-113">-Access</span><span class="sxs-lookup"><span data-stu-id="c6f4b-113">-Access</span></span>
<span data-ttu-id="c6f4b-114">Kuralın erişim türü.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-114">The access type of the rule.</span></span>
<span data-ttu-id="c6f4b-115">Olası değerler: ' Izin ver ', ' Reddet '</span><span class="sxs-lookup"><span data-stu-id="c6f4b-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="c6f4b-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="c6f4b-116">-CommunityList</span></span>
<span data-ttu-id="c6f4b-117">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="c6f4b-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="c6f4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6f4b-118">-DefaultProfile</span></span>
<span data-ttu-id="c6f4b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6f4b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c6f4b-120">-Force</span></span>
<span data-ttu-id="c6f4b-121">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="c6f4b-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c6f4b-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6f4b-122">-Name</span></span>
<span data-ttu-id="c6f4b-123">Yol filtresi kuralının adı</span><span class="sxs-lookup"><span data-stu-id="c6f4b-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="c6f4b-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6f4b-124">-RouteFilter</span></span>
<span data-ttu-id="c6f4b-125">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6f4b-125">The RouteFilter</span></span>

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

### <span data-ttu-id="c6f4b-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="c6f4b-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="c6f4b-127">Kuralın yol filtresi kuralı türü.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="c6f4b-128">Olası değerler: ' topluluk '</span><span class="sxs-lookup"><span data-stu-id="c6f4b-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="c6f4b-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6f4b-129">-Confirm</span></span>
<span data-ttu-id="c6f4b-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6f4b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6f4b-131">-WhatIf</span></span>
<span data-ttu-id="c6f4b-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6f4b-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6f4b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6f4b-134">CommonParameters</span></span>
<span data-ttu-id="c6f4b-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6f4b-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6f4b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6f4b-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6f4b-137">INPUTS</span></span>

### <span data-ttu-id="c6f4b-138">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6f4b-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c6f4b-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6f4b-139">OUTPUTS</span></span>

### <span data-ttu-id="c6f4b-140">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6f4b-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c6f4b-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6f4b-141">NOTES</span></span>

## <span data-ttu-id="c6f4b-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6f4b-142">RELATED LINKS</span></span>

[<span data-ttu-id="c6f4b-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6f4b-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6f4b-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6f4b-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6f4b-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6f4b-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6f4b-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6f4b-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="c6f4b-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6f4b-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="c6f4b-148">Yeni-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6f4b-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="c6f4b-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6f4b-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="c6f4b-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c6f4b-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
