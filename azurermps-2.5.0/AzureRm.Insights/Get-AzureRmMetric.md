---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
ms.openlocfilehash: 5a0594bc1a90457874a590628076daf7e7d49d8d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938871"
---
# <span data-ttu-id="f774f-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="f774f-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="f774f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f774f-102">SYNOPSIS</span></span>
<span data-ttu-id="f774f-103">Kaynağın metrik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f774f-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f774f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f774f-104">SYNTAX</span></span>

### <span data-ttu-id="f774f-105">GetWithDefaultParameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f774f-105">GetWithDefaultParameters (Default)</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f774f-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="f774f-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Top <Int32>] [-OrderBy <String>] [-MetricNamespace <String>]
 [-ResultType <ResultType>] [-MetricFilter <String>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f774f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f774f-107">DESCRIPTION</span></span>
<span data-ttu-id="f774f-108">**Get-AzureRmMetric** cmdlet 'i, belirli bir kaynağın ölçüm değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f774f-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="f774f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f774f-109">EXAMPLES</span></span>

### <span data-ttu-id="f774f-110">Örnek 1: özetlenmiş çıkış içeren bir metrik alma</span><span class="sxs-lookup"><span data-stu-id="f774f-110">Example 1: Get a metric with summarized output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
DimensionName  : 
DimensionValue : 
Name           : AverageMemoryWorkingSet
EndTime        : 3/20/2015 6:40:46 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, 
                 Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:40:00 PM
TimeGrain      : 00:01:00
Unit           : Bytes
```

<span data-ttu-id="f774f-111">Bu komut, zaman çizgisi 1 dakikalık bir WebSite3 için ölçüm değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f774f-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="f774f-112">Örnek 2: ayrıntılı çıktı içeren bir metrik alın</span><span class="sxs-lookup"><span data-stu-id="f774f-112">Example 2: Get a metric with detailed output</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:37:00 PM
                     Total      : 0
                     Average    : 0.106
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 0.106
                     Average    : 0.064
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 0.064
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : AverageResponseTime
EndTime        : 3/20/2015 6:43:33 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:43:00 PM
TimeGrain      : 00:01:00
Unit           : Seconds
```

<span data-ttu-id="f774f-113">Bu komut, zaman çizgisi 1 dakikalık bir WebSite3 için ölçüm değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f774f-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="f774f-114">Çıktı</span><span class="sxs-lookup"><span data-stu-id="f774f-114">The output is detailed.</span></span>

### <span data-ttu-id="f774f-115">Örnek 3: belirli bir metrik için ayrıntılı çıktı alma</span><span class="sxs-lookup"><span data-stu-id="f774f-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -MetricNames "Requests" -TimeGrain 00:01:00 -DetailedOutput
MetricValues   : 
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:39:00 PM
                     Total      : 1
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:41:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:43:00 PM
                     Total      : 0
                     Average    : 1
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:44:00 PM
                     Total      : 1
                     Average    : 0
                     Count      : 1
                     Last       : 
                     Maximum    : 
                     Minimum    : 
                     Properties : 
                     Timestamp  : 3/20/2015 6:45:00 PM
                     Total      : 0
Properties     : 
DimensionName  : 
DimensionValue : 
Name           : Requests
EndTime        : 3/20/2015 6:47:56 PM
ResourceId     : /subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3
StartTime      : 3/20/2015 5:47:00 PM
TimeGrain      : 00:01:00
Unit           : Count
```

<span data-ttu-id="f774f-116">Bu komut, Istekler için ayrıntılı çıktı alır.</span><span class="sxs-lookup"><span data-stu-id="f774f-116">This command gets detailed output for the Requests metric.</span></span>

### <span data-ttu-id="f774f-117">Örnek 4: belirtilen bir metrik</span><span class="sxs-lookup"><span data-stu-id="f774f-117">Example 4: Get summarized output for a specified metric with specified dimension filter</span></span>
```
PS C:\> $dimFilter = @((New-AzureRmMetricFilter -Dimension City -Operator eq -Values "Seattle","Toronto"), (New-AzureRmMetricDimensionFilter -Dimension AuthenticationType -Operator eq -Values User))

PS C:\> Get-AzureRmMetricValues -ResourceId <resourcId> -MetricName PageViews -TimeGrain PT5M -MetricFilter $dimFilter -StartTime 2018-02-01T12:00:00Z -EndTime 2018-02-01T12:10:00Z -AggregationType -Average
ResourceId  : [ResourceId]
MetricNamespace : Microsoft.Insights/ApplicationInsights
Metric Name :
                    LocalizedValue  : Page Views
                    Value       : PageViews
Unit        : Seconds
Timeseries  :
            City            : Seattle
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 3518

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 1984

            City            : Toronto
            AuthenticationType  : User

                    Timestamp   : 2018-02-01 12:00:00 PM
                    Average     : 894

                    Timestamp   : 2018-02-01 12:05:00 PM
                    Average     : 967
```

<span data-ttu-id="f774f-118">Bu komut, PageViews ölçüsünün belirtilen dimema filtresi ve toplama türü ile özetlenmiş çıktısını alır.</span><span class="sxs-lookup"><span data-stu-id="f774f-118">This command gets summarized output for the PageViews metric with specified dimesion filter and aggregation type.</span></span>

## <span data-ttu-id="f774f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f774f-119">PARAMETERS</span></span>

### <span data-ttu-id="f774f-120">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="f774f-120">-AggregationType</span></span>
<span data-ttu-id="f774f-121">Sorgunun toplama türü</span><span class="sxs-lookup"><span data-stu-id="f774f-121">The aggregation type of the query</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: None, Average, Count, Minimum, Maximum, Total

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f774f-122">-DefaultProfile</span></span>
<span data-ttu-id="f774f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f774f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f774f-124">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="f774f-124">-DetailedOutput</span></span>
<span data-ttu-id="f774f-125">Bu cmdlet 'in ayrıntılı çıkış görüntüleyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f774f-125">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="f774f-126">Varsayılan olarak, çıktı özetlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="f774f-126">By default, output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-127">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="f774f-127">-EndTime</span></span>
<span data-ttu-id="f774f-128">Yerel saatte sorgunun bitiş saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f774f-128">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="f774f-129">Varsayılan geçerli saat.</span><span class="sxs-lookup"><span data-stu-id="f774f-129">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-130">-MetricFilter</span><span class="sxs-lookup"><span data-stu-id="f774f-130">-MetricFilter</span></span>
<span data-ttu-id="f774f-131">Ölçümleri sorgulamak için ölçüm boyutu filtresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f774f-131">Specifies the metric dimension filter to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-132">-MetricName</span><span class="sxs-lookup"><span data-stu-id="f774f-132">-MetricName</span></span>
<span data-ttu-id="f774f-133">Ölçüm adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f774f-133">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: GetWithDefaultParameters
Aliases: MetricNames

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: GetWithFullParameters
Aliases: MetricNames

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-134">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="f774f-134">-MetricNamespace</span></span>
<span data-ttu-id="f774f-135">Ölçümleri sorgulamak için ölçü ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f774f-135">Specifies the metric namespace to query metrics for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-136">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="f774f-136">-OrderBy</span></span>
<span data-ttu-id="f774f-137">Sonuçları sıralarken kullanılacak toplamı ve sıralamanın yönünü belirtir (örnek: Sum ASC).</span><span class="sxs-lookup"><span data-stu-id="f774f-137">Specifies the aggregation to use for sorting results and the direction of the sort (Example: sum asc).</span></span>

```yaml
Type: System.String
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f774f-138">-ResourceId</span></span>
<span data-ttu-id="f774f-139">Ölçümün kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f774f-139">Specifies the resource ID of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-140">-ResultType</span><span class="sxs-lookup"><span data-stu-id="f774f-140">-ResultType</span></span>
<span data-ttu-id="f774f-141">Döndürülecek sonuç türünü belirtir (meta veriler veya veriler).</span><span class="sxs-lookup"><span data-stu-id="f774f-141">Specifies the result type to be returned (metadata or data).</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.ResultType]
Parameter Sets: GetWithFullParameters
Aliases:
Accepted values: Data, Metadata

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-142">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="f774f-142">-StartTime</span></span>
<span data-ttu-id="f774f-143">Sorgunun başlangıç saatini yerel saatte belirtir.</span><span class="sxs-lookup"><span data-stu-id="f774f-143">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="f774f-144">Varsayılan, geçerli yerel saatin bir saattir.</span><span class="sxs-lookup"><span data-stu-id="f774f-144">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-145">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="f774f-145">-TimeGrain</span></span>
<span data-ttu-id="f774f-146">Ölçü süresinin ss: DD: ss biçiminde bir **TimeSpan** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f774f-146">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-147">-Üst</span><span class="sxs-lookup"><span data-stu-id="f774f-147">-Top</span></span>
<span data-ttu-id="f774f-148">$Filter ile belirtiye alınacak en fazla kayıt sayısını (varsayılan: 10) belirtir.</span><span class="sxs-lookup"><span data-stu-id="f774f-148">Specifies the maximum number of records to retrieve (default:10), to be specified with $filter.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetWithFullParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f774f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f774f-149">CommonParameters</span></span>
<span data-ttu-id="f774f-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f774f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f774f-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f774f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f774f-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f774f-152">INPUTS</span></span>

