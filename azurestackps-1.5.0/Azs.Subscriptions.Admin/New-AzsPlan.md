---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cddc7e5b3e0d9c7181248e024982293d1418e680
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571605"
---
# <span data-ttu-id="d5c5f-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="d5c5f-101">New-AzsPlan</span></span>

## <span data-ttu-id="d5c5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c5f-103">Yeni plan oluşturur</span><span class="sxs-lookup"><span data-stu-id="d5c5f-103">Creates a new plan</span></span>

## <span data-ttu-id="d5c5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5c5f-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5c5f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="d5c5f-106">Yeni plan oluşturur</span><span class="sxs-lookup"><span data-stu-id="d5c5f-106">Creates a new plan</span></span>

## <span data-ttu-id="d5c5f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5c5f-107">EXAMPLES</span></span>

### <span data-ttu-id="d5c5f-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d5c5f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="d5c5f-109">Yeni plan oluşturur</span><span class="sxs-lookup"><span data-stu-id="d5c5f-109">Creates a new plan</span></span>

## <span data-ttu-id="d5c5f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5c5f-110">PARAMETERS</span></span>

### <span data-ttu-id="d5c5f-111">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d5c5f-111">-Description</span></span>
<span data-ttu-id="d5c5f-112">Planın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-112">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c5f-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d5c5f-113">-DisplayName</span></span>
<span data-ttu-id="d5c5f-114">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-114">Display name.</span></span>

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

### <span data-ttu-id="d5c5f-115">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="d5c5f-115">-ExternalReferenceId</span></span>
<span data-ttu-id="d5c5f-116">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c5f-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="d5c5f-117">-Location</span></span>
<span data-ttu-id="d5c5f-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c5f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5c5f-119">-Name</span></span>
<span data-ttu-id="d5c5f-120">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-120">Name of the plan.</span></span>

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

### <span data-ttu-id="d5c5f-121">-Quotaıds</span><span class="sxs-lookup"><span data-stu-id="d5c5f-121">-QuotaIds</span></span>
<span data-ttu-id="d5c5f-122">Planın altındaki kota tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d5c5f-124">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d5c5f-125">-Skuid 'ler</span><span class="sxs-lookup"><span data-stu-id="d5c5f-125">-SkuIds</span></span>
<span data-ttu-id="d5c5f-126">SKU kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c5f-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="d5c5f-127">-SubscriptionCount</span></span>
<span data-ttu-id="d5c5f-128">Abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-128">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c5f-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5c5f-129">-Confirm</span></span>
<span data-ttu-id="d5c5f-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c5f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c5f-131">-WhatIf</span></span>
<span data-ttu-id="d5c5f-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5c5f-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c5f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c5f-134">CommonParameters</span></span>
<span data-ttu-id="d5c5f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5c5f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c5f-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c5f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c5f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5c5f-137">INPUTS</span></span>

## <span data-ttu-id="d5c5f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5c5f-138">OUTPUTS</span></span>

### <span data-ttu-id="d5c5f-139">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan</span><span class="sxs-lookup"><span data-stu-id="d5c5f-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="d5c5f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5c5f-140">NOTES</span></span>

## <span data-ttu-id="d5c5f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5c5f-141">RELATED LINKS</span></span>

