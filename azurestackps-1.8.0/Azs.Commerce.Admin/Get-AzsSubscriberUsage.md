---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4f45a90d4f8e8c3072393c5dc959885636b64dce
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934554"
---
# <span data-ttu-id="049d6-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="049d6-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="049d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="049d6-102">SYNOPSIS</span></span>
<span data-ttu-id="049d6-103">Belirtilen TimeSpan değeri süresince kullanım verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="049d6-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="049d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="049d6-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="049d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="049d6-105">DESCRIPTION</span></span>
<span data-ttu-id="049d6-106">Belirtilen TimeSpan değeri süresince kullanım verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="049d6-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="049d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="049d6-107">EXAMPLES</span></span>

### <span data-ttu-id="049d6-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="049d6-108">EXAMPLE 1</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="049d6-109">Son 24 saatten kullanım verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="049d6-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="049d6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="049d6-110">PARAMETERS</span></span>

### <span data-ttu-id="049d6-111">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="049d6-111">-SubscriberId</span></span>
<span data-ttu-id="049d6-112">Kiracı aboneliği tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="049d6-112">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="049d6-113">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="049d6-113">-ReportedStartTime</span></span>
<span data-ttu-id="049d6-114">Bildirilen başlangıç zamanı (dahil).</span><span class="sxs-lookup"><span data-stu-id="049d6-114">The reported start time (inclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049d6-115">-Aggregationparçalı yapı</span><span class="sxs-lookup"><span data-stu-id="049d6-115">-AggregationGranularity</span></span>
<span data-ttu-id="049d6-116">Toplama ayrıntı düzeyi.</span><span class="sxs-lookup"><span data-stu-id="049d6-116">The aggregation granularity.</span></span>

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

### <span data-ttu-id="049d6-117">-Atla</span><span class="sxs-lookup"><span data-stu-id="049d6-117">-Skip</span></span>
<span data-ttu-id="049d6-118">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="049d6-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049d6-119">-Reportedenvseçtime</span><span class="sxs-lookup"><span data-stu-id="049d6-119">-ReportedEndTime</span></span>
<span data-ttu-id="049d6-120">Bildirilen bitiş zamanı (özel).</span><span class="sxs-lookup"><span data-stu-id="049d6-120">The reported end time (exclusive).</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049d6-121">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="049d6-121">-ContinuationToken</span></span>
<span data-ttu-id="049d6-122">Devam belirteci.</span><span class="sxs-lookup"><span data-stu-id="049d6-122">The continuation token.</span></span>

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

### <span data-ttu-id="049d6-123">-Üst</span><span class="sxs-lookup"><span data-stu-id="049d6-123">-Top</span></span>
<span data-ttu-id="049d6-124">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="049d6-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="049d6-125">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="049d6-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="049d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049d6-126">CommonParameters</span></span>
<span data-ttu-id="049d6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="049d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049d6-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="049d6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049d6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="049d6-129">INPUTS</span></span>

## <span data-ttu-id="049d6-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="049d6-130">OUTPUTS</span></span>

### <span data-ttu-id="049d6-131">Microsoft. AzureStack. Management. Commerce. admin. modeller. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="049d6-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="049d6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="049d6-132">NOTES</span></span>

## <span data-ttu-id="049d6-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="049d6-133">RELATED LINKS</span></span>
