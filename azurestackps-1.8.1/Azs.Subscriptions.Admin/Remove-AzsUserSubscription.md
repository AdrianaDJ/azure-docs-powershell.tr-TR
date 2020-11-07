---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25411a71a6d8233be55ab25ac99487da0b44bd0b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934875"
---
# <span data-ttu-id="8bdb9-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="8bdb9-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="8bdb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bdb9-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdb9-103">Belirtilen kiracı aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="8bdb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8bdb9-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bdb9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8bdb9-105">DESCRIPTION</span></span>
<span data-ttu-id="8bdb9-106">Belirtilen kiracı aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="8bdb9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8bdb9-107">EXAMPLES</span></span>

### <span data-ttu-id="8bdb9-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8bdb9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="8bdb9-109">Belirtilen kiracı aboneliğini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="8bdb9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8bdb9-110">PARAMETERS</span></span>

### <span data-ttu-id="8bdb9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8bdb9-111">-Force</span></span>
<span data-ttu-id="8bdb9-112">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="8bdb9-113">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="8bdb9-113">-SubscriptionId</span></span>
<span data-ttu-id="8bdb9-114">Abonelik kimliği parametresi.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-114">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="8bdb9-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="8bdb9-115">-Confirm</span></span>
<span data-ttu-id="8bdb9-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bdb9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bdb9-117">-WhatIf</span></span>
<span data-ttu-id="8bdb9-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bdb9-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bdb9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdb9-120">CommonParameters</span></span>
<span data-ttu-id="8bdb9-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8bdb9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdb9-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bdb9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdb9-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8bdb9-123">INPUTS</span></span>

## <span data-ttu-id="8bdb9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8bdb9-124">OUTPUTS</span></span>

## <span data-ttu-id="8bdb9-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8bdb9-125">NOTES</span></span>

## <span data-ttu-id="8bdb9-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8bdb9-126">RELATED LINKS</span></span>

