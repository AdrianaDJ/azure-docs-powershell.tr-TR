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
ms.locfileid: "93761716"
---
# <span data-ttu-id="e3205-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="e3205-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="e3205-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3205-102">SYNOPSIS</span></span>
<span data-ttu-id="e3205-103">Planın bir tekliften bağlantısını kesme.</span><span class="sxs-lookup"><span data-stu-id="e3205-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="e3205-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3205-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3205-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3205-105">DESCRIPTION</span></span>
<span data-ttu-id="e3205-106">Planın bir tekliften bağlantısını kesme.</span><span class="sxs-lookup"><span data-stu-id="e3205-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="e3205-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3205-107">EXAMPLES</span></span>

### <span data-ttu-id="e3205-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3205-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="e3205-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3205-109">PARAMETERS</span></span>

### <span data-ttu-id="e3205-110">-Force</span><span class="sxs-lookup"><span data-stu-id="e3205-110">-Force</span></span>
<span data-ttu-id="e3205-111">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="e3205-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="e3205-112">-Maxtanışan</span><span class="sxs-lookup"><span data-stu-id="e3205-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="e3205-113">Abonelere göre en fazla Alım sayısı</span><span class="sxs-lookup"><span data-stu-id="e3205-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="e3205-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="e3205-114">-OfferName</span></span>
<span data-ttu-id="e3205-115">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="e3205-115">Name of an offer.</span></span>

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

### <span data-ttu-id="e3205-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="e3205-116">-PlanLinkType</span></span>
<span data-ttu-id="e3205-117">Plan bağlantısının türü.</span><span class="sxs-lookup"><span data-stu-id="e3205-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="e3205-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="e3205-118">-PlanName</span></span>
<span data-ttu-id="e3205-119">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="e3205-119">Name of the plan.</span></span>

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

### <span data-ttu-id="e3205-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3205-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3205-121">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e3205-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e3205-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3205-122">-Confirm</span></span>
<span data-ttu-id="e3205-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3205-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3205-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3205-124">-WhatIf</span></span>
<span data-ttu-id="e3205-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3205-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3205-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3205-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3205-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3205-127">CommonParameters</span></span>
<span data-ttu-id="e3205-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3205-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3205-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3205-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3205-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3205-130">INPUTS</span></span>

## <span data-ttu-id="e3205-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3205-131">OUTPUTS</span></span>

## <span data-ttu-id="e3205-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3205-132">NOTES</span></span>

## <span data-ttu-id="e3205-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3205-133">RELATED LINKS</span></span>
