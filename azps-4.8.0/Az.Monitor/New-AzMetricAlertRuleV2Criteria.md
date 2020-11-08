---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 101d522c1f8ae3b44545bdb204bad01fbe21df9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274425"
---
# <span data-ttu-id="2f650-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2f650-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="2f650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f650-102">SYNOPSIS</span></span>
<span data-ttu-id="2f650-103">Yeni bir metrik uyarısı oluşturmak için kullanılabilecek bir yerel ölçüt nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="2f650-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="2f650-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f650-104">SYNTAX</span></span>

### <span data-ttu-id="2f650-105">StaticThresholdParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f650-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> -Threshold <Double> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f650-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f650-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-SkipMetricValidation <Boolean>] [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String>
 -Operator <String> [-ThresholdSensitivity <String>] [-ViolationCount <Int32>]
 [-ExaminedAggregatedPointCount <Int32>] [-IgnoreDataBefore <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f650-107">WebtestParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f650-107">WebtestParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-WebTest] -WebTestId <String> -ApplicationInsightsId <String>
 [-FailedLocationCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f650-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f650-108">DESCRIPTION</span></span>
<span data-ttu-id="2f650-109">**New-AzMetricAlertRuleV2Criteria** cmdlet 'i, yeni bir metrik uyarı kuralı oluşturan bir giriş Add-AzMetricAlertRuleV2 cmdlet 'i olarak kullanılmak üzere yerel bir metrik ölçüt nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2f650-109">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="2f650-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f650-110">EXAMPLES</span></span>

### <span data-ttu-id="2f650-111">Örnek 1: basit bir metrik uyarı ölçütleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f650-111">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 5
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="2f650-112">Bu komut, bir metrik uyarı kuralında kullanılabilen basit bir metrik uyarı ölçütleri oluşturur</span><span class="sxs-lookup"><span data-stu-id="2f650-112">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="2f650-113">Örnek 2: dinamik bir metrik uyarı ölçütleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f650-113">Example 2: Create a dynamic metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -Dynamic -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -ThresholdSensitivity Medium -ViolationCount 2 -ExaminedAggregatedPointCount 4
CriterionType        : DynamicThresholdCriterion
OperatorProperty     : GreaterThan
AlertSensitivity     : Medium
FailingPeriods       : Microsoft.Azure.Management.Monitor.Models.DynamicThresholdFailingPeriods
IgnoreDataBefore     :
AdditionalProperties :
Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
TimeAggregation      : Average
Dimensions           :
```

<span data-ttu-id="2f650-114">Bu komut, bir metrik uyarı kuralında kullanılabilecek bir dinamik ölçü uyarısı ölçütü oluşturur</span><span class="sxs-lookup"><span data-stu-id="2f650-114">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="2f650-115">Örnek 3: daha karmaşık bir metrik uyarı ölçütü oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f650-115">Example 3: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
CriterionType        : StaticThresholdCriterion
OperatorProperty     : GreaterThan
Threshold            : 2
AdditionalProperties :
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
TimeAggregation      : Average
Dimensions           : {availabilityResult/name}
```

<span data-ttu-id="2f650-116">Bu komut kümesi, boyut seçimi içeren daha karmaşık bir metrik uyarı ölçütü oluşturur</span><span class="sxs-lookup"><span data-stu-id="2f650-116">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

### <span data-ttu-id="2f650-117">Örnek 4: WebTest kullanılabilirlik ölçütleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f650-117">Example 4: Create a webtest availability criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2Criteria -WebTest -WebTestId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights" -ApplicationInsightsId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights" -FailedLocationCount 3
CriterionType        : WebtestLocationAvailabilityCriterion
WebTestId            : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/webtests/PingTest-appInsights
ComponentId          : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Insights/components/appInsights
FailedLocationCount  : 3
AdditionalProperties :
```

<span data-ttu-id="2f650-118">Bu komut, bir metrik uyarı kuralında kullanılabilen bir WebTest kullanılabilirlik ölçütü oluşturur</span><span class="sxs-lookup"><span data-stu-id="2f650-118">This command creates a webtest availability criteria that can be used in a metric alert rule</span></span>

## <span data-ttu-id="2f650-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f650-119">PARAMETERS</span></span>

### <span data-ttu-id="2f650-120">-Applicationınsightsıd</span><span class="sxs-lookup"><span data-stu-id="2f650-120">-ApplicationInsightsId</span></span>
<span data-ttu-id="2f650-121">Application Insights kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2f650-121">The Application Insights resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases: componentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f650-122">-DefaultProfile</span></span>
<span data-ttu-id="2f650-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f650-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f650-124">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2f650-124">-DimensionSelection</span></span>
<span data-ttu-id="2f650-125">Boyut koşullarının listesi</span><span class="sxs-lookup"><span data-stu-id="2f650-125">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-126">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="2f650-126">-DynamicThreshold</span></span>
<span data-ttu-id="2f650-127">Dinamik Eşik türü kullanımıyla ilgili anahtar parametresi</span><span class="sxs-lookup"><span data-stu-id="2f650-127">Switch parameter for using Dynamic Threshold Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-128">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="2f650-128">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="2f650-129">İncelenen toplam puan sayısı</span><span class="sxs-lookup"><span data-stu-id="2f650-129">The Total number of examined points</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: TotalPeriod, NumberOfExaminedAggregatedPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-130">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="2f650-130">-FailedLocationCount</span></span>
<span data-ttu-id="2f650-131">Uyarı oluşturmak için en az başarısız konum sayısı.</span><span class="sxs-lookup"><span data-stu-id="2f650-131">The minimum number of failed locations to raise an alert.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WebtestParameterSet
Aliases: AlertLocationThreshold

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-132">-Ignoredatabefore</span><span class="sxs-lookup"><span data-stu-id="2f650-132">-IgnoreDataBefore</span></span>
<span data-ttu-id="2f650-133">Ignoredatabefore parametresi</span><span class="sxs-lookup"><span data-stu-id="2f650-133">The IgnoreDataBefore parameter</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-134">-MetricName</span><span class="sxs-lookup"><span data-stu-id="2f650-134">-MetricName</span></span>
<span data-ttu-id="2f650-135">Kuralın ölçü adı</span><span class="sxs-lookup"><span data-stu-id="2f650-135">The metric name for rule</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-136">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="2f650-136">-MetricNamespace</span></span>
<span data-ttu-id="2f650-137">Ölçümün ad alanı</span><span class="sxs-lookup"><span data-stu-id="2f650-137">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-138">-İşleç</span><span class="sxs-lookup"><span data-stu-id="2f650-138">-Operator</span></span>
<span data-ttu-id="2f650-139">Kural koşulu işleci</span><span class="sxs-lookup"><span data-stu-id="2f650-139">The rule condition operator</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-140">-SkipMetricValidation</span><span class="sxs-lookup"><span data-stu-id="2f650-140">-SkipMetricValidation</span></span>
<span data-ttu-id="2f650-141">Henüz yayınlanmadığınız özel bir ölçümde, ölçü doğrulamasının atlanmasına neden olan bir uyarı kuralı oluşturmaya olanak tanır</span><span class="sxs-lookup"><span data-stu-id="2f650-141">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-142">Eşiği</span><span class="sxs-lookup"><span data-stu-id="2f650-142">-Threshold</span></span>
<span data-ttu-id="2f650-143">Kural koşulu eşiği</span><span class="sxs-lookup"><span data-stu-id="2f650-143">The threshold for rule condition</span></span>

```yaml
Type: System.Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-144">-Thresholdduyarlılık</span><span class="sxs-lookup"><span data-stu-id="2f650-144">-ThresholdSensitivity</span></span>
<span data-ttu-id="2f650-145">Kural koşulu için duyarlılık</span><span class="sxs-lookup"><span data-stu-id="2f650-145">The sensitivity for rule condition</span></span>

```yaml
Type: System.String
Parameter Sets: DynamicThresholdParameterSet
Aliases: Sensitivity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-146">-Timetoplamayı</span><span class="sxs-lookup"><span data-stu-id="2f650-146">-TimeAggregation</span></span>
<span data-ttu-id="2f650-147">Pencere aralığında birden çok ölçüm değerini aktarmak için kullanılan toplama işlemi</span><span class="sxs-lookup"><span data-stu-id="2f650-147">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: System.String
Parameter Sets: StaticThresholdParameterSet, DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-148">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="2f650-148">-ViolationCount</span></span>
<span data-ttu-id="2f650-149">Uyarı oluşturmak için seçilen geri dönüş zamanı penceresinde gereken en az ihlal sayısı</span><span class="sxs-lookup"><span data-stu-id="2f650-149">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

```yaml
Type: System.Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases: FailingPeriod, NumberOfViolations

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-150">-WebTest</span><span class="sxs-lookup"><span data-stu-id="2f650-150">-WebTest</span></span>
<span data-ttu-id="2f650-151">Kullanılabilirlik ölçütü türünü kullanmak için Switch parametresi</span><span class="sxs-lookup"><span data-stu-id="2f650-151">Switch parameter for using availability criteria Type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebtestParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-152">-Webtesd</span><span class="sxs-lookup"><span data-stu-id="2f650-152">-WebTestId</span></span>
<span data-ttu-id="2f650-153">Application Insights Web test kimliği.</span><span class="sxs-lookup"><span data-stu-id="2f650-153">The Application Insights web test Id.</span></span>

```yaml
Type: System.String
Parameter Sets: WebtestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f650-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f650-154">CommonParameters</span></span>
<span data-ttu-id="2f650-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f650-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f650-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2f650-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f650-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f650-157">INPUTS</span></span>

### <span data-ttu-id="2f650-158">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="2f650-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="2f650-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f650-159">OUTPUTS</span></span>

### <span data-ttu-id="2f650-160">Microsoft. Azure. Commands. Insights. outputclasses. ıpsmulw32</span><span class="sxs-lookup"><span data-stu-id="2f650-160">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="2f650-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f650-161">NOTES</span></span>

## <span data-ttu-id="2f650-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f650-162">RELATED LINKS</span></span>
