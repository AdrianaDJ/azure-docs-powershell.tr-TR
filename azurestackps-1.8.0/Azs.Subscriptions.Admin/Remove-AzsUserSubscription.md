---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25411a71a6d8233be55ab25ac99487da0b44bd0b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934575"
---
# <span data-ttu-id="0aea0-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="0aea0-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="0aea0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aea0-102">SYNOPSIS</span></span>
<span data-ttu-id="0aea0-103">Belirtilen kiracı aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0aea0-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="0aea0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0aea0-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aea0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0aea0-105">DESCRIPTION</span></span>
<span data-ttu-id="0aea0-106">Belirtilen kiracı aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0aea0-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="0aea0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0aea0-107">EXAMPLES</span></span>

### <span data-ttu-id="0aea0-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0aea0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="0aea0-109">Belirtilen kiracı aboneliğini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="0aea0-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="0aea0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0aea0-110">PARAMETERS</span></span>

### <span data-ttu-id="0aea0-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0aea0-111">-Force</span></span>
<span data-ttu-id="0aea0-112">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="0aea0-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="0aea0-113">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0aea0-113">-SubscriptionId</span></span>
<span data-ttu-id="0aea0-114">Abonelik kimliği parametresi.</span><span class="sxs-lookup"><span data-stu-id="0aea0-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aea0-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="0aea0-115">-Confirm</span></span>
<span data-ttu-id="0aea0-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0aea0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aea0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aea0-117">-WhatIf</span></span>
<span data-ttu-id="0aea0-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0aea0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aea0-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0aea0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aea0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aea0-120">CommonParameters</span></span>
<span data-ttu-id="0aea0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0aea0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aea0-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aea0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aea0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0aea0-123">INPUTS</span></span>

## <span data-ttu-id="0aea0-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0aea0-124">OUTPUTS</span></span>

## <span data-ttu-id="0aea0-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0aea0-125">NOTES</span></span>

## <span data-ttu-id="0aea0-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0aea0-126">RELATED LINKS</span></span>

