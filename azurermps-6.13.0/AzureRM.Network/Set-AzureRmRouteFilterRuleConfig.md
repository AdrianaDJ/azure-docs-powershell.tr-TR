---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 88863b0db825eacfc844a8c24cc81f3ad866894d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591935"
---
# <span data-ttu-id="d2c72-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2c72-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="d2c72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c72-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c72-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="d2c72-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2c72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2c72-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2c72-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2c72-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c72-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="d2c72-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d2c72-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2c72-107">EXAMPLES</span></span>

### <span data-ttu-id="d2c72-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2c72-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d2c72-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="d2c72-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d2c72-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2c72-110">PARAMETERS</span></span>

### <span data-ttu-id="d2c72-111">-Access</span><span class="sxs-lookup"><span data-stu-id="d2c72-111">-Access</span></span>
<span data-ttu-id="d2c72-112">Kuralın erişim türü.</span><span class="sxs-lookup"><span data-stu-id="d2c72-112">The access type of the rule.</span></span>
<span data-ttu-id="d2c72-113">Olası değerler: ' Izin ver ', ' Reddet '</span><span class="sxs-lookup"><span data-stu-id="d2c72-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="d2c72-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="d2c72-114">-CommunityList</span></span>
<span data-ttu-id="d2c72-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="d2c72-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="d2c72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c72-116">-DefaultProfile</span></span>
<span data-ttu-id="d2c72-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2c72-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2c72-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d2c72-118">-Force</span></span>
<span data-ttu-id="d2c72-119">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="d2c72-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="d2c72-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2c72-120">-Name</span></span>
<span data-ttu-id="d2c72-121">Yol filtresi kuralının adı</span><span class="sxs-lookup"><span data-stu-id="d2c72-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="d2c72-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d2c72-122">-RouteFilter</span></span>
<span data-ttu-id="d2c72-123">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d2c72-123">The RouteFilter</span></span>

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

### <span data-ttu-id="d2c72-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="d2c72-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="d2c72-125">Kuralın yol filtresi kuralı türü.</span><span class="sxs-lookup"><span data-stu-id="d2c72-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="d2c72-126">Olası değerler: ' topluluk '</span><span class="sxs-lookup"><span data-stu-id="d2c72-126">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="d2c72-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2c72-127">-Confirm</span></span>
<span data-ttu-id="d2c72-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2c72-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c72-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c72-129">-WhatIf</span></span>
<span data-ttu-id="d2c72-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2c72-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2c72-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2c72-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c72-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c72-132">CommonParameters</span></span>
<span data-ttu-id="d2c72-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2c72-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c72-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c72-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c72-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2c72-135">INPUTS</span></span>

### <span data-ttu-id="d2c72-136">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d2c72-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="d2c72-137">Parametreler: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2c72-137">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="d2c72-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2c72-138">OUTPUTS</span></span>

### <span data-ttu-id="d2c72-139">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d2c72-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="d2c72-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2c72-140">NOTES</span></span>

## <span data-ttu-id="d2c72-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2c72-141">RELATED LINKS</span></span>
