---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 0725b75c15fa6ab977d0b829a1928943bfd9ed31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593718"
---
# <span data-ttu-id="21b00-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="21b00-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="21b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21b00-102">SYNOPSIS</span></span>
<span data-ttu-id="21b00-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="21b00-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21b00-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21b00-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21b00-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21b00-105">DESCRIPTION</span></span>
<span data-ttu-id="21b00-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="21b00-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="21b00-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21b00-107">EXAMPLES</span></span>

### <span data-ttu-id="21b00-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21b00-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="21b00-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="21b00-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="21b00-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21b00-110">PARAMETERS</span></span>

### <span data-ttu-id="21b00-111">-Access</span><span class="sxs-lookup"><span data-stu-id="21b00-111">-Access</span></span>
<span data-ttu-id="21b00-112">Kuralın erişim türü.</span><span class="sxs-lookup"><span data-stu-id="21b00-112">The access type of the rule.</span></span>
<span data-ttu-id="21b00-113">Olası değerler: ' Izin ver ', ' Reddet '</span><span class="sxs-lookup"><span data-stu-id="21b00-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="21b00-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="21b00-114">-CommunityList</span></span>
<span data-ttu-id="21b00-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="21b00-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="21b00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b00-116">-DefaultProfile</span></span>
<span data-ttu-id="21b00-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21b00-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21b00-118">-Force</span><span class="sxs-lookup"><span data-stu-id="21b00-118">-Force</span></span>
<span data-ttu-id="21b00-119">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="21b00-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="21b00-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="21b00-120">-Name</span></span>
<span data-ttu-id="21b00-121">Yol filtresi kuralının adı</span><span class="sxs-lookup"><span data-stu-id="21b00-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="21b00-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="21b00-122">-RouteFilter</span></span>
<span data-ttu-id="21b00-123">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="21b00-123">The RouteFilter</span></span>

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

### <span data-ttu-id="21b00-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="21b00-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="21b00-125">Kuralın yol filtresi kuralı türü.</span><span class="sxs-lookup"><span data-stu-id="21b00-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="21b00-126">Olası değerler: ' topluluk '</span><span class="sxs-lookup"><span data-stu-id="21b00-126">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="21b00-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="21b00-127">-Confirm</span></span>
<span data-ttu-id="21b00-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21b00-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21b00-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21b00-129">-WhatIf</span></span>
<span data-ttu-id="21b00-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="21b00-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21b00-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="21b00-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21b00-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b00-132">CommonParameters</span></span>
<span data-ttu-id="21b00-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21b00-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b00-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b00-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b00-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21b00-135">INPUTS</span></span>

### <span data-ttu-id="21b00-136">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21b00-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="21b00-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21b00-137">OUTPUTS</span></span>

### <span data-ttu-id="21b00-138">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="21b00-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="21b00-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21b00-139">NOTES</span></span>

## <span data-ttu-id="21b00-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21b00-140">RELATED LINKS</span></span>

