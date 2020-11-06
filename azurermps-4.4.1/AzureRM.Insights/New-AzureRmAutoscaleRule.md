---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: e6f157e199dedf6a7587f607cdd275183ec67c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594272"
---
# <span data-ttu-id="8e7fe-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="8e7fe-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="8e7fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7fe-103">Otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e7fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e7fe-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e7fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e7fe-105">DESCRIPTION</span></span>
<span data-ttu-id="8e7fe-106">**Yeni-AzureRmAutoscaleRule** cmdlet 'ı otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="8e7fe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e7fe-107">EXAMPLES</span></span>

### <span data-ttu-id="8e7fe-108">Örnek 1: kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="8e7fe-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="8e7fe-109">Bu komut bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-109">This command creates a rule.</span></span>

### <span data-ttu-id="8e7fe-110">Örnek 2: iki kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="8e7fe-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="8e7fe-111">İlk komut Istekler için bir kural oluşturur ve sonra bunu $Rule 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="8e7fe-112">İkinci komut Istekler için ikinci bir kural oluşturur ve ardından $Rule 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="8e7fe-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e7fe-113">PARAMETERS</span></span>

### <span data-ttu-id="8e7fe-114">-MetricName</span><span class="sxs-lookup"><span data-stu-id="8e7fe-114">-MetricName</span></span>
<span data-ttu-id="8e7fe-115">Ölçümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-115">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-116">-Metricresourceıd</span><span class="sxs-lookup"><span data-stu-id="8e7fe-116">-MetricResourceId</span></span>
<span data-ttu-id="8e7fe-117">Ölçüm kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-117">Specifies the metric resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-118">-Metricistatistiğini</span><span class="sxs-lookup"><span data-stu-id="8e7fe-118">-MetricStatistic</span></span>
<span data-ttu-id="8e7fe-119">Ölçüm istatistiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-119">Specifies the metric statistic.</span></span>
<span data-ttu-id="8e7fe-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8e7fe-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e7fe-121">Geçen</span><span class="sxs-lookup"><span data-stu-id="8e7fe-121">Average</span></span>
- <span data-ttu-id="8e7fe-122">Enaz</span><span class="sxs-lookup"><span data-stu-id="8e7fe-122">Min</span></span>
- <span data-ttu-id="8e7fe-123">Biçimlendir</span><span class="sxs-lookup"><span data-stu-id="8e7fe-123">Max</span></span>
- <span data-ttu-id="8e7fe-124">Harfi</span><span class="sxs-lookup"><span data-stu-id="8e7fe-124">Sum</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-125">-İşleç</span><span class="sxs-lookup"><span data-stu-id="8e7fe-125">-Operator</span></span>
<span data-ttu-id="8e7fe-126">İşleci belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-126">Specifies the operator.</span></span>
<span data-ttu-id="8e7fe-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8e7fe-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e7fe-128">Ken</span><span class="sxs-lookup"><span data-stu-id="8e7fe-128">Equals</span></span>
- <span data-ttu-id="8e7fe-129">Notals</span><span class="sxs-lookup"><span data-stu-id="8e7fe-129">NotEquals</span></span>
- <span data-ttu-id="8e7fe-130">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="8e7fe-130">GreaterThan</span></span>
- <span data-ttu-id="8e7fe-131">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="8e7fe-131">GreaterThanOrEqual</span></span>
- <span data-ttu-id="8e7fe-132">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="8e7fe-132">LessThan</span></span>
- <span data-ttu-id="8e7fe-133">Gezi Bayramı</span><span class="sxs-lookup"><span data-stu-id="8e7fe-133">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-134">-Scaleactioncoolaşağı</span><span class="sxs-lookup"><span data-stu-id="8e7fe-134">-ScaleActionCooldown</span></span>
<span data-ttu-id="8e7fe-135">Coolıyuvarla eylemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-135">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-136">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="8e7fe-136">-ScaleActionDirection</span></span>
<span data-ttu-id="8e7fe-137">Ölçek eyleminin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-137">Specifies the scale action direction.</span></span>
<span data-ttu-id="8e7fe-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8e7fe-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e7fe-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8e7fe-139">None</span></span>
- <span data-ttu-id="8e7fe-140">Artırmak</span><span class="sxs-lookup"><span data-stu-id="8e7fe-140">Increase</span></span>
- <span data-ttu-id="8e7fe-141">Azalt</span><span class="sxs-lookup"><span data-stu-id="8e7fe-141">Decrease</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-142">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="8e7fe-142">-ScaleActionScaleType</span></span>
<span data-ttu-id="8e7fe-143">Ölçek türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-143">Specifies the scale type.</span></span>
<span data-ttu-id="8e7fe-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8e7fe-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e7fe-145">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="8e7fe-145">ChangeSize</span></span>
- <span data-ttu-id="8e7fe-146">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="8e7fe-146">ChangeCount</span></span>
- <span data-ttu-id="8e7fe-147">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="8e7fe-147">PercentChangeCount</span></span>
- <span data-ttu-id="8e7fe-148">ExactCount</span><span class="sxs-lookup"><span data-stu-id="8e7fe-148">ExactCount</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-149">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="8e7fe-149">-ScaleActionValue</span></span>
<span data-ttu-id="8e7fe-150">Eylem değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-150">Specifies the action value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-151">Eşiği</span><span class="sxs-lookup"><span data-stu-id="8e7fe-151">-Threshold</span></span>
<span data-ttu-id="8e7fe-152">Ölçüm değerinin eşiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-152">Specifies the threshold of the metric value.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-153">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="8e7fe-153">-TimeAggregationOperator</span></span>
<span data-ttu-id="8e7fe-154">Zaman toplama işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-154">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="8e7fe-155">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8e7fe-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8e7fe-156">Geçen</span><span class="sxs-lookup"><span data-stu-id="8e7fe-156">Average</span></span>
- <span data-ttu-id="8e7fe-157">Gerekliliktir</span><span class="sxs-lookup"><span data-stu-id="8e7fe-157">Minimum</span></span>
- <span data-ttu-id="8e7fe-158">Sayısını</span><span class="sxs-lookup"><span data-stu-id="8e7fe-158">Maximum</span></span>
- <span data-ttu-id="8e7fe-159">Soya</span><span class="sxs-lookup"><span data-stu-id="8e7fe-159">Last</span></span>
- <span data-ttu-id="8e7fe-160">Toplam, say</span><span class="sxs-lookup"><span data-stu-id="8e7fe-160">Total, Count</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-161">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="8e7fe-161">-TimeGrain</span></span>
<span data-ttu-id="8e7fe-162">Zaman gösterimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-162">Specifies the time grain.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e7fe-163">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="8e7fe-163">-TimeWindow</span></span>
<span data-ttu-id="8e7fe-164">Zaman penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-164">Specifies the time window.</span></span>

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

### <span data-ttu-id="8e7fe-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7fe-165">-DefaultProfile</span></span>
<span data-ttu-id="8e7fe-166">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e7fe-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7fe-167">CommonParameters</span></span>
<span data-ttu-id="8e7fe-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e7fe-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7fe-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e7fe-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7fe-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e7fe-170">INPUTS</span></span>

## <span data-ttu-id="8e7fe-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e7fe-171">OUTPUTS</span></span>

### <span data-ttu-id="8e7fe-172">Microsoft. Azure. Management. Monitor. Management. modeller. Salerule</span><span class="sxs-lookup"><span data-stu-id="8e7fe-172">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="8e7fe-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e7fe-173">NOTES</span></span>

## <span data-ttu-id="8e7fe-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e7fe-174">RELATED LINKS</span></span>

[<span data-ttu-id="8e7fe-175">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8e7fe-175">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="8e7fe-176">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="8e7fe-176">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="8e7fe-177">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8e7fe-177">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="8e7fe-178">Yeni-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="8e7fe-178">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="8e7fe-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8e7fe-179">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


