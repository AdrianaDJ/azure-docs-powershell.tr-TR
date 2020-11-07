---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalerule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleRule.md
ms.openlocfilehash: 575c6e5b210ca47e1904c5174f97b5886b0428b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763277"
---
# <span data-ttu-id="581bf-101">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="581bf-101">New-AzureRmAutoscaleRule</span></span>

## <span data-ttu-id="581bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="581bf-102">SYNOPSIS</span></span>
<span data-ttu-id="581bf-103">Otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="581bf-103">Creates an Autoscale rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="581bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="581bf-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleRule -MetricName <String> -MetricResourceId <String> -Operator <ComparisonOperationType>
 -MetricStatistic <MetricStatisticType> -Threshold <Double> [-TimeAggregationOperator <TimeAggregationType>]
 -TimeGrain <TimeSpan> [-TimeWindow <TimeSpan>] -ScaleActionCooldown <TimeSpan>
 -ScaleActionDirection <ScaleDirection> [-ScaleActionScaleType <ScaleType>] -ScaleActionValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="581bf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="581bf-105">DESCRIPTION</span></span>
<span data-ttu-id="581bf-106">**Yeni-AzureRmAutoscaleRule** cmdlet 'ı otomatik ölçeklendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="581bf-106">The **New-AzureRmAutoscaleRule** cmdlet creates an Autoscale rule.</span></span>

## <span data-ttu-id="581bf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="581bf-107">EXAMPLES</span></span>

### <span data-ttu-id="581bf-108">Örnek 1: kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="581bf-108">Example 1: Create a rule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="581bf-109">Bu komut bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="581bf-109">This command creates a rule.</span></span>

### <span data-ttu-id="581bf-110">Örnek 2: iki kural oluşturma</span><span class="sxs-lookup"><span data-stu-id="581bf-110">Example 2: Create two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"
MetricTrigger                                               ScaleAction
-------------                                               -----------
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
Microsoft.Azure.Management.Insights.Models.MetricTrigger    Microsoft.Azure.Management.Insights.Models.ScaleAction
```

<span data-ttu-id="581bf-111">İlk komut Istekler için bir kural oluşturur ve sonra bunu $Rule 1 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="581bf-111">The first command creates a rule for the Requests metric, and then stores it in the $Rule1 variable.</span></span>

<span data-ttu-id="581bf-112">İkinci komut Istekler için ikinci bir kural oluşturur ve ardından $Rule 2 değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="581bf-112">The second command creates a second rule for the Requests metric, and then stores it in the $Rule2 variable.</span></span>

## <span data-ttu-id="581bf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="581bf-113">PARAMETERS</span></span>

### <span data-ttu-id="581bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581bf-114">-DefaultProfile</span></span>
<span data-ttu-id="581bf-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="581bf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="581bf-116">-MetricName</span><span class="sxs-lookup"><span data-stu-id="581bf-116">-MetricName</span></span>
<span data-ttu-id="581bf-117">Ölçümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-117">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-118">-Metricresourceıd</span><span class="sxs-lookup"><span data-stu-id="581bf-118">-MetricResourceId</span></span>
<span data-ttu-id="581bf-119">Ölçüm kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-119">Specifies the metric resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-120">-Metricistatistiğini</span><span class="sxs-lookup"><span data-stu-id="581bf-120">-MetricStatistic</span></span>
<span data-ttu-id="581bf-121">Ölçüm istatistiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-121">Specifies the metric statistic.</span></span>
<span data-ttu-id="581bf-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="581bf-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="581bf-123">Geçen</span><span class="sxs-lookup"><span data-stu-id="581bf-123">Average</span></span>
- <span data-ttu-id="581bf-124">Enaz</span><span class="sxs-lookup"><span data-stu-id="581bf-124">Min</span></span>
- <span data-ttu-id="581bf-125">Biçimlendir</span><span class="sxs-lookup"><span data-stu-id="581bf-125">Max</span></span>
- <span data-ttu-id="581bf-126">Harfi</span><span class="sxs-lookup"><span data-stu-id="581bf-126">Sum</span></span>

```yaml
Type: MetricStatisticType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Min, Max, Sum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-127">-İşleç</span><span class="sxs-lookup"><span data-stu-id="581bf-127">-Operator</span></span>
<span data-ttu-id="581bf-128">İşleci belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-128">Specifies the operator.</span></span>
<span data-ttu-id="581bf-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="581bf-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="581bf-130">Ken</span><span class="sxs-lookup"><span data-stu-id="581bf-130">Equals</span></span>
- <span data-ttu-id="581bf-131">Notals</span><span class="sxs-lookup"><span data-stu-id="581bf-131">NotEquals</span></span>
- <span data-ttu-id="581bf-132">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="581bf-132">GreaterThan</span></span>
- <span data-ttu-id="581bf-133">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="581bf-133">GreaterThanOrEqual</span></span>
- <span data-ttu-id="581bf-134">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="581bf-134">LessThan</span></span>
- <span data-ttu-id="581bf-135">Gezi Bayramı</span><span class="sxs-lookup"><span data-stu-id="581bf-135">LessThanOrEqual</span></span>

