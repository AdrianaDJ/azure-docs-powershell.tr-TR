---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934754"
---
# <span data-ttu-id="cc3f6-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="cc3f6-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="cc3f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="cc3f6-103">Abonelik planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="cc3f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc3f6-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc3f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc3f6-105">DESCRIPTION</span></span>
<span data-ttu-id="cc3f6-106">Abonelik planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="cc3f6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc3f6-107">EXAMPLES</span></span>

### <span data-ttu-id="cc3f6-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cc3f6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="cc3f6-109">Abonelik planı oluşturma.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-109">Create an subscription plan.</span></span>

## <span data-ttu-id="cc3f6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc3f6-110">PARAMETERS</span></span>

### <span data-ttu-id="cc3f6-111">-Tanışın kimliği</span><span class="sxs-lookup"><span data-stu-id="cc3f6-111">-AcquisitionId</span></span>
<span data-ttu-id="cc3f6-112">Alım tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc3f6-113">-Plankimliği</span><span class="sxs-lookup"><span data-stu-id="cc3f6-113">-PlanId</span></span>
<span data-ttu-id="cc3f6-114">Kiracı aboneliği bağlamında plan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-114">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc3f6-115">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="cc3f6-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="cc3f6-116">Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc3f6-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc3f6-117">-Confirm</span></span>
<span data-ttu-id="cc3f6-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc3f6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc3f6-119">-WhatIf</span></span>
<span data-ttu-id="cc3f6-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc3f6-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc3f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc3f6-122">CommonParameters</span></span>
<span data-ttu-id="cc3f6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc3f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc3f6-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc3f6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc3f6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc3f6-125">INPUTS</span></span>

## <span data-ttu-id="cc3f6-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc3f6-126">OUTPUTS</span></span>

### <span data-ttu-id="cc3f6-127">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Planalımı</span><span class="sxs-lookup"><span data-stu-id="cc3f6-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="cc3f6-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc3f6-128">NOTES</span></span>

## <span data-ttu-id="cc3f6-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc3f6-129">RELATED LINKS</span></span>
