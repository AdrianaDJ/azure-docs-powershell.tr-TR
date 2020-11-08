---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/invoke-azoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Invoke-AzOperationalInsightsQuery.md
ms.openlocfilehash: 528588ac4a85303809b6e287f3e99b06db9f2a6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096122"
---
# <span data-ttu-id="05d87-101">Invoke-AzOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="05d87-101">Invoke-AzOperationalInsightsQuery</span></span>

## <span data-ttu-id="05d87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05d87-102">SYNOPSIS</span></span>
<span data-ttu-id="05d87-103">Belirtilen parametrelere dayalı olarak arama sonuçlarını getirir.</span><span class="sxs-lookup"><span data-stu-id="05d87-103">Returns search results based on the specified parameters.</span></span>

## <span data-ttu-id="05d87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05d87-104">SYNTAX</span></span>

### <span data-ttu-id="05d87-105">By</span><span class="sxs-lookup"><span data-stu-id="05d87-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>] [-Wait <Int32>]
 [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05d87-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="05d87-106">ByWorkspaceObject</span></span>
```
Invoke-AzOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05d87-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="05d87-107">DESCRIPTION</span></span>
<span data-ttu-id="05d87-108">**Invoke-Azoperationalınsightsquery** cmdlet 'i, arama sonuçlarını belirtilen parametrelere göre döndürür.</span><span class="sxs-lookup"><span data-stu-id="05d87-108">The **Invoke-AzOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="05d87-109">Döndürülen nesnenin meta veri özelliğindeki aramanın durumuna erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05d87-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="05d87-110">Durum beklemede olduğunda, arama tamamlanmaz ve sonuçlar arşivden olacaktır.</span><span class="sxs-lookup"><span data-stu-id="05d87-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="05d87-111">Döndürülen nesnenin değer özelliğinden aramanın sonuçlarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05d87-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="05d87-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05d87-112">EXAMPLES</span></span>

### <span data-ttu-id="05d87-113">Örnek 1: sorgu kullanarak arama sonuçları alma</span><span class="sxs-lookup"><span data-stu-id="05d87-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="05d87-114">Yüklendikten sonra $queryResults. sonuçlar Sorgunuzdaki tüm sonuç satırlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="05d87-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="05d87-115">Örnek 2: $results dönüştürün. Diziye sonuç IEnumerable</span><span class="sxs-lookup"><span data-stu-id="05d87-115">Example 2: Convert $results.Result IEnumerable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($queryResults.Results)
...
```

<span data-ttu-id="05d87-116">Bazı sorgular, çok büyük veri kümelerinin döndürülmesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="05d87-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="05d87-117">Bu nedenle, cmdlet 'in varsayılan davranışı bellek maliyetini azaltmak için IEnumerable döndürmelidir.</span><span class="sxs-lookup"><span data-stu-id="05d87-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="05d87-118">Sonuç dizisi olmasını tercih ediyorsanız, IEnumerable 'yu bir diziye dönüştürmek için LINQ sıralanabilir. ToArray () genişletme yöntemini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05d87-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="05d87-119">Örnek 3: belirli bir zaman diliminde sorgu kullanarak arama sonuçları alma</span><span class="sxs-lookup"><span data-stu-id="05d87-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="05d87-120">Bu sorgudaki sonuçlar son 24 saat ile sınırlanacak.</span><span class="sxs-lookup"><span data-stu-id="05d87-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="05d87-121">Örnek 4: sorgu sonucuna işleme & istatistiklerini ekleme</span><span class="sxs-lookup"><span data-stu-id="05d87-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="05d87-122">[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Oluşturma ve istatistik bilgileri hakkında bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="05d87-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="05d87-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05d87-123">PARAMETERS</span></span>

### <span data-ttu-id="05d87-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="05d87-124">-AsJob</span></span>
<span data-ttu-id="05d87-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="05d87-125">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d87-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d87-126">-DefaultProfile</span></span>
<span data-ttu-id="05d87-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05d87-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05d87-128">-Includerender</span><span class="sxs-lookup"><span data-stu-id="05d87-128">-IncludeRender</span></span>
<span data-ttu-id="05d87-129">Belirtilmişse, metrik sorguların işleme bilgileri yanıta dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="05d87-129">If specified, rendering information for metric queries will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d87-130">-Includestatistics</span><span class="sxs-lookup"><span data-stu-id="05d87-130">-IncludeStatistics</span></span>
<span data-ttu-id="05d87-131">Belirtilmişse, sorgu istatistikleri yanıta dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="05d87-131">If specified, query statistics will be included in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d87-132">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="05d87-132">-Query</span></span>
<span data-ttu-id="05d87-133">Yürütülecek sorgu.</span><span class="sxs-lookup"><span data-stu-id="05d87-133">The query to execute.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d87-134">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="05d87-134">-Timespan</span></span>
<span data-ttu-id="05d87-135">Sorguyu bağlama aralığı.</span><span class="sxs-lookup"><span data-stu-id="05d87-135">The timespan to bound the query by.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d87-136">-Bekleme</span><span class="sxs-lookup"><span data-stu-id="05d87-136">-Wait</span></span>
<span data-ttu-id="05d87-137">Sunucunun sorguyu işlemeye harcadıkları süre için bir üst sınır koyar.</span><span class="sxs-lookup"><span data-stu-id="05d87-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="05d87-138">Öğrenmek https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="05d87-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d87-139">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="05d87-139">-Workspace</span></span>
<span data-ttu-id="05d87-140">Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="05d87-140">The workspace</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05d87-141">-</span><span class="sxs-lookup"><span data-stu-id="05d87-141">-WorkspaceId</span></span>
<span data-ttu-id="05d87-142">Çalışma alanı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="05d87-142">The workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05d87-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d87-143">CommonParameters</span></span>
<span data-ttu-id="05d87-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05d87-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d87-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05d87-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d87-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05d87-146">INPUTS</span></span>

### <span data-ttu-id="05d87-147">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="05d87-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="05d87-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05d87-148">OUTPUTS</span></span>

### <span data-ttu-id="05d87-149">Microsoft. Azure. Commands. Operationalınsights. model. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="05d87-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="05d87-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05d87-150">NOTES</span></span>

## <span data-ttu-id="05d87-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05d87-151">RELATED LINKS</span></span>
