---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b82dadf9a9e26b0023872378d41e4978e18436ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571801"
---
# <span data-ttu-id="d13bf-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="d13bf-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="d13bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d13bf-102">SYNOPSIS</span></span>
<span data-ttu-id="d13bf-103">Abonelik planını siler.</span><span class="sxs-lookup"><span data-stu-id="d13bf-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="d13bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d13bf-104">SYNTAX</span></span>

### <span data-ttu-id="d13bf-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d13bf-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d13bf-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d13bf-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d13bf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d13bf-107">DESCRIPTION</span></span>
<span data-ttu-id="d13bf-108">Abonelik planını siler.</span><span class="sxs-lookup"><span data-stu-id="d13bf-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="d13bf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d13bf-109">EXAMPLES</span></span>

### <span data-ttu-id="d13bf-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d13bf-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="d13bf-111">Abonelik planını silme.</span><span class="sxs-lookup"><span data-stu-id="d13bf-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="d13bf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d13bf-112">PARAMETERS</span></span>

### <span data-ttu-id="d13bf-113">-Tanışın kimliği</span><span class="sxs-lookup"><span data-stu-id="d13bf-113">-AcquisitionId</span></span>
<span data-ttu-id="d13bf-114">Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="d13bf-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13bf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d13bf-115">-Force</span></span>
<span data-ttu-id="d13bf-116">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="d13bf-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="d13bf-117">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d13bf-117">-ResourceId</span></span>
<span data-ttu-id="d13bf-118">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d13bf-118">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d13bf-119">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="d13bf-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="d13bf-120">Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d13bf-120">The target subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d13bf-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="d13bf-121">-Confirm</span></span>
<span data-ttu-id="d13bf-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d13bf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d13bf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d13bf-123">-WhatIf</span></span>
<span data-ttu-id="d13bf-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d13bf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d13bf-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d13bf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d13bf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13bf-126">CommonParameters</span></span>
<span data-ttu-id="d13bf-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d13bf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13bf-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d13bf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13bf-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d13bf-129">INPUTS</span></span>

## <span data-ttu-id="d13bf-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d13bf-130">OUTPUTS</span></span>

## <span data-ttu-id="d13bf-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d13bf-131">NOTES</span></span>

## <span data-ttu-id="d13bf-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d13bf-132">RELATED LINKS</span></span>

