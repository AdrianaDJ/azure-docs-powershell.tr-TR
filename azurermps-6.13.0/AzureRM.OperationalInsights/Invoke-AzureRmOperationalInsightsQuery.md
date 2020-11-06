---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/invoke-azurermoperationalinsightsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Invoke-AzureRmOperationalInsightsQuery.md
ms.openlocfilehash: 6672bb6f788b06896fdfe9cde44c68639077e5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589406"
---
# <span data-ttu-id="a6684-101">Invoke-AzureRmOperationalInsightsQuery</span><span class="sxs-lookup"><span data-stu-id="a6684-101">Invoke-AzureRmOperationalInsightsQuery</span></span>

## <span data-ttu-id="a6684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6684-102">SYNOPSIS</span></span>
<span data-ttu-id="a6684-103">Belirtilen parametrelere dayalı olarak arama sonuçlarını getirir.</span><span class="sxs-lookup"><span data-stu-id="a6684-103">Returns search results based on the specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6684-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6684-104">SYNTAX</span></span>

### <span data-ttu-id="a6684-105">By</span><span class="sxs-lookup"><span data-stu-id="a6684-105">ByWorkspaceId (Default)</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -WorkspaceId <String> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6684-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="a6684-106">ByWorkspaceObject</span></span>
```
Invoke-AzureRmOperationalInsightsQuery -Workspace <PSWorkspace> -Query <String> [-Timespan <TimeSpan>]
 [-Wait <Int32>] [-IncludeRender] [-IncludeStatistics] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6684-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6684-107">DESCRIPTION</span></span>
<span data-ttu-id="a6684-108">**Invoke-Azurermoperationalınsightsquery** cmdlet 'i, arama sonuçlarını belirtilen parametrelere göre döndürür.</span><span class="sxs-lookup"><span data-stu-id="a6684-108">The **Invoke-AzureRmOperationalInsightsQuery** cmdlet returns the search results based on the specified parameters.</span></span>
<span data-ttu-id="a6684-109">Döndürülen nesnenin meta veri özelliğindeki aramanın durumuna erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6684-109">You can access the status of the search in the Metadata property of the returned object.</span></span>
<span data-ttu-id="a6684-110">Durum beklemede olduğunda, arama tamamlanmaz ve sonuçlar arşivden olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a6684-110">If the status is Pending, then the search has not completed, and the results will be from the archive.</span></span>
<span data-ttu-id="a6684-111">Döndürülen nesnenin değer özelliğinden aramanın sonuçlarını alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6684-111">You can retrieve the results of the search from the Value property of the returned object.</span></span>

## <span data-ttu-id="a6684-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6684-112">EXAMPLES</span></span>

### <span data-ttu-id="a6684-113">Örnek 1: sorgu kullanarak arama sonuçları alma</span><span class="sxs-lookup"><span data-stu-id="a6684-113">Example 1: Get search results using a query</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="a6684-114">Yüklendikten sonra $queryResults. sonuçlar Sorgunuzdaki tüm sonuç satırlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="a6684-114">Once invoked, $queryResults.Results will contain all of the resulting rows from your query.</span></span>

### <span data-ttu-id="a6684-115">Örnek 2: $results dönüştürün. Bir diziye</span><span class="sxs-lookup"><span data-stu-id="a6684-115">Example 2: Convert $results.Result IEnumberable to an array</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10"
PS C:\> $resultsArray = [System.Linq.Enumerable]::ToArray($results.Results)
...
```

<span data-ttu-id="a6684-116">Bazı sorgular, çok büyük veri kümelerinin döndürülmesine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="a6684-116">Some queries can result in very large data sets being returned.</span></span> <span data-ttu-id="a6684-117">Bu nedenle, cmdlet 'in varsayılan davranışı bellek maliyetini azaltmak için IEnumerable döndürmelidir.</span><span class="sxs-lookup"><span data-stu-id="a6684-117">Because of this, the default behavior of the cmdlet is to return an IEnumerable to reduce memory costs.</span></span> <span data-ttu-id="a6684-118">Sonuç dizisi olmasını tercih ediyorsanız, IEnumerable 'yu bir diziye dönüştürmek için LINQ sıralanabilir. ToArray () genişletme yöntemini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6684-118">If you'd prefer to have an array of results, you can use the LINQ Enumerable.ToArray() extension method to convert the IEnumerable to an array.</span></span>

