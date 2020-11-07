---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d76356e99419ff345e2eccc025c91637417de1a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761733"
---
# <span data-ttu-id="ec906-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="ec906-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="ec906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec906-102">SYNOPSIS</span></span>
<span data-ttu-id="ec906-103">Belirtilen kiracı aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ec906-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="ec906-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec906-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec906-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec906-105">DESCRIPTION</span></span>
<span data-ttu-id="ec906-106">Belirtilen kiracı aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ec906-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="ec906-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec906-107">EXAMPLES</span></span>

### <span data-ttu-id="ec906-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ec906-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="ec906-109">Belirtilen kiracı aboneliğini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ec906-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="ec906-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec906-110">PARAMETERS</span></span>

### <span data-ttu-id="ec906-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ec906-111">-Force</span></span>
<span data-ttu-id="ec906-112">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="ec906-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="ec906-113">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ec906-113">-SubscriptionId</span></span>
<span data-ttu-id="ec906-114">Abonelik kimliği parametresi.</span><span class="sxs-lookup"><span data-stu-id="ec906-114">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="ec906-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec906-115">-Confirm</span></span>
<span data-ttu-id="ec906-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec906-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec906-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec906-117">-WhatIf</span></span>
<span data-ttu-id="ec906-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec906-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec906-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec906-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec906-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec906-120">CommonParameters</span></span>
<span data-ttu-id="ec906-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec906-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec906-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec906-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec906-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec906-123">INPUTS</span></span>

## <span data-ttu-id="ec906-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec906-124">OUTPUTS</span></span>

## <span data-ttu-id="ec906-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec906-125">NOTES</span></span>

## <span data-ttu-id="ec906-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec906-126">RELATED LINKS</span></span>
