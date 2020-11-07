---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: 63ade199b63e57cc72e965002942773f47214494
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762264"
---
# <span data-ttu-id="9f765-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="9f765-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="9f765-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f765-102">SYNOPSIS</span></span>
<span data-ttu-id="9f765-103">Kaynağın metrik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9f765-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f765-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f765-104">SYNTAX</span></span>

### <span data-ttu-id="9f765-105">GetWithDefaultParameters</span><span class="sxs-lookup"><span data-stu-id="9f765-105">GetWithDefaultParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [[-MetricName] <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f765-106">GetWithFullParameters</span><span class="sxs-lookup"><span data-stu-id="9f765-106">GetWithFullParameters</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-TimeGrain <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-MetricName] <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f765-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f765-107">DESCRIPTION</span></span>
<span data-ttu-id="9f765-108">**Get-AzureRmMetric** cmdlet 'i, belirli bir kaynağın ölçüm değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9f765-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="9f765-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f765-109">EXAMPLES</span></span>

### <span data-ttu-id="9f765-110">Örnek 1: özetlenmiş çıkış içeren bir metrik alma</span><span class="sxs-lookup"><span data-stu-id="9f765-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="9f765-111">Bu komut, zaman çizgisi 1 dakikalık bir WebSite3 için ölçüm değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9f765-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="9f765-112">Örnek 2: ayrıntılı çıktı içeren bir metrik alın</span><span class="sxs-lookup"><span data-stu-id="9f765-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="9f765-113">Bu komut, zaman çizgisi 1 dakikalık bir WebSite3 için ölçüm değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9f765-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="9f765-114">Çıktı</span><span class="sxs-lookup"><span data-stu-id="9f765-114">The output is detailed.</span></span>

### <span data-ttu-id="9f765-115">Örnek 3: belirli bir metrik için ayrıntılı çıktı alma</span><span class="sxs-lookup"><span data-stu-id="9f765-115">Example 3: Get detailed output for a specified metric</span></span>
```
PS C:\>Get-AzureRmMetric -ResourceId "/subscriptions/e3f5b07d-3c39-4b0f-bf3b-40fdeba10f2a/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website3" -TimeGrain 00:01:00 -DetailedOutput -MetricNames "Requests"
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

<span data-ttu-id="9f765-116">Bu komut, Istekler için ayrıntılı çıktı alır.</span><span class="sxs-lookup"><span data-stu-id="9f765-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="9f765-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f765-117">PARAMETERS</span></span>

### <span data-ttu-id="9f765-118">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="9f765-118">-AggregationType</span></span>
<span data-ttu-id="9f765-119">Sorgunun toplama türü</span><span class="sxs-lookup"><span data-stu-id="9f765-119">The aggregation type of the query</span></span>

```yaml
Type: AggregationType
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f765-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f765-120">-DefaultProfile</span></span>
<span data-ttu-id="9f765-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f765-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f765-122">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="9f765-122">-DetailedOutput</span></span>
<span data-ttu-id="9f765-123">Bu cmdlet 'in ayrıntılı çıkış görüntüleyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f765-123">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="9f765-124">Varsayılan olarak, çıktı özetlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="9f765-124">By default, output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f765-125">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="9f765-125">-EndTime</span></span>
<span data-ttu-id="9f765-126">Yerel saatte sorgunun bitiş saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f765-126">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="9f765-127">Varsayılan geçerli saat.</span><span class="sxs-lookup"><span data-stu-id="9f765-127">The default is the current time.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f765-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9f765-128">-MetricName</span></span>
<span data-ttu-id="9f765-129">Ölçüm adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f765-129">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False (GetWithDefaultParameters), True (GetAzureRmAMetricFullParamGroup)
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: GetWithFullParameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f765-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9f765-130">-ResourceId</span></span>
<span data-ttu-id="9f765-131">Ölçümün kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f765-131">Specifies the resource ID of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f765-132">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="9f765-132">-StartTime</span></span>
<span data-ttu-id="9f765-133">Sorgunun başlangıç saatini yerel saatte belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f765-133">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="9f765-134">Varsayılan, geçerli yerel saatin bir saattir.</span><span class="sxs-lookup"><span data-stu-id="9f765-134">The default is the current local time minus one hour.</span></span>

```yaml
Type: DateTime
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f765-135">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="9f765-135">-TimeGrain</span></span>
<span data-ttu-id="9f765-136">Ölçü süresinin ss: DD: ss biçiminde bir **TimeSpan** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f765-136">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: GetWithFullParameters
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f765-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f765-137">CommonParameters</span></span>
<span data-ttu-id="9f765-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f765-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f765-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f765-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f765-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f765-140">INPUTS</span></span>

### <span data-ttu-id="9f765-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9f765-141">None</span></span>
<span data-ttu-id="9f765-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9f765-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f765-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f765-143">OUTPUTS</span></span>

### <span data-ttu-id="9f765-144">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="9f765-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="9f765-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f765-145">NOTES</span></span>

## <span data-ttu-id="9f765-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f765-146">RELATED LINKS</span></span>

[<span data-ttu-id="9f765-147">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="9f765-147">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


