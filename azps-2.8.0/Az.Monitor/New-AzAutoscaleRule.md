---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cc3899555f5039b2ae3d53d7fbc3d50fa2bda892
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931865"
---
# <span data-ttu-id="69023-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="69023-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="69023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69023-102">SYNOPSIS</span></span>
<span data-ttu-id="69023-103">Otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69023-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="69023-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69023-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69023-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69023-105">DESCRIPTION</span></span>
<span data-ttu-id="69023-106">**Yeni-AzAutoscaleRule** cmdlet 'ı bir otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69023-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="69023-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69023-107">EXAMPLES</span></span>

### <span data-ttu-id="69023-108">Örnek 1: kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="69023-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="69023-109">Bu komut bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69023-109">This command creates a rule.</span></span>

### <span data-ttu-id="69023-110">Örnek 2: iki kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="69023-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="69023-111">İlk komut Istekler için bir kural oluşturur ve sonra bunu $Rule 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="69023-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="69023-112">İkinci komut Istekler için ikinci bir kural oluşturur ve ardından $Rule 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="69023-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="69023-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69023-113">PARAMETERS</span></span>

### <span data-ttu-id="69023-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69023-114">-DefaultProfile</span></span>
<span data-ttu-id="69023-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="69023-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69023-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="69023-116">-MetricName</span></span>
<span data-ttu-id="69023-117">Ölçümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-117">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="69023-118">-Metricresourceıd</span><span class="sxs-lookup"><span data-stu-id="69023-118">-MetricResourceId</span></span>
<span data-ttu-id="69023-119">Ölçüm kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-119">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="69023-120">-Metricistatistiğini</span><span class="sxs-lookup"><span data-stu-id="69023-120">-MetricStatistic</span></span>
<span data-ttu-id="69023-121">Ölçüm istatistiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="69023-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="69023-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69023-123">Geçen</span><span class="sxs-lookup"><span data-stu-id="69023-123">Average</span></span>
- <span data-ttu-id="69023-124">Enaz</span><span class="sxs-lookup"><span data-stu-id="69023-124">Min</span></span>
- <span data-ttu-id="69023-125">Biçimlendir</span><span class="sxs-lookup"><span data-stu-id="69023-125">Max</span></span>
- <span data-ttu-id="69023-126">Harfi</span><span class="sxs-lookup"><span data-stu-id="69023-126">Sum</span></span>

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

### <span data-ttu-id="69023-127">-İşleç</span><span class="sxs-lookup"><span data-stu-id="69023-127">-Operator</span></span>
<span data-ttu-id="69023-128">İşleci belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-128">Specifies the operator.</span></span>
<span data-ttu-id="69023-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="69023-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69023-130">Ken</span><span class="sxs-lookup"><span data-stu-id="69023-130">Equals</span></span>
- <span data-ttu-id="69023-131">Notals</span><span class="sxs-lookup"><span data-stu-id="69023-131">NotEquals</span></span>
- <span data-ttu-id="69023-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="69023-132">GreaterThan</span></span>
- <span data-ttu-id="69023-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="69023-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="69023-134">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="69023-134">LessThan</span></span>
- <span data-ttu-id="69023-135">Gezi Bayramı</span><span class="sxs-lookup"><span data-stu-id="69023-135">LessThanOrEqual</span></span>

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

### <span data-ttu-id="69023-136">-Scaleactioncoolaşağı</span><span class="sxs-lookup"><span data-stu-id="69023-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="69023-137">Coolıyuvarla eylemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-137">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="69023-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="69023-138">-ScaleActionDirection</span></span>
<span data-ttu-id="69023-139">Ölçek eyleminin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="69023-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="69023-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69023-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="69023-141">None</span></span>
- <span data-ttu-id="69023-142">Artırmak</span><span class="sxs-lookup"><span data-stu-id="69023-142">Increase</span></span>
- <span data-ttu-id="69023-143">Azalt</span><span class="sxs-lookup"><span data-stu-id="69023-143">Decrease</span></span>

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

