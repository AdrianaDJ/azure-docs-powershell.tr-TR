---
external help file: ''
Module Name: Azs.Commerce.Admin
online version: https://docs.microsoft.com/powershell/module/azs.commerce.admin/get-azssubscriberusage
schema: 2.0.0
ms.openlocfilehash: 9eed3f6f2a4d07bd48136c50ec173f801b30c928
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937168"
---
# <span data-ttu-id="f4dfe-101">Get-AzsSubscriberUsage</span><span class="sxs-lookup"><span data-stu-id="f4dfe-101">Get-AzsSubscriberUsage</span></span>

## <span data-ttu-id="f4dfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4dfe-102">SYNOPSIS</span></span>
<span data-ttu-id="f4dfe-103">Kullanıcılardan gelen Usage toplamları olan SubscriberUsageAggregates koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-103">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="f4dfe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4dfe-104">SYNTAX</span></span>

```
Get-AzsSubscriberUsage -ReportedEndTime <DateTime> -ReportedStartTime <DateTime> [-SubscriptionId <String[]>]
 [-AggregationGranularity <String>] [-ContinuationToken <String>] [-SubscriberId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f4dfe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4dfe-105">DESCRIPTION</span></span>
<span data-ttu-id="f4dfe-106">Kullanıcılardan gelen Usage toplamları olan SubscriberUsageAggregates koleksiyonunu alır.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-106">Gets a collection of SubscriberUsageAggregates, which are UsageAggregates from users.</span></span>

## <span data-ttu-id="f4dfe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4dfe-107">EXAMPLES</span></span>

### <span data-ttu-id="f4dfe-108">Örnek 1: güne göre toplanan kullanım verilerini al</span><span class="sxs-lookup"><span data-stu-id="f4dfe-108">Example 1: Get usage data aggregated by day</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-31T00:00:00Z" -AggregationGranularity Daily
```

<span data-ttu-id="f4dfe-109">Gün tarafından toplanan tüm kiracıları için 30 Ara 2019 (UTC olarak) tüm gününün kullanım verilerini alın.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-109">Get the usage data for the entire day of 30th Dec 2019 (in UTC) for all tenants under provider aggregated by the day.</span></span>
<span data-ttu-id="f4dfe-110">ReportedStartTime ve Reportedenvseçtime, günlere yuvarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-110">ReportedStartTime and ReportedEndTime must be rounded to days.</span></span>
<span data-ttu-id="f4dfe-111">Hizmet Yöneticisi olarak çağrılırsa, bu işlem tüm kiracının tüm kullanım verilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-111">If called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

### <span data-ttu-id="f4dfe-112">Örnek 2: saatte toplanan kullanım verilerini alma</span><span class="sxs-lookup"><span data-stu-id="f4dfe-112">Example 2: Get usage data aggregated by the hour</span></span>
```powershell
Get-AzsSubscriberUsage -ReportedStartTime "2019-12-30T00:00:00Z" -ReportedEndTime "2019-12-30T02:00:00Z" -AggregationGranularity Hourly
```

<span data-ttu-id="f4dfe-113">Saat esasına göre toplanmış 30 TL 'nin 2019 (UTC)</span><span class="sxs-lookup"><span data-stu-id="f4dfe-113">Get the usage data between  12am - 2am on 30th Dec 2019 (in UTC) aggregated by the hour.</span></span>
<span data-ttu-id="f4dfe-114">ReportedStartTime ve Reportedenvseçtime saate yuvarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-114">ReportedStartTime and ReportedEndTime must be rounded to hours.</span></span>
<span data-ttu-id="f4dfe-115">Aynı şekilde, hizmet yöneticisi olarak çağrılırsa, bu işlem tüm kiracının tüm kullanım verilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-115">Likewise, if called as the service administrator, this effectively shows all usage data for every tenant.</span></span>

## <span data-ttu-id="f4dfe-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4dfe-116">PARAMETERS</span></span>

### <span data-ttu-id="f4dfe-117">-Aggregationparçalı yapı</span><span class="sxs-lookup"><span data-stu-id="f4dfe-117">-AggregationGranularity</span></span>
<span data-ttu-id="f4dfe-118">Toplama ayrıntı düzeyi.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-118">The aggregation granularity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4dfe-119">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="f4dfe-119">-ContinuationToken</span></span>
<span data-ttu-id="f4dfe-120">Devam belirteci.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-120">The continuation token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4dfe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4dfe-121">-DefaultProfile</span></span>
<span data-ttu-id="f4dfe-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4dfe-123">-Reportedenvseçtime</span><span class="sxs-lookup"><span data-stu-id="f4dfe-123">-ReportedEndTime</span></span>
<span data-ttu-id="f4dfe-124">Bildirilen bitiş zamanı (özel).</span><span class="sxs-lookup"><span data-stu-id="f4dfe-124">The reported end time (exclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4dfe-125">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="f4dfe-125">-ReportedStartTime</span></span>
<span data-ttu-id="f4dfe-126">Bildirilen başlangıç zamanı (dahil).</span><span class="sxs-lookup"><span data-stu-id="f4dfe-126">The reported start time (inclusive).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4dfe-127">-SubscriberId</span><span class="sxs-lookup"><span data-stu-id="f4dfe-127">-SubscriberId</span></span>
<span data-ttu-id="f4dfe-128">Kiracı aboneliği tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-128">The tenant subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4dfe-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f4dfe-129">-SubscriptionId</span></span>
<span data-ttu-id="f4dfe-130">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f4dfe-131">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4dfe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4dfe-132">CommonParameters</span></span>
<span data-ttu-id="f4dfe-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4dfe-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f4dfe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4dfe-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4dfe-135">INPUTS</span></span>

## <span data-ttu-id="f4dfe-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4dfe-136">OUTPUTS</span></span>

### <span data-ttu-id="f4dfe-137">Microsoft. Azure. PowerShell. cmdlet. Commerce. modeller. Api20150601Preview. ıusageaggregate</span><span class="sxs-lookup"><span data-stu-id="f4dfe-137">Microsoft.Azure.PowerShell.Cmdlets.Commerce.Models.Api20150601Preview.IUsageAggregate</span></span>



## <span data-ttu-id="f4dfe-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4dfe-138">NOTES</span></span>

## <span data-ttu-id="f4dfe-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4dfe-139">RELATED LINKS</span></span>
