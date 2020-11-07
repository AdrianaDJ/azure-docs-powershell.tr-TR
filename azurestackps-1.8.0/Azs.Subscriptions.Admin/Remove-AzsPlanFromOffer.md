---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934749"
---
# <span data-ttu-id="f6bdf-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="f6bdf-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="f6bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="f6bdf-103">Planın bir tekliften bağlantısını kesme.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="f6bdf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6bdf-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6bdf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="f6bdf-106">Planın bir tekliften bağlantısını kesme.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="f6bdf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6bdf-107">EXAMPLES</span></span>

### <span data-ttu-id="f6bdf-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f6bdf-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="f6bdf-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6bdf-109">PARAMETERS</span></span>

### <span data-ttu-id="f6bdf-110">-Force</span><span class="sxs-lookup"><span data-stu-id="f6bdf-110">-Force</span></span>
<span data-ttu-id="f6bdf-111">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="f6bdf-112">-Maxtanışan</span><span class="sxs-lookup"><span data-stu-id="f6bdf-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="f6bdf-113">Abonelere göre en fazla Alım sayısı</span><span class="sxs-lookup"><span data-stu-id="f6bdf-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6bdf-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="f6bdf-114">-OfferName</span></span>
<span data-ttu-id="f6bdf-115">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-115">Name of an offer.</span></span>

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

### <span data-ttu-id="f6bdf-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="f6bdf-116">-PlanLinkType</span></span>
<span data-ttu-id="f6bdf-117">Plan bağlantısının türü.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6bdf-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="f6bdf-118">-PlanName</span></span>
<span data-ttu-id="f6bdf-119">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-119">Name of the plan.</span></span>

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

### <span data-ttu-id="f6bdf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6bdf-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6bdf-121">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f6bdf-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6bdf-122">-Confirm</span></span>
<span data-ttu-id="f6bdf-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6bdf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6bdf-124">-WhatIf</span></span>
<span data-ttu-id="f6bdf-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6bdf-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6bdf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6bdf-127">CommonParameters</span></span>
<span data-ttu-id="f6bdf-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6bdf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6bdf-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6bdf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6bdf-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6bdf-130">INPUTS</span></span>

## <span data-ttu-id="f6bdf-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6bdf-131">OUTPUTS</span></span>

## <span data-ttu-id="f6bdf-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6bdf-132">NOTES</span></span>

## <span data-ttu-id="f6bdf-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6bdf-133">RELATED LINKS</span></span>

