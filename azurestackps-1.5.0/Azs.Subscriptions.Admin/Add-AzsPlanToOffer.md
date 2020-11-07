---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e501feeea3509725b53c85007934c8e682de48a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761682"
---
# <span data-ttu-id="c96f3-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="c96f3-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="c96f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c96f3-102">SYNOPSIS</span></span>
<span data-ttu-id="c96f3-103">Bir planı teklife bağlar.</span><span class="sxs-lookup"><span data-stu-id="c96f3-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="c96f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c96f3-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c96f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c96f3-105">DESCRIPTION</span></span>
<span data-ttu-id="c96f3-106">Bir planı teklife bağlar.</span><span class="sxs-lookup"><span data-stu-id="c96f3-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="c96f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c96f3-107">EXAMPLES</span></span>

### <span data-ttu-id="c96f3-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c96f3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="c96f3-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c96f3-109">PARAMETERS</span></span>

### <span data-ttu-id="c96f3-110">-Force</span><span class="sxs-lookup"><span data-stu-id="c96f3-110">-Force</span></span>
<span data-ttu-id="c96f3-111">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="c96f3-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="c96f3-112">-Maxtanışan</span><span class="sxs-lookup"><span data-stu-id="c96f3-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="c96f3-113">Abonelere göre en fazla Alım sayısı</span><span class="sxs-lookup"><span data-stu-id="c96f3-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c96f3-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="c96f3-114">-OfferName</span></span>
<span data-ttu-id="c96f3-115">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="c96f3-115">Name of an offer.</span></span>

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

### <span data-ttu-id="c96f3-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="c96f3-116">-PlanLinkType</span></span>
<span data-ttu-id="c96f3-117">Plan bağlantısının türü.</span><span class="sxs-lookup"><span data-stu-id="c96f3-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c96f3-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c96f3-118">-PlanName</span></span>
<span data-ttu-id="c96f3-119">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="c96f3-119">Name of the plan.</span></span>

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

### <span data-ttu-id="c96f3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c96f3-120">-ResourceGroupName</span></span>
<span data-ttu-id="c96f3-121">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="c96f3-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c96f3-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="c96f3-122">-Confirm</span></span>
<span data-ttu-id="c96f3-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c96f3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c96f3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c96f3-124">-WhatIf</span></span>
<span data-ttu-id="c96f3-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c96f3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c96f3-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c96f3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c96f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c96f3-127">CommonParameters</span></span>
<span data-ttu-id="c96f3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c96f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c96f3-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c96f3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c96f3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c96f3-130">INPUTS</span></span>

## <span data-ttu-id="c96f3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c96f3-131">OUTPUTS</span></span>

## <span data-ttu-id="c96f3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c96f3-132">NOTES</span></span>

## <span data-ttu-id="c96f3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c96f3-133">RELATED LINKS</span></span>

