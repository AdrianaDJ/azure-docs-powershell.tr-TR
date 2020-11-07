---
external help file: Microsoft.Azure.PowerShell.Cmdlets.UsageAggregates.dll-Help.xml
Module Name: Az.Billing
ms.assetid: 52B3ECCB-80E5-4E16-954A-B83D0BDC7E22
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-usageaggregates
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-UsageAggregates.md
ms.openlocfilehash: 35324b558d673f71d9007a63c578d77d69a5f338
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753136"
---
# <span data-ttu-id="81efc-101">Get-UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="81efc-101">Get-UsageAggregates</span></span>

## <span data-ttu-id="81efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81efc-102">SYNOPSIS</span></span>
<span data-ttu-id="81efc-103">Bildirilen Azure aboneliği kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="81efc-103">Gets the reported Azure subscription usage details.</span></span>

## <span data-ttu-id="81efc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81efc-104">SYNTAX</span></span>

```
Get-UsageAggregates -ReportedStartTime <DateTime> -ReportedEndTime <DateTime>
 [-AggregationGranularity <AggregationGranularity>] [-ShowDetails <Boolean>] [-ContinuationToken <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81efc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81efc-105">DESCRIPTION</span></span>
<span data-ttu-id="81efc-106">**Get-Usagetoplamaları** cmdlet 'i aşağıdaki özellikler tarafından toplanan Azure aboneliği kullanımı verilerini alır:</span><span class="sxs-lookup"><span data-stu-id="81efc-106">The **Get-UsageAggregates** cmdlet gets aggregated Azure subscription usage data by the following properties:</span></span> 
- <span data-ttu-id="81efc-107">Kullanım rapor edildiğinde başlangıç ve bitiş saatleri.</span><span class="sxs-lookup"><span data-stu-id="81efc-107">Start and end times of when the usage was reported.</span></span>
- <span data-ttu-id="81efc-108">Günlük veya saatlik, toplama duyarlılığı.</span><span class="sxs-lookup"><span data-stu-id="81efc-108">Aggregation precision, either daily or hourly.</span></span>
- <span data-ttu-id="81efc-109">Aynı kaynağın birden çok örneği için örnek düzeyi ayrıntısı.</span><span class="sxs-lookup"><span data-stu-id="81efc-109">Instance level detail for multiple instances of the same resource.</span></span>
<span data-ttu-id="81efc-110">Tutarlı sonuçlar için, döndürülen veriler, kullanım ayrıntılarının Azure kaynağı tarafından raporlanma sırasında temel alınarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="81efc-110">For consistent results, the returned data is based on when the usage details were reported by the Azure resource.</span></span>
<span data-ttu-id="81efc-111">Daha fazla bilgi için bkz: Azure Faturalandırma REST API https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c başvurusu https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) .</span><span class="sxs-lookup"><span data-stu-id="81efc-111">For more information, see Azure Billing REST API Referencehttps://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c (https://msdn.microsoft.com/library/azure/1ea5b323-54bb-423d-916f-190de96c6a3c) in the Microsoft Developer Network library.</span></span>

## <span data-ttu-id="81efc-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81efc-112">EXAMPLES</span></span>

### <span data-ttu-id="81efc-113">Örnek 1: abonelik verilerini alma</span><span class="sxs-lookup"><span data-stu-id="81efc-113">Example 1: Retrieve subscription data</span></span>
```
PS C:\>Get-UsageAggregates -ReportedStartTime "5/2/2015" -ReportedEndTime "5/5/2015"
```

<span data-ttu-id="81efc-114">Bu komut, 5/2/2015 ile 5/5/2015 arasındaki abonelik için bildirilen kullanım verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="81efc-114">This command retrieves the reported usage data for the subscription between 5/2/2015 and 5/5/2015.</span></span>

## <span data-ttu-id="81efc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81efc-115">PARAMETERS</span></span>

### <span data-ttu-id="81efc-116">-Aggregationparçalı yapı</span><span class="sxs-lookup"><span data-stu-id="81efc-116">-AggregationGranularity</span></span>
<span data-ttu-id="81efc-117">Verilerin toplama hassasiyetini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81efc-117">Specifies the aggregation precision of the data.</span></span>
<span data-ttu-id="81efc-118">Geçerli değerler: günlük ve saatlik.</span><span class="sxs-lookup"><span data-stu-id="81efc-118">Valid values are: Daily and Hourly.</span></span>
<span data-ttu-id="81efc-119">Varsayılan değer günlük değeridir.</span><span class="sxs-lookup"><span data-stu-id="81efc-119">The default value is Daily.</span></span>

```yaml
Type: Microsoft.Azure.Commerce.UsageAggregates.Models.AggregationGranularity
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Hourly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81efc-120">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="81efc-120">-ContinuationToken</span></span>
<span data-ttu-id="81efc-121">Önceki çağrıda bulunan Yanıt gövdesinden alınan devam belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81efc-121">Specifies the continuation token that was retrieved from the response body in the previous call.</span></span>
<span data-ttu-id="81efc-122">Büyük bir sonuç kümesi için, süreklilik belirteçleri kullanılarak yanıtlar disk belleğine alınır.</span><span class="sxs-lookup"><span data-stu-id="81efc-122">For a large result set, responses are paged by using continuation tokens.</span></span>
<span data-ttu-id="81efc-123">Devam belirteci ilerleme için bir yer işareti görevi görür.</span><span class="sxs-lookup"><span data-stu-id="81efc-123">The continuation token serves as a bookmark for progress.</span></span>
<span data-ttu-id="81efc-124">Bu parametreyi belirtmezseniz, veriler, *Reportedstarttime* 'te belirtilen günün başından veya saatte alınır.</span><span class="sxs-lookup"><span data-stu-id="81efc-124">If you do not specify this parameter, the data is retrieved from the beginning of the day or hour specified in *ReportedStartTime*.</span></span>
<span data-ttu-id="81efc-125">Veri olan Yanıtla sayfasındaki bir sonraki bağlantıyı izlemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="81efc-125">We recommend that you follow the next link in the response to page though the data.</span></span>

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

