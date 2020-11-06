---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: fdceee36319d1c9ea950dbf5573b4ba0e3c614ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571545"
---
# <span data-ttu-id="e5f7a-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="e5f7a-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="e5f7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f7a-103">Belirtilen aboneliği silin.</span><span class="sxs-lookup"><span data-stu-id="e5f7a-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="e5f7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5f7a-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5f7a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5f7a-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f7a-106">Belirtilen aboneliği silin.</span><span class="sxs-lookup"><span data-stu-id="e5f7a-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="e5f7a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5f7a-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f7a-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e5f7a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="e5f7a-109">Belirtilen aboneliği silin.</span><span class="sxs-lookup"><span data-stu-id="e5f7a-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="e5f7a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5f7a-110">PARAMETERS</span></span>

### <span data-ttu-id="e5f7a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e5f7a-111">-Force</span></span>
<span data-ttu-id="e5f7a-112">Aboneliği sormadan kaldır</span><span class="sxs-lookup"><span data-stu-id="e5f7a-112">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="e5f7a-113">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e5f7a-113">-SubscriptionId</span></span>
<span data-ttu-id="e5f7a-114">Aboneliğin kimliği.</span><span class="sxs-lookup"><span data-stu-id="e5f7a-114">Id of the subscription.</span></span>

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

### <span data-ttu-id="e5f7a-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="e5f7a-115">-Confirm</span></span>
<span data-ttu-id="e5f7a-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e5f7a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f7a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f7a-117">-WhatIf</span></span>
<span data-ttu-id="e5f7a-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5f7a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5f7a-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5f7a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f7a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f7a-120">CommonParameters</span></span>
<span data-ttu-id="e5f7a-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5f7a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f7a-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f7a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f7a-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5f7a-123">INPUTS</span></span>

## <span data-ttu-id="e5f7a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5f7a-124">OUTPUTS</span></span>

## <span data-ttu-id="e5f7a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5f7a-125">NOTES</span></span>

## <span data-ttu-id="e5f7a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5f7a-126">RELATED LINKS</span></span>

