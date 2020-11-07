---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935143"
---
# <span data-ttu-id="e9864-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="e9864-101">New-AzsPlan</span></span>

## <span data-ttu-id="e9864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9864-102">SYNOPSIS</span></span>
<span data-ttu-id="e9864-103">Yeni plan oluşturur</span><span class="sxs-lookup"><span data-stu-id="e9864-103">Creates a new plan</span></span>

## <span data-ttu-id="e9864-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9864-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9864-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9864-105">DESCRIPTION</span></span>
<span data-ttu-id="e9864-106">Yeni plan oluşturur</span><span class="sxs-lookup"><span data-stu-id="e9864-106">Creates a new plan</span></span>

## <span data-ttu-id="e9864-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9864-107">EXAMPLES</span></span>

### <span data-ttu-id="e9864-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e9864-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="e9864-109">Yeni plan oluşturur</span><span class="sxs-lookup"><span data-stu-id="e9864-109">Creates a new plan</span></span>

## <span data-ttu-id="e9864-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9864-110">PARAMETERS</span></span>

### <span data-ttu-id="e9864-111">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e9864-111">-Description</span></span>
<span data-ttu-id="e9864-112">Planın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="e9864-112">Description of the plan.</span></span>

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

### <span data-ttu-id="e9864-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e9864-113">-DisplayName</span></span>
<span data-ttu-id="e9864-114">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="e9864-114">Display name.</span></span>

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

### <span data-ttu-id="e9864-115">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="e9864-115">-ExternalReferenceId</span></span>
<span data-ttu-id="e9864-116">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e9864-116">External reference identifier.</span></span>

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

### <span data-ttu-id="e9864-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="e9864-117">-Location</span></span>
<span data-ttu-id="e9864-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="e9864-118">Location of the resource.</span></span>

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

### <span data-ttu-id="e9864-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9864-119">-Name</span></span>
<span data-ttu-id="e9864-120">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="e9864-120">Name of the plan.</span></span>

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

### <span data-ttu-id="e9864-121">-Quotaıds</span><span class="sxs-lookup"><span data-stu-id="e9864-121">-QuotaIds</span></span>
<span data-ttu-id="e9864-122">Planın altındaki kota tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="e9864-122">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="e9864-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9864-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9864-124">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e9864-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e9864-125">-Skuid 'ler</span><span class="sxs-lookup"><span data-stu-id="e9864-125">-SkuIds</span></span>
<span data-ttu-id="e9864-126">SKU kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="e9864-126">SKU identifiers.</span></span>

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

### <span data-ttu-id="e9864-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="e9864-127">-SubscriptionCount</span></span>
<span data-ttu-id="e9864-128">Abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="e9864-128">Subscription count.</span></span>

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

### <span data-ttu-id="e9864-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9864-129">-Confirm</span></span>
<span data-ttu-id="e9864-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9864-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9864-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9864-131">-WhatIf</span></span>
<span data-ttu-id="e9864-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9864-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9864-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9864-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9864-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9864-134">CommonParameters</span></span>
<span data-ttu-id="e9864-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9864-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9864-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9864-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9864-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9864-137">INPUTS</span></span>

## <span data-ttu-id="e9864-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9864-138">OUTPUTS</span></span>

### <span data-ttu-id="e9864-139">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan</span><span class="sxs-lookup"><span data-stu-id="e9864-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="e9864-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9864-140">NOTES</span></span>

## <span data-ttu-id="e9864-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9864-141">RELATED LINKS</span></span>

