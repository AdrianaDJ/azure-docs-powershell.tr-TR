---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: d11de748c8c86c974b45ac2f171b5eb54b97ee6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939502"
---
# <span data-ttu-id="c4cf9-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c4cf9-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c4cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="c4cf9-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="c4cf9-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4cf9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4cf9-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4cf9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="c4cf9-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="c4cf9-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c4cf9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="c4cf9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4cf9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c4cf9-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="c4cf9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="c4cf9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4cf9-110">PARAMETERS</span></span>

### <span data-ttu-id="c4cf9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4cf9-111">-DefaultProfile</span></span>
<span data-ttu-id="c4cf9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4cf9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c4cf9-113">-Force</span></span>
<span data-ttu-id="c4cf9-114">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="c4cf9-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="c4cf9-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4cf9-115">-Name</span></span>
<span data-ttu-id="c4cf9-116">Yol filtresi kuralının adı</span><span class="sxs-lookup"><span data-stu-id="c4cf9-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="c4cf9-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c4cf9-117">-RouteFilter</span></span>
<span data-ttu-id="c4cf9-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c4cf9-118">The RouteFilter</span></span>

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

### <span data-ttu-id="c4cf9-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4cf9-119">-Confirm</span></span>
<span data-ttu-id="c4cf9-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4cf9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4cf9-121">-WhatIf</span></span>
<span data-ttu-id="c4cf9-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4cf9-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4cf9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4cf9-124">CommonParameters</span></span>
<span data-ttu-id="c4cf9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4cf9-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4cf9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4cf9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4cf9-127">INPUTS</span></span>

### <span data-ttu-id="c4cf9-128">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c4cf9-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c4cf9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4cf9-129">OUTPUTS</span></span>

### <span data-ttu-id="c4cf9-130">Microsoft. Azure. Commands. Network. model. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="c4cf9-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="c4cf9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4cf9-131">NOTES</span></span>

## <span data-ttu-id="c4cf9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4cf9-132">RELATED LINKS</span></span>