### <span data-ttu-id="69023-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="69023-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="69023-145">Ölçek türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-145">Specifies the scale type.</span></span>
<span data-ttu-id="69023-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="69023-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69023-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="69023-147">ChangeSize</span></span>
- <span data-ttu-id="69023-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="69023-148">ChangeCount</span></span>
- <span data-ttu-id="69023-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="69023-149">PercentChangeCount</span></span>
- <span data-ttu-id="69023-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="69023-150">ExactCount</span></span>

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

### <span data-ttu-id="69023-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="69023-151">-ScaleActionValue</span></span>
<span data-ttu-id="69023-152">Eylem değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-152">Specifies the action value.</span></span>

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

### <span data-ttu-id="69023-153">Eşiği</span><span class="sxs-lookup"><span data-stu-id="69023-153">-Threshold</span></span>
<span data-ttu-id="69023-154">Ölçüm değerinin eşiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-154">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="69023-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="69023-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="69023-156">Zaman toplama işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="69023-157">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="69023-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69023-158">Geçen</span><span class="sxs-lookup"><span data-stu-id="69023-158">Average</span></span>
- <span data-ttu-id="69023-159">Gerekliliktir</span><span class="sxs-lookup"><span data-stu-id="69023-159">Minimum</span></span>
- <span data-ttu-id="69023-160">Sayısını</span><span class="sxs-lookup"><span data-stu-id="69023-160">Maximum</span></span>
- <span data-ttu-id="69023-161">Soya</span><span class="sxs-lookup"><span data-stu-id="69023-161">Last</span></span>
- <span data-ttu-id="69023-162">Toplam, say</span><span class="sxs-lookup"><span data-stu-id="69023-162">Total, Count</span></span>

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

### <span data-ttu-id="69023-163">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="69023-163">-TimeGrain</span></span>
<span data-ttu-id="69023-164">Zaman gösterimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-164">Specifies the time grain.</span></span>

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

### <span data-ttu-id="69023-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="69023-165">-TimeWindow</span></span>
<span data-ttu-id="69023-166">Zaman penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="69023-166">Specifies the time window.</span></span>

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

### <span data-ttu-id="69023-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69023-167">CommonParameters</span></span>
<span data-ttu-id="69023-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69023-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69023-169">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69023-169">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69023-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69023-170">INPUTS</span></span>

### <span data-ttu-id="69023-171">System. String</span><span class="sxs-lookup"><span data-stu-id="69023-171">System.String</span></span>

### <span data-ttu-id="69023-172">Microsoft. Azure. Management. Monitor. Management. modeller. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="69023-172">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="69023-173">Microsoft. Azure. Management. Monitor. Management. modeller. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="69023-173">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="69023-174">System. Double</span><span class="sxs-lookup"><span data-stu-id="69023-174">System.Double</span></span>

### <span data-ttu-id="69023-175">Microsoft. Azure. Management. Monitor. Management. modeller. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="69023-175">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="69023-176">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="69023-176">System.TimeSpan</span></span>

### <span data-ttu-id="69023-177">Microsoft. Azure. Management. Monitor. Management. modeller. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="69023-177">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="69023-178">Microsoft. Azure. Management. Monitor. Management. modeller. ScaleType</span><span class="sxs-lookup"><span data-stu-id="69023-178">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="69023-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69023-179">OUTPUTS</span></span>

### <span data-ttu-id="69023-180">Microsoft. Azure. Management. Monitor. Management. modeller. Salerule</span><span class="sxs-lookup"><span data-stu-id="69023-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="69023-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69023-181">NOTES</span></span>

## <span data-ttu-id="69023-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69023-182">RELATED LINKS</span></span>

[<span data-ttu-id="69023-183">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="69023-183">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="69023-184">Get-Azotomatik ölçek geçmişi</span><span class="sxs-lookup"><span data-stu-id="69023-184">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="69023-185">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="69023-185">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="69023-186">Yeni-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="69023-186">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="69023-187">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="69023-187">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


