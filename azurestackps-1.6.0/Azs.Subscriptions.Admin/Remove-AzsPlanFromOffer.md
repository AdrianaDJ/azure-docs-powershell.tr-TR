---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9212655ecb5f67dbf459548c48ff6d25420a8537
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572325"
---
# <span data-ttu-id="11b5d-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="11b5d-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="11b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="11b5d-103">Planın bir tekliften bağlantısını kesme.</span><span class="sxs-lookup"><span data-stu-id="11b5d-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="11b5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11b5d-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11b5d-105">DESCRIPTION</span></span>
<span data-ttu-id="11b5d-106">Planın bir tekliften bağlantısını kesme.</span><span class="sxs-lookup"><span data-stu-id="11b5d-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="11b5d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11b5d-107">EXAMPLES</span></span>

### <span data-ttu-id="11b5d-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="11b5d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="11b5d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11b5d-109">PARAMETERS</span></span>

### <span data-ttu-id="11b5d-110">-Force</span><span class="sxs-lookup"><span data-stu-id="11b5d-110">-Force</span></span>
<span data-ttu-id="11b5d-111">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="11b5d-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="11b5d-112">-Maxtanışan</span><span class="sxs-lookup"><span data-stu-id="11b5d-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="11b5d-113">Abonelere göre en fazla Alım sayısı</span><span class="sxs-lookup"><span data-stu-id="11b5d-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="11b5d-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="11b5d-114">-OfferName</span></span>
<span data-ttu-id="11b5d-115">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="11b5d-115">Name of an offer.</span></span>

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

### <span data-ttu-id="11b5d-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="11b5d-116">-PlanLinkType</span></span>
<span data-ttu-id="11b5d-117">Plan bağlantısının türü.</span><span class="sxs-lookup"><span data-stu-id="11b5d-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="11b5d-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="11b5d-118">-PlanName</span></span>
<span data-ttu-id="11b5d-119">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="11b5d-119">Name of the plan.</span></span>

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

### <span data-ttu-id="11b5d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b5d-120">-ResourceGroupName</span></span>
<span data-ttu-id="11b5d-121">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="11b5d-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="11b5d-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="11b5d-122">-Confirm</span></span>
<span data-ttu-id="11b5d-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="11b5d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b5d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b5d-124">-WhatIf</span></span>
<span data-ttu-id="11b5d-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="11b5d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11b5d-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="11b5d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b5d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b5d-127">CommonParameters</span></span>
<span data-ttu-id="11b5d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11b5d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b5d-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b5d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b5d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11b5d-130">INPUTS</span></span>

## <span data-ttu-id="11b5d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11b5d-131">OUTPUTS</span></span>

## <span data-ttu-id="11b5d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11b5d-132">NOTES</span></span>

## <span data-ttu-id="11b5d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11b5d-133">RELATED LINKS</span></span>

