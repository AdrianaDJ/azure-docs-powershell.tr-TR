---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 895819175f9fe4215d926d57c55307bbb4c75ab3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939870"
---
# <span data-ttu-id="2d693-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d693-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="2d693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d693-102">SYNOPSIS</span></span>
<span data-ttu-id="2d693-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="2d693-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d693-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d693-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d693-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d693-105">DESCRIPTION</span></span>
<span data-ttu-id="2d693-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="2d693-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2d693-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d693-107">EXAMPLES</span></span>

### <span data-ttu-id="2d693-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d693-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="2d693-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="2d693-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="2d693-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d693-110">PARAMETERS</span></span>

### <span data-ttu-id="2d693-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="2d693-111">-AsJob</span></span>
<span data-ttu-id="2d693-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2d693-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d693-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d693-113">-DefaultProfile</span></span>
<span data-ttu-id="2d693-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d693-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d693-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2d693-115">-Force</span></span>
<span data-ttu-id="2d693-116">Kaynağın üzerine yazılsın mı?</span><span class="sxs-lookup"><span data-stu-id="2d693-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="2d693-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d693-117">-RouteFilter</span></span>
<span data-ttu-id="2d693-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d693-118">The RouteFilter</span></span>

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

### <span data-ttu-id="2d693-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d693-119">-Confirm</span></span>
<span data-ttu-id="2d693-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d693-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d693-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d693-121">-WhatIf</span></span>
<span data-ttu-id="2d693-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d693-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d693-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d693-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d693-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d693-124">CommonParameters</span></span>
<span data-ttu-id="2d693-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d693-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d693-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d693-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d693-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d693-127">INPUTS</span></span>

### <span data-ttu-id="2d693-128">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d693-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2d693-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d693-129">OUTPUTS</span></span>

### <span data-ttu-id="2d693-130">Microsoft. Azure. Commands. Network. modeller. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="2d693-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="2d693-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d693-131">NOTES</span></span>

## <span data-ttu-id="2d693-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d693-132">RELATED LINKS</span></span>