```yaml
Type: ComparisonOperationType
Parameter Sets: (All)
Aliases: 
Accepted values: Equals, NotEquals, GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-136">-Scaleactioncoolaşağı</span><span class="sxs-lookup"><span data-stu-id="581bf-136">-ScaleActionCooldown</span></span>
<span data-ttu-id="581bf-137">Coolıyuvarla eylemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-137">Specifies the Autoscale action cooldown time.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-138">-ScaleActionDirection</span><span class="sxs-lookup"><span data-stu-id="581bf-138">-ScaleActionDirection</span></span>
<span data-ttu-id="581bf-139">Ölçek eyleminin yönünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-139">Specifies the scale action direction.</span></span>
<span data-ttu-id="581bf-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="581bf-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="581bf-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="581bf-141">None</span></span>
- <span data-ttu-id="581bf-142">Artırmak</span><span class="sxs-lookup"><span data-stu-id="581bf-142">Increase</span></span>
- <span data-ttu-id="581bf-143">Azalt</span><span class="sxs-lookup"><span data-stu-id="581bf-143">Decrease</span></span>

```yaml
Type: ScaleDirection
Parameter Sets: (All)
Aliases: 
Accepted values: None, Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-144">-ScaleActionScaleType</span><span class="sxs-lookup"><span data-stu-id="581bf-144">-ScaleActionScaleType</span></span>
<span data-ttu-id="581bf-145">Ölçek türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-145">Specifies the scale type.</span></span>
<span data-ttu-id="581bf-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="581bf-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="581bf-147">ChangeSize</span><span class="sxs-lookup"><span data-stu-id="581bf-147">ChangeSize</span></span>
- <span data-ttu-id="581bf-148">ChangeCount</span><span class="sxs-lookup"><span data-stu-id="581bf-148">ChangeCount</span></span>
- <span data-ttu-id="581bf-149">PercentChangeCount</span><span class="sxs-lookup"><span data-stu-id="581bf-149">PercentChangeCount</span></span>
- <span data-ttu-id="581bf-150">ExactCount</span><span class="sxs-lookup"><span data-stu-id="581bf-150">ExactCount</span></span>

```yaml
Type: ScaleType
Parameter Sets: (All)
Aliases: 
Accepted values: ChangeCount, PercentChangeCount, ExactCount

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-151">-ScaleActionValue</span><span class="sxs-lookup"><span data-stu-id="581bf-151">-ScaleActionValue</span></span>
<span data-ttu-id="581bf-152">Eylem değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-152">Specifies the action value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-153">Eşiği</span><span class="sxs-lookup"><span data-stu-id="581bf-153">-Threshold</span></span>
<span data-ttu-id="581bf-154">Ölçüm değerinin eşiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-154">Specifies the threshold of the metric value.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-155">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="581bf-155">-TimeAggregationOperator</span></span>
<span data-ttu-id="581bf-156">Zaman toplama işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-156">Specifies the time aggregation operator.</span></span>
<span data-ttu-id="581bf-157">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="581bf-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="581bf-158">Geçen</span><span class="sxs-lookup"><span data-stu-id="581bf-158">Average</span></span>
- <span data-ttu-id="581bf-159">Gerekliliktir</span><span class="sxs-lookup"><span data-stu-id="581bf-159">Minimum</span></span>
- <span data-ttu-id="581bf-160">Sayısını</span><span class="sxs-lookup"><span data-stu-id="581bf-160">Maximum</span></span>
- <span data-ttu-id="581bf-161">Soya</span><span class="sxs-lookup"><span data-stu-id="581bf-161">Last</span></span>
- <span data-ttu-id="581bf-162">Toplam, say</span><span class="sxs-lookup"><span data-stu-id="581bf-162">Total, Count</span></span>

```yaml
Type: TimeAggregationType
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Count

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-163">-Zaman çizgisi</span><span class="sxs-lookup"><span data-stu-id="581bf-163">-TimeGrain</span></span>
<span data-ttu-id="581bf-164">Zaman gösterimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-164">Specifies the time grain.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-165">-TimeWindow</span><span class="sxs-lookup"><span data-stu-id="581bf-165">-TimeWindow</span></span>
<span data-ttu-id="581bf-166">Zaman penceresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="581bf-166">Specifies the time window.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="581bf-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581bf-167">CommonParameters</span></span>
<span data-ttu-id="581bf-168">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="581bf-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581bf-169">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="581bf-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581bf-170">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="581bf-170">INPUTS</span></span>

### <span data-ttu-id="581bf-171">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="581bf-171">None</span></span>
<span data-ttu-id="581bf-172">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="581bf-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="581bf-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="581bf-173">OUTPUTS</span></span>

### <span data-ttu-id="581bf-174">Microsoft. Azure. Management. Monitor. Management. modeller. Salerule</span><span class="sxs-lookup"><span data-stu-id="581bf-174">Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule</span></span>

## <span data-ttu-id="581bf-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="581bf-175">NOTES</span></span>

## <span data-ttu-id="581bf-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="581bf-176">RELATED LINKS</span></span>

[<span data-ttu-id="581bf-177">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="581bf-177">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="581bf-178">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="581bf-178">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="581bf-179">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="581bf-179">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="581bf-180">Yeni-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="581bf-180">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="581bf-181">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="581bf-181">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


