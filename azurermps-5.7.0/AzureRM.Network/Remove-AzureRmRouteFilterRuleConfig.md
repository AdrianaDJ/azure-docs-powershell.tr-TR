---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 59a8ff1467bf70cea2eafe2117850d3423236f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764172"
---
# <span data-ttu-id="612c9-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="612c9-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="612c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="612c9-102">SYNOPSIS</span></span>
<span data-ttu-id="612c9-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="612c9-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="612c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="612c9-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="612c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="612c9-105">DESCRIPTION</span></span>
<span data-ttu-id="612c9-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="612c9-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="612c9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="612c9-107">EXAMPLES</span></span>

### <span data-ttu-id="612c9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="612c9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="612c9-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="612c9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="612c9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="612c9-110">PARAMETERS</span></span>

### <span data-ttu-id="612c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="612c9-111">-DefaultProfile</span></span>
<span data-ttu-id="612c9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="612c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="612c9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="612c9-113">-Force</span></span>
<span data-ttu-id="612c9-114">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="612c9-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="612c9-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="612c9-115">-Name</span></span>
<span data-ttu-id="612c9-116">Yol filtresi kuralının adı</span><span class="sxs-lookup"><span data-stu-id="612c9-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="612c9-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="612c9-117">-RouteFilter</span></span>
<span data-ttu-id="612c9-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="612c9-118">The RouteFilter</span></span>

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

### <span data-ttu-id="612c9-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="612c9-119">-Confirm</span></span>
<span data-ttu-id="612c9-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="612c9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="612c9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="612c9-121">-WhatIf</span></span>
<span data-ttu-id="612c9-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="612c9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="612c9-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="612c9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="612c9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="612c9-124">CommonParameters</span></span>
<span data-ttu-id="612c9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="612c9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="612c9-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="612c9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="612c9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="612c9-127">INPUTS</span></span>

### <span data-ttu-id="612c9-128">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="612c9-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="612c9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="612c9-129">OUTPUTS</span></span>

### <span data-ttu-id="612c9-130">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="612c9-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="612c9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="612c9-131">NOTES</span></span>

## <span data-ttu-id="612c9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="612c9-132">RELATED LINKS</span></span>