### <span data-ttu-id="f774f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f774f-153">System.String</span></span>

### <span data-ttu-id="f774f-154">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="f774f-154">System.TimeSpan</span></span>

### <span data-ttu-id="f774f-155">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. modeller. AggregationType, Microsoft. Azure. Management. Monitor, Version = 0.19.1.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f774f-155">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.AggregationType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f774f-156">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="f774f-156">System.DateTime</span></span>

### <span data-ttu-id="f774f-157">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f774f-157">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f774f-158">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. modeller. ResultType, Microsoft. Azure. Management. Monitor, Version = 0.19.1.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f774f-158">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Models.ResultType, Microsoft.Azure.Management.Monitor, Version=0.19.1.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f774f-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="f774f-159">System.String[]</span></span>

### <span data-ttu-id="f774f-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f774f-160">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f774f-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f774f-161">OUTPUTS</span></span>

### <span data-ttu-id="f774f-162">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric</span><span class="sxs-lookup"><span data-stu-id="f774f-162">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric</span></span>

## <span data-ttu-id="f774f-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f774f-163">NOTES</span></span>

## <span data-ttu-id="f774f-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f774f-164">RELATED LINKS</span></span>

<span data-ttu-id="f774f-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md) 
 [Yeni-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="f774f-165">[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)
[New-AzureRmMetricFilter](./New-AzureRmMetricFilter.md)</span></span>