### <span data-ttu-id="81efc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81efc-126">-DefaultProfile</span></span>
<span data-ttu-id="81efc-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="81efc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81efc-128">-Reportedenvseçtime</span><span class="sxs-lookup"><span data-stu-id="81efc-128">-ReportedEndTime</span></span>
<span data-ttu-id="81efc-129">Azure Faturalandırma sistemi 'nde kaynak kullanımının ne zaman kaydedildiğini belirten rapor.</span><span class="sxs-lookup"><span data-stu-id="81efc-129">Specifies the reported end time for when resource usage was recorded in the Azure billing system.</span></span>
<span data-ttu-id="81efc-130">Azure, dünya genelinde birden çok veri merkezini kapsayan dağıtılmış bir sistemdir, bu nedenle Kaynağın fiili kullanım süresi olan ve kullanım olayının, kaynak kullanımı bildirilen zamanı olan faturalandırma sistemine eriştiği zaman arasında bir gecikme vardır.</span><span class="sxs-lookup"><span data-stu-id="81efc-130">Azure is a distributed system, spanning multiple datacenters around the world, so there is a delay between when the resource was actually consumed, which is the resource usage time, and when the usage event reached the billing system, which is the resource usage reported time.</span></span>
<span data-ttu-id="81efc-131">Bir zaman aralığı için raporlanan bir aboneliğin tüm kullanım olaylarını almak için, bildirilen sürede sorgulama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81efc-131">In order to get all usage events for a subscription that are reported for a time period, you query by reported time.</span></span>
<span data-ttu-id="81efc-132">Bildirilen sürede sorgulama yapsanız da cmdlet, yanıt verilerini kaynak kullanım zamanına göre toplar.</span><span class="sxs-lookup"><span data-stu-id="81efc-132">Even though you query by reported time, the cmdlet aggregates the response data by the resource usage time.</span></span>
<span data-ttu-id="81efc-133">Kaynak kullanım verileri, verilerin çözümlenmesi için yararlı bir Özet.</span><span class="sxs-lookup"><span data-stu-id="81efc-133">The resource usage data is the useful pivot for analyzing the data.</span></span>

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

### <span data-ttu-id="81efc-134">-ReportedStartTime</span><span class="sxs-lookup"><span data-stu-id="81efc-134">-ReportedStartTime</span></span>
<span data-ttu-id="81efc-135">Azure Faturalandırma sistemine kaynak kullanımının kaydedildiği bildirilen başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81efc-135">Specifies the reported start time for when resource usage was recorded in the Azure billing system.</span></span>

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

### <span data-ttu-id="81efc-136">-ShowDetails</span><span class="sxs-lookup"><span data-stu-id="81efc-136">-ShowDetails</span></span>
<span data-ttu-id="81efc-137">Bu cmdlet 'in kullanım verileriyle örnek düzeyi ayrıntıları verip vermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="81efc-137">Indicates whether this cmdlet returns instance-level details with the usage data.</span></span>
<span data-ttu-id="81efc-138">Varsayılan değer $True.</span><span class="sxs-lookup"><span data-stu-id="81efc-138">The default value is $True.</span></span>
<span data-ttu-id="81efc-139">$False, hizmet, sunucu tarafında sonuçları toplar ve daha az toplam grup döndürür.</span><span class="sxs-lookup"><span data-stu-id="81efc-139">If $False, the service aggregates the results on the server side, and therefore returns fewer aggregate groups.</span></span>
<span data-ttu-id="81efc-140">Örneğin, üç Web sitesi çalıştırıyorsanız, varsayılan olarak Web sitesi tüketimi için üç satır öğesi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="81efc-140">For example, if you are running three websites, by default you will get three line items for website consumption.</span></span>
<span data-ttu-id="81efc-141">Bununla birlikte, değer $False, aynı **SubscriptionID** , **meterId** , **usagestarttime** ve **usagebitişsaati** için tüm veriler tek satırlı bir öğeye daraltılmıştır.</span><span class="sxs-lookup"><span data-stu-id="81efc-141">However, when the value is $False, all the data for the same **subscriptionId** , **meterId** , **usageStartTime** , and **usageEndTime** is collapsed into a single line item.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81efc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81efc-142">CommonParameters</span></span>
<span data-ttu-id="81efc-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81efc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81efc-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81efc-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81efc-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81efc-145">INPUTS</span></span>

### <span data-ttu-id="81efc-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="81efc-146">None</span></span>

## <span data-ttu-id="81efc-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81efc-147">OUTPUTS</span></span>

### <span data-ttu-id="81efc-148">Microsoft. Azure. Commerce. Usagetoplamagetresponse</span><span class="sxs-lookup"><span data-stu-id="81efc-148">Microsoft.Azure.Commerce.UsageAggregates.Models.UsageAggregationGetResponse</span></span>

## <span data-ttu-id="81efc-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81efc-149">NOTES</span></span>

## <span data-ttu-id="81efc-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81efc-150">RELATED LINKS</span></span>
