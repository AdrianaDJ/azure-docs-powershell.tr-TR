---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04c79f659f2dcf1d4100151ff0506722482aaad5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107164"
---
# <span data-ttu-id="577d3-101">New-PlanObject</span><span class="sxs-lookup"><span data-stu-id="577d3-101">New-PlanObject</span></span>

## <span data-ttu-id="577d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="577d3-102">SYNOPSIS</span></span>
<span data-ttu-id="577d3-103">Bir plan, kiracıları sunan bir kotalar ve Özellikler paketini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="577d3-103">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="577d3-104">Bir kiracı bu planı temel bulut hizmetlerine erişimi yükseltme teklifi aracılığıyla alabilir.</span><span class="sxs-lookup"><span data-stu-id="577d3-104">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="577d3-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="577d3-105">SYNTAX</span></span>

```
New-PlanObject [[-Description] <String>] [[-Id] <String>] [[-Type] <String>] [[-SkuIds] <String[]>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-ExternalReferenceId] <String>] [[-Name] <String>] [[-DisplayName] <String>] [[-Location] <String>]
 [[-QuotaIds] <String[]>] [[-SubscriptionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="577d3-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="577d3-106">DESCRIPTION</span></span>
<span data-ttu-id="577d3-107">Bir plan, kiracıları sunan bir kotalar ve Özellikler paketini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="577d3-107">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="577d3-108">Bir kiracı bu planı temel bulut hizmetlerine erişimi yükseltme teklifi aracılığıyla alabilir.</span><span class="sxs-lookup"><span data-stu-id="577d3-108">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>

## <span data-ttu-id="577d3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="577d3-109">EXAMPLES</span></span>

### <span data-ttu-id="577d3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="577d3-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="577d3-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="577d3-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="577d3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="577d3-112">PARAMETERS</span></span>

### <span data-ttu-id="577d3-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="577d3-113">-Description</span></span>
<span data-ttu-id="577d3-114">Planın açıklaması.</span><span class="sxs-lookup"><span data-stu-id="577d3-114">Description of the plan.</span></span>

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

### <span data-ttu-id="577d3-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="577d3-115">-DisplayName</span></span>
<span data-ttu-id="577d3-116">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="577d3-116">Display name.</span></span>

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

### <span data-ttu-id="577d3-117">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="577d3-117">-ExternalReferenceId</span></span>
<span data-ttu-id="577d3-118">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="577d3-118">External reference identifier.</span></span>

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

### <span data-ttu-id="577d3-119">-ID</span><span class="sxs-lookup"><span data-stu-id="577d3-119">-Id</span></span>
<span data-ttu-id="577d3-120">Kaynağın URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="577d3-120">URI of the resource.</span></span>

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

### <span data-ttu-id="577d3-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="577d3-121">-Location</span></span>
<span data-ttu-id="577d3-122">Kaynağın konum olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="577d3-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="577d3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="577d3-123">-Name</span></span>
<span data-ttu-id="577d3-124">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="577d3-124">Name of the resource.</span></span>

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

### <span data-ttu-id="577d3-125">-Quotaıds</span><span class="sxs-lookup"><span data-stu-id="577d3-125">-QuotaIds</span></span>
<span data-ttu-id="577d3-126">Planın altındaki kota tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="577d3-126">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="577d3-127">-Skuid 'ler</span><span class="sxs-lookup"><span data-stu-id="577d3-127">-SkuIds</span></span>
<span data-ttu-id="577d3-128">SKU kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="577d3-128">SKU identifiers.</span></span>

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

### <span data-ttu-id="577d3-129">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="577d3-129">-SubscriptionCount</span></span>
<span data-ttu-id="577d3-130">Abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="577d3-130">Subscription count.</span></span>

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

### <span data-ttu-id="577d3-131">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="577d3-131">-Tags</span></span>
<span data-ttu-id="577d3-132">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="577d3-132">List of key-value pairs.</span></span>

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

### <span data-ttu-id="577d3-133">-Tür</span><span class="sxs-lookup"><span data-stu-id="577d3-133">-Type</span></span>
<span data-ttu-id="577d3-134">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="577d3-134">Type of resource.</span></span>

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

### <span data-ttu-id="577d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577d3-135">CommonParameters</span></span>
<span data-ttu-id="577d3-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="577d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577d3-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="577d3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577d3-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="577d3-138">INPUTS</span></span>

## <span data-ttu-id="577d3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="577d3-139">OUTPUTS</span></span>

## <span data-ttu-id="577d3-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="577d3-140">NOTES</span></span>

## <span data-ttu-id="577d3-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="577d3-141">RELATED LINKS</span></span>

