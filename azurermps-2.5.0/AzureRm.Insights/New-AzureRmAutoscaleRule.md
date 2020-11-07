---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
ms.openlocfilehash: 785424560ebd0af3ce7035265e9fb64b22713049
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939387"
---
# <span data-ttu-id="1faf4-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="1faf4-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="1faf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1faf4-102">SYNOPSIS</span></span>
<span data-ttu-id="1faf4-103">Otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1faf4-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1faf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1faf4-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1faf4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1faf4-105">DESCRIPTION</span></span>
<span data-ttu-id="1faf4-106">**Yeni-AzureRmAutoscaleRule** cmdlet 'ı otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1faf4-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="1faf4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1faf4-107">EXAMPLES</span></span>

### <span data-ttu-id="1faf4-108">Örnek 1: kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="1faf4-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="1faf4-109">Bu komut bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1faf4-109">This command creates a rule.</span></span>

### <span data-ttu-id="1faf4-110">Örnek 2: iki kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="1faf4-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="1faf4-111">İlk komut Istekler için bir kural oluşturur ve sonra bunu $Rule 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1faf4-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="1faf4-112">İkinci komut Istekler için ikinci bir kural oluşturur ve ardından $Rule 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1faf4-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="1faf4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1faf4-113">PARAMETERS</span></span>

### <span data-ttu-id="1faf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1faf4-114">-DefaultProfile</span></span>
<span data-ttu-id="1faf4-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1faf4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1faf4-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="1faf4-116">-MetricName</span></span>
<span data-ttu-id="1faf4-117">Ölçümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="1faf4-118">-Metricresourceıd</span><span class="sxs-lookup"><span data-stu-id="1faf4-118">-MetricResourceId</span></span>
<span data-ttu-id="1faf4-119">Ölçüm kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="1faf4-120">-Metricistatistiğini</span><span class="sxs-lookup"><span data-stu-id="1faf4-120">-MetricStatistic</span></span>
<span data-ttu-id="1faf4-121">Ölçüm istatistiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="1faf4-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1faf4-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1faf4-123">Geçen</span><span class="sxs-lookup"><span data-stu-id="1faf4-123">Average</span></span>
- <span data-ttu-id="1faf4-124">Enaz</span><span class="sxs-lookup"><span data-stu-id="1faf4-124">Min</span></span>
- <span data-ttu-id="1faf4-125">Biçimlendir</span><span class="sxs-lookup"><span data-stu-id="1faf4-125">Max</span></span>
- <span data-ttu-id="1faf4-126">Harfi</span><span class="sxs-lookup"><span data-stu-id="1faf4-126">Sum</span></span>

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

### <span data-ttu-id="1faf4-127">-İşleç</span><span class="sxs-lookup"><span data-stu-id="1faf4-127">-Operator</span></span>
<span data-ttu-id="1faf4-128">İşleci belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-128">Specifies the operator.</span></span>
<span data-ttu-id="1faf4-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1faf4-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1faf4-130">Ken</span><span class="sxs-lookup"><span data-stu-id="1faf4-130">Equals</span></span>
- <span data-ttu-id="1faf4-131">Notals</span><span class="sxs-lookup"><span data-stu-id="1faf4-131">NotEquals</span></span>
- <span data-ttu-id="1faf4-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="1faf4-132">GreaterThan</span></span>
- <span data-ttu-id="1faf4-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="1faf4-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="1faf4-134">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="1faf4-134">LessThan</span></span>
- <span data-ttu-id="1faf4-135">Gezi Bayramı</span><span class="sxs-lookup"><span data-stu-id="1faf4-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="1faf4-136">-Scaleactioncoolaşağı</span><span class="sxs-lookup"><span data-stu-id="1faf4-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="1faf4-137">Coolıyuvarla eylemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="1faf4-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="1faf4-138">-ScaleActionDirection</span></span>
<span data-ttu-id="1faf4-139">Ölçek eyleminin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="1faf4-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1faf4-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1faf4-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1faf4-141">None</span></span>
- <span data-ttu-id="1faf4-142">Artırmak</span><span class="sxs-lookup"><span data-stu-id="1faf4-142">Increase</span></span>
- <span data-ttu-id="1faf4-143">Azalt</span><span class="sxs-lookup"><span data-stu-id="1faf4-143">Decrease</span></span>

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

