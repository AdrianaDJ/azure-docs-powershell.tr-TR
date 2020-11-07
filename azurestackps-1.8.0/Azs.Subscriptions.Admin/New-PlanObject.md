---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934579"
---
# <span data-ttu-id="9a5ee-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="9a5ee-101">New-PlanObject</span></span>

## <span data-ttu-id="9a5ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a5ee-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5ee-103">Bir plan, kiracıları sunan bir kotalar ve Özellikler paketini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="9a5ee-104">Bir kiracı bu planı temel bulut hizmetlerine erişimi yükseltme teklifi aracılığıyla alabilir.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="9a5ee-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a5ee-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="9a5ee-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a5ee-106">DESCRIPTION</span></span>
<span data-ttu-id="9a5ee-107">Bir plan, kiracıları sunan bir kotalar ve Özellikler paketini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="9a5ee-108">Bir kiracı bu planı temel bulut hizmetlerine erişimi yükseltme teklifi aracılığıyla alabilir.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="9a5ee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a5ee-109">EXAMPLES</span></span>

### <span data-ttu-id="9a5ee-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9a5ee-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9a5ee-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="9a5ee-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="9a5ee-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a5ee-112">PARAMETERS</span></span>

### <span data-ttu-id="9a5ee-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9a5ee-113">-Description</span></span>
<span data-ttu-id="9a5ee-114">Planın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-114">Description of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9a5ee-115">-DisplayName</span></span>
<span data-ttu-id="9a5ee-116">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-116">Display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-117">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="9a5ee-117">-ExternalReferenceId</span></span>
<span data-ttu-id="9a5ee-118">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-118">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-119">-ID</span><span class="sxs-lookup"><span data-stu-id="9a5ee-119">-Id</span></span>
<span data-ttu-id="9a5ee-120">Kaynağın URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-120">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="9a5ee-121">-Location</span></span>
<span data-ttu-id="9a5ee-122">Kaynağın konum olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="9a5ee-123">-Name</span></span>
<span data-ttu-id="9a5ee-124">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-124">Name of the resource.</span></span>

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

### <span data-ttu-id="9a5ee-125">-Quotaıds</span><span class="sxs-lookup"><span data-stu-id="9a5ee-125">-QuotaIds</span></span>
<span data-ttu-id="9a5ee-126">Planın altındaki kota tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-126">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-127">-Skuid 'ler</span><span class="sxs-lookup"><span data-stu-id="9a5ee-127">-SkuIds</span></span>
<span data-ttu-id="9a5ee-128">SKU kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-128">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="9a5ee-129">-SubscriptionCount</span></span>
<span data-ttu-id="9a5ee-130">Abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-130">Subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-131">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="9a5ee-131">-Tags</span></span>
<span data-ttu-id="9a5ee-132">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-132">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-133">-Tür</span><span class="sxs-lookup"><span data-stu-id="9a5ee-133">-Type</span></span>
<span data-ttu-id="9a5ee-134">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-134">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5ee-135">CommonParameters</span></span>
<span data-ttu-id="9a5ee-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a5ee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5ee-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a5ee-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5ee-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a5ee-138">INPUTS</span></span>

## <span data-ttu-id="9a5ee-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a5ee-139">OUTPUTS</span></span>

## <span data-ttu-id="9a5ee-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a5ee-140">NOTES</span></span>

## <span data-ttu-id="9a5ee-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a5ee-141">RELATED LINKS</span></span>