### <span data-ttu-id="a6684-119">Örnek 3: belirli bir zaman diliminde sorgu kullanarak arama sonuçları alma</span><span class="sxs-lookup"><span data-stu-id="a6684-119">Example 3: Get search results using a query over a specific timeframe</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -Timespan (New-TimeSpan -Hours 24)
PS C:\> $queryResults.Results
...
```

<span data-ttu-id="a6684-120">Bu sorgudaki sonuçlar son 24 saat ile sınırlanacak.</span><span class="sxs-lookup"><span data-stu-id="a6684-120">The results from this query will be limited to the past 24 hours.</span></span>

### <span data-ttu-id="a6684-121">Örnek 4: sorgu sonucuna işleme & istatistiklerini ekleme</span><span class="sxs-lookup"><span data-stu-id="a6684-121">Example 4: Include render & statistics in query result</span></span>
```
PS C:\> $queryResults = Invoke-AzureRmOperationalInsightsQuery -WorkspaceId "63613592-b6f7-4c3d-a390-22ba13102111" -Query "union * | take 10" -IncludeRender -IncludeStatistics
PS C:\> $queryResults.Results
...
PS C:\> $queryResults.Render
...
PS C:\> $queryResults.Statistics
...
```

<span data-ttu-id="a6684-122">[https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions)Oluşturma ve istatistik bilgileri hakkında bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="a6684-122">See [https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions](https://dev.loganalytics.io/documentation/Using-the-API/RequestOptions) for details on the render and statistics info.</span></span>

## <span data-ttu-id="a6684-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6684-123">PARAMETERS</span></span>

### <span data-ttu-id="a6684-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="a6684-124">-AsJob</span></span>
<span data-ttu-id="a6684-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a6684-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6684-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6684-126">-DefaultProfile</span></span>
<span data-ttu-id="a6684-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6684-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6684-128">-Includerender</span><span class="sxs-lookup"><span data-stu-id="a6684-128">-IncludeRender</span></span>
<span data-ttu-id="a6684-129">Belirtilmişse, metrik sorguların işleme bilgileri yanıta dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="a6684-129">If specified, rendering information for metric queries will be included in the response.</span></span>

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

### <span data-ttu-id="a6684-130">-Includestatistics</span><span class="sxs-lookup"><span data-stu-id="a6684-130">-IncludeStatistics</span></span>
<span data-ttu-id="a6684-131">Belirtilmişse, sorgu istatistikleri yanıta dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="a6684-131">If specified, query statistics will be included in the response.</span></span>

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

### <span data-ttu-id="a6684-132">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="a6684-132">-Query</span></span>
<span data-ttu-id="a6684-133">Yürütülecek sorgu.</span><span class="sxs-lookup"><span data-stu-id="a6684-133">The query to execute.</span></span>

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

### <span data-ttu-id="a6684-134">-TimeSpan</span><span class="sxs-lookup"><span data-stu-id="a6684-134">-Timespan</span></span>
<span data-ttu-id="a6684-135">Sorguyu bağlama aralığı.</span><span class="sxs-lookup"><span data-stu-id="a6684-135">The timespan to bound the query by.</span></span>

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

### <span data-ttu-id="a6684-136">-Bekleme</span><span class="sxs-lookup"><span data-stu-id="a6684-136">-Wait</span></span>
<span data-ttu-id="a6684-137">Sunucunun sorguyu işlemeye harcadıkları süre için bir üst sınır koyar.</span><span class="sxs-lookup"><span data-stu-id="a6684-137">Puts an upper bound on the amount of time the server will spend processing the query.</span></span>
<span data-ttu-id="a6684-138">Öğrenmek https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span><span class="sxs-lookup"><span data-stu-id="a6684-138">See: https://dev.loganalytics.io/documentation/Using-the-API/Timeouts</span></span>

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

### <span data-ttu-id="a6684-139">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="a6684-139">-Workspace</span></span>
<span data-ttu-id="a6684-140">Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="a6684-140">The workspace</span></span>

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

### <span data-ttu-id="a6684-141">-</span><span class="sxs-lookup"><span data-stu-id="a6684-141">-WorkspaceId</span></span>
<span data-ttu-id="a6684-142">Çalışma alanı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a6684-142">The workspace ID.</span></span>

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

### <span data-ttu-id="a6684-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6684-143">CommonParameters</span></span>
<span data-ttu-id="a6684-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6684-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6684-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6684-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6684-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6684-146">INPUTS</span></span>

### <span data-ttu-id="a6684-147">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a6684-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="a6684-148">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a6684-148">Parameters: Workspace (ByValue)</span></span>

## <span data-ttu-id="a6684-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6684-149">OUTPUTS</span></span>

### <span data-ttu-id="a6684-150">Microsoft. Azure. Commands. Operationalınsights. model. PSQueryResponse</span><span class="sxs-lookup"><span data-stu-id="a6684-150">Microsoft.Azure.Commands.OperationalInsights.Models.PSQueryResponse</span></span>

## <span data-ttu-id="a6684-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6684-151">NOTES</span></span>

## <span data-ttu-id="a6684-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6684-152">RELATED LINKS</span></span>