### <span data-ttu-id="1faf4-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="1faf4-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="1faf4-145">Ölçek türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-145">Specifies the scale type.</span></span>
<span data-ttu-id="1faf4-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1faf4-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1faf4-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="1faf4-147">ChangeSize</span></span>
- <span data-ttu-id="1faf4-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="1faf4-148">ChangeCount</span></span>
- <span data-ttu-id="1faf4-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="1faf4-149">PercentChangeCount</span></span>
- <span data-ttu-id="1faf4-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="1faf4-150">ExactCount</span></span>

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

### <span data-ttu-id="1faf4-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="1faf4-151">-ScaleActionValue</span></span>
<span data-ttu-id="1faf4-152">Eylem değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="1faf4-153">Eşiği</span><span class="sxs-lookup"><span data-stu-id="1faf4-153">-Threshold</span></span>
<span data-ttu-id="1faf4-154">Ölçüm değerinin eşiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="1faf4-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="1faf4-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="1faf4-156">Zaman toplama işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="1faf4-157">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1faf4-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1faf4-158">Geçen</span><span class="sxs-lookup"><span data-stu-id="1faf4-158">Average</span></span>
- <span data-ttu-id="1faf4-159">Gerekliliktir</span><span class="sxs-lookup"><span data-stu-id="1faf4-159">Minimum</span></span>
- <span data-ttu-id="1faf4-160">Sayısını</span><span class="sxs-lookup"><span data-stu-id="1faf4-160">Maximum</span></span>
- <span data-ttu-id="1faf4-161">Soya</span><span class="sxs-lookup"><span data-stu-id="1faf4-161">Last</span></span>
- <span data-ttu-id="1faf4-162">Toplam, say</span><span class="sxs-lookup"><span data-stu-id="1faf4-162">Total, Count</span></span>

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

### <span data-ttu-id="1faf4-163">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="1faf4-163">-TimeGrain</span></span>
<span data-ttu-id="1faf4-164">Zaman gösterimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="1faf4-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="1faf4-165">-TimeWindow</span></span>
<span data-ttu-id="1faf4-166">Zaman penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1faf4-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="1faf4-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1faf4-167">CommonParameters</span></span>
<span data-ttu-id="1faf4-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1faf4-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1faf4-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1faf4-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1faf4-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1faf4-170">INPUTS</span></span>

### <span data-ttu-id="1faf4-171">System. String</span><span class="sxs-lookup"><span data-stu-id="1faf4-171">System.String</span></span>

### <span data-ttu-id="1faf4-172">Microsoft. Azure. Management. Monitor. Management. modeller. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="1faf4-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="1faf4-173">Microsoft. Azure. Management. Monitor. Management. modeller. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="1faf4-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="1faf4-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="1faf4-174">System.Double</span></span>

### <span data-ttu-id="1faf4-175">Microsoft. Azure. Management. Monitor. Management. modeller. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="1faf4-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="1faf4-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="1faf4-176">System.TimeSpan</span></span>

### <span data-ttu-id="1faf4-177">Microsoft. Azure. Management. Monitor. Management. modeller. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="1faf4-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="1faf4-178">Microsoft. Azure. Management. Monitor. Management. modeller. ScaleType</span><span class="sxs-lookup"><span data-stu-id="1faf4-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="1faf4-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1faf4-179">OUTPUTS</span></span>

### <span data-ttu-id="1faf4-180">Microsoft. Azure. Management. Monitor. Management. modeller. Salerule</span><span class="sxs-lookup"><span data-stu-id="1faf4-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="1faf4-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1faf4-181">NOTES</span></span>

## <span data-ttu-id="1faf4-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1faf4-182">RELATED LINKS</span></span>

[<span data-ttu-id="1faf4-183">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1faf4-183">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1faf4-184">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="1faf4-184">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="1faf4-185">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1faf4-185">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1faf4-186">Yeni-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="1faf4-186">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="1faf4-187">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1faf4-187">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


