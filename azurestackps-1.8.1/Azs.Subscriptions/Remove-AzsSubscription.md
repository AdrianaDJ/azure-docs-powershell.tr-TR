---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935046"
---
# <span data-ttu-id="12bc0-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="12bc0-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="12bc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12bc0-102">SYNOPSIS</span></span>
<span data-ttu-id="12bc0-103">Belirtilen aboneliği silin.</span><span class="sxs-lookup"><span data-stu-id="12bc0-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="12bc0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12bc0-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12bc0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12bc0-105">DESCRIPTION</span></span>
<span data-ttu-id="12bc0-106">Belirtilen aboneliği silin.</span><span class="sxs-lookup"><span data-stu-id="12bc0-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="12bc0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12bc0-107">EXAMPLES</span></span>

### <span data-ttu-id="12bc0-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="12bc0-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="12bc0-109">Belirtilen aboneliği silin.</span><span class="sxs-lookup"><span data-stu-id="12bc0-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="12bc0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12bc0-110">PARAMETERS</span></span>

### <span data-ttu-id="12bc0-111">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="12bc0-111">-SubscriptionId</span></span>
<span data-ttu-id="12bc0-112">Aboneliğin kimliği.</span><span class="sxs-lookup"><span data-stu-id="12bc0-112">Id of the subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12bc0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="12bc0-113">-Force</span></span>
<span data-ttu-id="12bc0-114">Aboneliği sormadan kaldır</span><span class="sxs-lookup"><span data-stu-id="12bc0-114">Remove subscription without prompting</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12bc0-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12bc0-115">-WhatIf</span></span>
<span data-ttu-id="12bc0-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12bc0-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12bc0-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="12bc0-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12bc0-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="12bc0-118">-Confirm</span></span>
<span data-ttu-id="12bc0-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12bc0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12bc0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12bc0-120">CommonParameters</span></span>
<span data-ttu-id="12bc0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12bc0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12bc0-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12bc0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12bc0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12bc0-123">INPUTS</span></span>

## <span data-ttu-id="12bc0-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12bc0-124">OUTPUTS</span></span>

## <span data-ttu-id="12bc0-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12bc0-125">NOTES</span></span>

## <span data-ttu-id="12bc0-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12bc0-126">RELATED LINKS</span></span>
