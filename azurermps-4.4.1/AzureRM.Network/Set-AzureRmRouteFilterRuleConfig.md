---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: f5b2a3f66a1972edbf6d3e475f5f30fc9530929f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589215"
---
# <span data-ttu-id="1b980-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1b980-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1b980-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b980-102">SYNOPSIS</span></span>
<span data-ttu-id="1b980-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="1b980-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b980-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b980-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b980-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b980-105">DESCRIPTION</span></span>
<span data-ttu-id="1b980-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="1b980-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1b980-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b980-107">EXAMPLES</span></span>

### <span data-ttu-id="1b980-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b980-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1b980-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="1b980-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1b980-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b980-110">PARAMETERS</span></span>

### <span data-ttu-id="1b980-111">-Access</span><span class="sxs-lookup"><span data-stu-id="1b980-111">-Access</span></span>
<span data-ttu-id="1b980-112">Kuralın erişim türü.</span><span class="sxs-lookup"><span data-stu-id="1b980-112">The access type of the rule.</span></span>
<span data-ttu-id="1b980-113">Olası değerler: ' Izin ver ', ' Reddet '</span><span class="sxs-lookup"><span data-stu-id="1b980-113">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="1b980-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="1b980-114">-CommunityList</span></span>
<span data-ttu-id="1b980-115">Yol süzgecinin filtrelendirilecektir topluluk değeri listesi</span><span class="sxs-lookup"><span data-stu-id="1b980-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="1b980-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1b980-116">-Force</span></span>
<span data-ttu-id="1b980-117">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="1b980-117">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="1b980-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b980-118">-Name</span></span>
<span data-ttu-id="1b980-119">Yol filtresi kuralının adı</span><span class="sxs-lookup"><span data-stu-id="1b980-119">The name of the route filter rule</span></span>

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

### <span data-ttu-id="1b980-120">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b980-120">-RouteFilter</span></span>
<span data-ttu-id="1b980-121">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b980-121">The RouteFilter</span></span>

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

### <span data-ttu-id="1b980-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1b980-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="1b980-123">Kuralın yol filtresi kuralı türü.</span><span class="sxs-lookup"><span data-stu-id="1b980-123">The route filter rule type of the rule.</span></span>
<span data-ttu-id="1b980-124">Olası değerler: ' topluluk '</span><span class="sxs-lookup"><span data-stu-id="1b980-124">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="1b980-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b980-125">-Confirm</span></span>
<span data-ttu-id="1b980-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b980-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b980-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b980-127">-WhatIf</span></span>
<span data-ttu-id="1b980-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b980-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b980-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b980-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b980-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b980-130">-DefaultProfile</span></span>
<span data-ttu-id="1b980-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b980-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b980-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b980-132">CommonParameters</span></span>
<span data-ttu-id="1b980-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b980-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b980-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b980-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b980-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b980-135">INPUTS</span></span>

### <span data-ttu-id="1b980-136">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b980-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1b980-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b980-137">OUTPUTS</span></span>

### <span data-ttu-id="1b980-138">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1b980-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1b980-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b980-139">NOTES</span></span>

## <span data-ttu-id="1b980-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b980-140">RELATED LINKS</span></span>

