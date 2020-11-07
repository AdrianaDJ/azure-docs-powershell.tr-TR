---
external help file: Azs.Commerce.Admin-help.xml
Module Name: Azs.Commerce.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 12b98727cdb8e6d31fb1aaf1a2215b79a6b982e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761794"
---
# <span data-ttu-id="348aa-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="348aa-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="348aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="348aa-102">SYNOPSIS</span></span>
<span data-ttu-id="348aa-103">Belirtilen TimeSpan değeri süresince kullanım verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="348aa-103">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="348aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="348aa-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage [[-SubscriberId] <String>] [-ReportedStartTime] <DateTime>
 [[-AggregationGranularity] <String>] [[-Skip] <Int32>] [-ReportedEndTime] <DateTime>
 [[-ContinuationToken] <String>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="348aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="348aa-105">DESCRIPTION</span></span>
<span data-ttu-id="348aa-106">Belirtilen TimeSpan değeri süresince kullanım verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="348aa-106">Get usage data from during the specified timespan.</span></span>

## <span data-ttu-id="348aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="348aa-107">EXAMPLES</span></span>

### <span data-ttu-id="348aa-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="348aa-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriberUsage -ReportedStartTime "2017-09-06T00:00:00Z" -ReportedEndTime "2017-09-07T00:00:00Z"
```

<span data-ttu-id="348aa-109">Son 24 saatten kullanım verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="348aa-109">Get usage data from the last 24 hours.</span></span>

## <span data-ttu-id="348aa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="348aa-110">PARAMETERS</span></span>

### <span data-ttu-id="348aa-111">-Aggregationparçalı yapı</span><span class="sxs-lookup"><span data-stu-id="348aa-111">-AggregationGranularity</span></span>
<span data-ttu-id="348aa-112">Toplama ayrıntı düzeyi.</span><span class="sxs-lookup"><span data-stu-id="348aa-112">The aggregation granularity.</span></span>

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

### <span data-ttu-id="348aa-113">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="348aa-113">-ContinuationToken</span></span>
<span data-ttu-id="348aa-114">Devam belirteci.</span><span class="sxs-lookup"><span data-stu-id="348aa-114">The continuation token.</span></span>

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

### <span data-ttu-id="348aa-115">-Reportedenvseçtime</span><span class="sxs-lookup"><span data-stu-id="348aa-115">-ReportedEndTime</span></span>
<span data-ttu-id="348aa-116">Bildirilen bitiş zamanı (özel).</span><span class="sxs-lookup"><span data-stu-id="348aa-116">The reported end time (exclusive).</span></span>

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

### <span data-ttu-id="348aa-117">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="348aa-117">-ReportedStartTime</span></span>
<span data-ttu-id="348aa-118">Bildirilen başlangıç zamanı (dahil).</span><span class="sxs-lookup"><span data-stu-id="348aa-118">The reported start time (inclusive).</span></span>

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

### <span data-ttu-id="348aa-119">-Atla</span><span class="sxs-lookup"><span data-stu-id="348aa-119">-Skip</span></span>
<span data-ttu-id="348aa-120">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="348aa-120">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="348aa-121">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="348aa-121">-SubscriberId</span></span>
<span data-ttu-id="348aa-122">Kiracı aboneliği tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="348aa-122">The tenant subscription identifier.</span></span>

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

### <span data-ttu-id="348aa-123">-Üst</span><span class="sxs-lookup"><span data-stu-id="348aa-123">-Top</span></span>
<span data-ttu-id="348aa-124">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="348aa-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="348aa-125">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="348aa-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="348aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348aa-126">CommonParameters</span></span>
<span data-ttu-id="348aa-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="348aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="348aa-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="348aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348aa-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="348aa-129">INPUTS</span></span>

## <span data-ttu-id="348aa-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="348aa-130">OUTPUTS</span></span>

### <span data-ttu-id="348aa-131">Microsoft. AzureStack. Management. Commerce. admin. modeller. UsageAggregate</span><span class="sxs-lookup"><span data-stu-id="348aa-131">Microsoft.AzureStack.Management.Commerce.Admin.Models.UsageAggregate</span></span>

## <span data-ttu-id="348aa-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="348aa-132">NOTES</span></span>

## <span data-ttu-id="348aa-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="348aa-133">RELATED LINKS</span></span>
