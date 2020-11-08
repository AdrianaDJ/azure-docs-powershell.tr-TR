---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleRule.md
ms.openlocfilehash: cd4e374909fa58f036a0f67cd7a89bb968defd71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274431"
---
# <span data-ttu-id="957a2-101">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="957a2-101">New-AzAutoscaleRule</span></span>

## <span data-ttu-id="957a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="957a2-102">SYNOPSIS</span></span>
<span data-ttu-id="957a2-103">Otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="957a2-103">Creates an Autoscale rule.</span></span>

## <span data-ttu-id="957a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="957a2-104">SYNTAX</span></span>

```
New-AzAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="957a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="957a2-105">DESCRIPTION</span></span>
<span data-ttu-id="957a2-106">**Yeni-AzAutoscaleRule** cmdlet 'ı bir otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="957a2-106">The **New-AzAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="957a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="957a2-107">EXAMPLES</span></span>

### <span data-ttu-id="957a2-108">Örnek 1: kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="957a2-108">Example 1: Create a rule</span></span>
```powershell
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="957a2-109">Bu komut bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="957a2-109">This command creates a rule.</span></span>

### <span data-ttu-id="957a2-110">Örnek 2: iki kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="957a2-110">Example 2: Create two rules</span></span>
```powershell
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="957a2-111">İlk komut Istekler için bir kural oluşturur ve sonra bunu $Rule 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="957a2-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>
<span data-ttu-id="957a2-112">İkinci komut Istekler için ikinci bir kural oluşturur ve ardından $Rule 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="957a2-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

### <span data-ttu-id="957a2-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="957a2-113">Example 3</span></span>

<span data-ttu-id="957a2-114">Otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="957a2-114">Creates an Autoscale rule.</span></span> <span data-ttu-id="957a2-115">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="957a2-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzAutoscaleRule -MetricName 'Requests' -MetricResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite' -MetricStatistic Average -Operator Equals -ScaleActionCooldown 00:05:00 -ScaleActionDirection None -ScaleActionScaleType ChangeCount -ScaleActionValue '1' -Threshold 10 -TimeGrain 00:01:00 -TimeWindow <TimeSpan>
```

## <span data-ttu-id="957a2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="957a2-116">PARAMETERS</span></span>

### <span data-ttu-id="957a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="957a2-117">-DefaultProfile</span></span>
<span data-ttu-id="957a2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="957a2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="957a2-119">-MetricName</span><span class="sxs-lookup"><span data-stu-id="957a2-119">-MetricName</span></span>
<span data-ttu-id="957a2-120">Ölçümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-120">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="957a2-121">-Metricresourceıd</span><span class="sxs-lookup"><span data-stu-id="957a2-121">-MetricResourceId</span></span>
<span data-ttu-id="957a2-122">Ölçüm kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-122">Specifies the metric resource ID.</span></span>

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

### <span data-ttu-id="957a2-123">-Metricistatistiğini</span><span class="sxs-lookup"><span data-stu-id="957a2-123">-MetricStatistic</span></span>
<span data-ttu-id="957a2-124">Ölçüm istatistiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-124">Specifies the metric statistic.</span></span>
<span data-ttu-id="957a2-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="957a2-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="957a2-126">Geçen</span><span class="sxs-lookup"><span data-stu-id="957a2-126">Average</span></span>
- <span data-ttu-id="957a2-127">Enaz</span><span class="sxs-lookup"><span data-stu-id="957a2-127">Min</span></span>
- <span data-ttu-id="957a2-128">Biçimlendir</span><span class="sxs-lookup"><span data-stu-id="957a2-128">Max</span></span>
- <span data-ttu-id="957a2-129">Harfi</span><span class="sxs-lookup"><span data-stu-id="957a2-129">Sum</span></span>

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

### <span data-ttu-id="957a2-130">-İşleç</span><span class="sxs-lookup"><span data-stu-id="957a2-130">-Operator</span></span>
<span data-ttu-id="957a2-131">İşleci belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-131">Specifies the operator.</span></span>
<span data-ttu-id="957a2-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="957a2-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="957a2-133">Ken</span><span class="sxs-lookup"><span data-stu-id="957a2-133">Equals</span></span>
- <span data-ttu-id="957a2-134">Notals</span><span class="sxs-lookup"><span data-stu-id="957a2-134">NotEquals</span></span>
- <span data-ttu-id="957a2-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="957a2-135">GreaterThan</span></span>
- <span data-ttu-id="957a2-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="957a2-136">GreaterThanOrEqual</span></span>
- <span data-ttu-id="957a2-137">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="957a2-137">LessThan</span></span>
- <span data-ttu-id="957a2-138">Gezi Bayramı</span><span class="sxs-lookup"><span data-stu-id="957a2-138">LessThanOrEqual</span></span>

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

### <span data-ttu-id="957a2-139">-Scaleactioncoolaşağı</span><span class="sxs-lookup"><span data-stu-id="957a2-139">-ScaleActionCooldown</span></span>
<span data-ttu-id="957a2-140">Coolıyuvarla eylemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-140">Specifies the Autoscale action cooldown time.</span></span>

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

### <span data-ttu-id="957a2-141">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="957a2-141">-ScaleActionDirection</span></span>
<span data-ttu-id="957a2-142">Ölçek eyleminin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-142">Specifies the scale action direction.</span></span>
<span data-ttu-id="957a2-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="957a2-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="957a2-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="957a2-144">None</span></span>
- <span data-ttu-id="957a2-145">Artırmak</span><span class="sxs-lookup"><span data-stu-id="957a2-145">Increase</span></span>
- <span data-ttu-id="957a2-146">Azalt</span><span class="sxs-lookup"><span data-stu-id="957a2-146">Decrease</span></span>

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

