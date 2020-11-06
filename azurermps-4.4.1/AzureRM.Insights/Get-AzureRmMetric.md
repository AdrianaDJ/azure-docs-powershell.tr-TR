---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: EAFB9C98-000C-4EAC-A32D-6B0F1939AA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetric.md
ms.openlocfilehash: d8b7c83ff2804de3e60af7c5ea8ce9f3e2d1eb97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593128"
---
# <span data-ttu-id="1206d-101">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="1206d-101">Get-AzureRmMetric</span></span>

## <span data-ttu-id="1206d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1206d-102">SYNOPSIS</span></span>
<span data-ttu-id="1206d-103">Kaynağın metrik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="1206d-103">Gets the metric values of a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1206d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1206d-104">SYNTAX</span></span>

### <span data-ttu-id="1206d-105">Varsayılan modda Get-AzureRmMetric cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="1206d-105">Parameters for Get-AzureRmMetric cmdlet in the default mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1206d-106">Tam parametre kümesi modunda Get-AzureRmMetric cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="1206d-106">Parameters for Get-AzureRmMetric cmdlet in the full param set mode</span></span>
```
Get-AzureRmMetric [-ResourceId] <String> [[-TimeGrain] <TimeSpan>] [-AggregationType <AggregationType>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] -MetricNames <String[]> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1206d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1206d-107">DESCRIPTION</span></span>
<span data-ttu-id="1206d-108">**Get-AzureRmMetric** cmdlet 'i, belirli bir kaynağın ölçüm değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="1206d-108">The **Get-AzureRmMetric** cmdlet gets the metric values for a specified resource.</span></span>

## <span data-ttu-id="1206d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1206d-109">EXAMPLES</span></span>

### <span data-ttu-id="1206d-110">Örnek 1: özetlenmiş çıkış içeren bir metrik alma</span><span class="sxs-lookup"><span data-stu-id="1206d-110">Example 1: Get a metric with summarized output</span></span>
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

<span data-ttu-id="1206d-111">Bu komut, zaman çizgisi 1 dakikalık bir WebSite3 için ölçüm değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="1206d-111">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>

### <span data-ttu-id="1206d-112">Örnek 2: ayrıntılı çıktı içeren bir metrik alın</span><span class="sxs-lookup"><span data-stu-id="1206d-112">Example 2: Get a metric with detailed output</span></span>
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

<span data-ttu-id="1206d-113">Bu komut, zaman çizgisi 1 dakikalık bir WebSite3 için ölçüm değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="1206d-113">This command gets the metric values for website3 with a time grain of 1 minute.</span></span>
<span data-ttu-id="1206d-114">Çıktı</span><span class="sxs-lookup"><span data-stu-id="1206d-114">The output is detailed.</span></span>

### <span data-ttu-id="1206d-115">Örnek 3: belirli bir metrik için ayrıntılı çıktı alma</span><span class="sxs-lookup"><span data-stu-id="1206d-115">Example 3: Get detailed output for a specified metric</span></span>
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

<span data-ttu-id="1206d-116">Bu komut, Istekler için ayrıntılı çıktı alır.</span><span class="sxs-lookup"><span data-stu-id="1206d-116">This command gets detailed output for the Requests metric.</span></span>

## <span data-ttu-id="1206d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1206d-117">PARAMETERS</span></span>

### <span data-ttu-id="1206d-118">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="1206d-118">-DetailedOutput</span></span>
<span data-ttu-id="1206d-119">Bu cmdlet 'in ayrıntılı çıkış görüntüleyeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1206d-119">Indicates that this cmdlet displays detailed output.</span></span>
<span data-ttu-id="1206d-120">Varsayılan olarak, çıktı özetlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="1206d-120">By default, output is summarized.</span></span>

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

### <span data-ttu-id="1206d-121">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="1206d-121">-EndTime</span></span>
<span data-ttu-id="1206d-122">Yerel saatte sorgunun bitiş saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1206d-122">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="1206d-123">Varsayılan geçerli saat.</span><span class="sxs-lookup"><span data-stu-id="1206d-123">The default is the current time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1206d-124">-Metrik adları</span><span class="sxs-lookup"><span data-stu-id="1206d-124">-MetricNames</span></span>
<span data-ttu-id="1206d-125">Ölçüm adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1206d-125">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the default mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1206d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1206d-126">-ResourceId</span></span>
<span data-ttu-id="1206d-127">Ölçümün kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1206d-127">Specifies the resource ID of the metric.</span></span>

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

### <span data-ttu-id="1206d-128">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="1206d-128">-StartTime</span></span>
<span data-ttu-id="1206d-129">Sorgunun başlangıç saatini yerel saatte belirtir.</span><span class="sxs-lookup"><span data-stu-id="1206d-129">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="1206d-130">Varsayılan, geçerli yerel saatin bir saattir.</span><span class="sxs-lookup"><span data-stu-id="1206d-130">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1206d-131">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="1206d-131">-TimeGrain</span></span>
<span data-ttu-id="1206d-132">Ölçü süresinin ss: DD: ss biçiminde bir **TimeSpan** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1206d-132">Specifies the time grain of the metric as a **TimeSpan** object in the format hh:mm:ss.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1206d-133">-AggregationType</span><span class="sxs-lookup"><span data-stu-id="1206d-133">-AggregationType</span></span>
<span data-ttu-id="1206d-134">En iyi yol türü</span><span class="sxs-lookup"><span data-stu-id="1206d-134">The aggregation type of the quer</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Models.AggregationType]
Parameter Sets: Parameters for Get-AzureRmMetric cmdlet in the full param set mode
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1206d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1206d-135">-DefaultProfile</span></span>
<span data-ttu-id="1206d-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1206d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1206d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1206d-137">CommonParameters</span></span>
<span data-ttu-id="1206d-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1206d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1206d-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1206d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1206d-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1206d-140">INPUTS</span></span>

## <span data-ttu-id="1206d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1206d-141">OUTPUTS</span></span>

### <span data-ttu-id="1206d-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetric []</span><span class="sxs-lookup"><span data-stu-id="1206d-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetric[]</span></span>

## <span data-ttu-id="1206d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1206d-143">NOTES</span></span>

## <span data-ttu-id="1206d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1206d-144">RELATED LINKS</span></span>

[<span data-ttu-id="1206d-145">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="1206d-145">Get-AzureRmMetricDefinition</span></span>](./Get-AzureRmMetricDefinition.md)