### <span data-ttu-id="957a2-147">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="957a2-147">-ScaleActionScaleType</span></span>
<span data-ttu-id="957a2-148">Ölçek türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-148">Specifies the scale type.</span></span>
<span data-ttu-id="957a2-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="957a2-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="957a2-150">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="957a2-150">ChangeSize</span></span>
- <span data-ttu-id="957a2-151">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="957a2-151">ChangeCount</span></span>
- <span data-ttu-id="957a2-152">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="957a2-152">PercentChangeCount</span></span>
- <span data-ttu-id="957a2-153">ExactCount</span><span class="sxs-lookup"><span data-stu-id="957a2-153">ExactCount</span></span>

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

### <span data-ttu-id="957a2-154">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="957a2-154">-ScaleActionValue</span></span>
<span data-ttu-id="957a2-155">Eylem değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-155">Specifies the action value.</span></span>

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

### <span data-ttu-id="957a2-156">Eşiği</span><span class="sxs-lookup"><span data-stu-id="957a2-156">-Threshold</span></span>
<span data-ttu-id="957a2-157">Ölçüm değerinin eşiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-157">Specifies the threshold of the metric value.</span></span>

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

### <span data-ttu-id="957a2-158">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="957a2-158">-TimeAggregationOperator</span></span>
<span data-ttu-id="957a2-159">Zaman toplama işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-159">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="957a2-160">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="957a2-160">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="957a2-161">Geçen</span><span class="sxs-lookup"><span data-stu-id="957a2-161">Average</span></span>
- <span data-ttu-id="957a2-162">Gerekliliktir</span><span class="sxs-lookup"><span data-stu-id="957a2-162">Minimum</span></span>
- <span data-ttu-id="957a2-163">Sayısını</span><span class="sxs-lookup"><span data-stu-id="957a2-163">Maximum</span></span>
- <span data-ttu-id="957a2-164">Soya</span><span class="sxs-lookup"><span data-stu-id="957a2-164">Last</span></span>
- <span data-ttu-id="957a2-165">Toplam, say</span><span class="sxs-lookup"><span data-stu-id="957a2-165">Total, Count</span></span>

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

### <span data-ttu-id="957a2-166">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="957a2-166">-TimeGrain</span></span>
<span data-ttu-id="957a2-167">Zaman gösterimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-167">Specifies the time grain.</span></span>

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

### <span data-ttu-id="957a2-168">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="957a2-168">-TimeWindow</span></span>
<span data-ttu-id="957a2-169">Zaman penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="957a2-169">Specifies the time window.</span></span>

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

### <span data-ttu-id="957a2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="957a2-170">CommonParameters</span></span>
<span data-ttu-id="957a2-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="957a2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="957a2-172">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="957a2-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="957a2-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="957a2-173">INPUTS</span></span>

### <span data-ttu-id="957a2-174">System. String</span><span class="sxs-lookup"><span data-stu-id="957a2-174">System.String</span></span>

### <span data-ttu-id="957a2-175">Microsoft. Azure. Management. Monitor. Management. modeller. ComparisonOperationType</span><span class="sxs-lookup"><span data-stu-id="957a2-175">Microsoft.Azure.Management.Monitor.Management.Models.ComparisonOperationType</span></span>

### <span data-ttu-id="957a2-176">Microsoft. Azure. Management. Monitor. Management. modeller. MetricStatisticType</span><span class="sxs-lookup"><span data-stu-id="957a2-176">Microsoft.Azure.Management.Monitor.Management.Models.MetricStatisticType</span></span>

### <span data-ttu-id="957a2-177">System. Double</span><span class="sxs-lookup"><span data-stu-id="957a2-177">System.Double</span></span>

### <span data-ttu-id="957a2-178">Microsoft. Azure. Management. Monitor. Management. modeller. TimeAggregationType</span><span class="sxs-lookup"><span data-stu-id="957a2-178">Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationType</span></span>

### <span data-ttu-id="957a2-179">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="957a2-179">System.TimeSpan</span></span>

### <span data-ttu-id="957a2-180">Microsoft. Azure. Management. Monitor. Management. modeller. ScaleDirection</span><span class="sxs-lookup"><span data-stu-id="957a2-180">Microsoft.Azure.Management.Monitor.Management.Models.ScaleDirection</span></span>

### <span data-ttu-id="957a2-181">Microsoft. Azure. Management. Monitor. Management. modeller. ScaleType</span><span class="sxs-lookup"><span data-stu-id="957a2-181">Microsoft.Azure.Management.Monitor.Management.Models.ScaleType</span></span>

## <span data-ttu-id="957a2-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="957a2-182">OUTPUTS</span></span>

### <span data-ttu-id="957a2-183">Microsoft. Azure. Management. Monitor. Management. modeller. Salerule</span><span class="sxs-lookup"><span data-stu-id="957a2-183">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="957a2-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="957a2-184">NOTES</span></span>

## <span data-ttu-id="957a2-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="957a2-185">RELATED LINKS</span></span>

[<span data-ttu-id="957a2-186">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="957a2-186">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="957a2-187">Get-Azotomatik ölçek geçmişi</span><span class="sxs-lookup"><span data-stu-id="957a2-187">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="957a2-188">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="957a2-188">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="957a2-189">Yeni-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="957a2-189">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="957a2-190">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="957a2-190">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


