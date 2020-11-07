---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: bb72a50c2db43a8db053d273c601ca51e96402f0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935710"
---
# <span data-ttu-id="187a8-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="187a8-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="187a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="187a8-102">SYNOPSIS</span></span>
<span data-ttu-id="187a8-103">Yeni bir metrik uyarısı oluşturmak için kullanılabilecek bir yerel ölçüt nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="187a8-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="187a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="187a8-104">SYNTAX</span></span>

### <span data-ttu-id="187a8-105">StaticThresholdParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="187a8-105">StaticThresholdParameterSet (Default)</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="187a8-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="187a8-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria [-DynamicThreshold] -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 [-ThresholdSensitivity <String>] [-ViolationCount <Int32>] [-ExaminedAggregatedPointCount <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="187a8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="187a8-107">DESCRIPTION</span></span>
<span data-ttu-id="187a8-108">**New-AzMetricAlertRuleV2Criteria** cmdlet 'i, yeni bir metrik uyarı kuralı oluşturan bir giriş Add-AzMetricAlertRuleV2 cmdlet 'i olarak kullanılmak üzere yerel bir metrik ölçüt nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="187a8-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="187a8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="187a8-109">EXAMPLES</span></span>

### <span data-ttu-id="187a8-110">Örnek 1: basit bir metrik uyarı ölçütleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="187a8-110">Example 1: Create a simple metric alert criteria</span></span>

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

<span data-ttu-id="187a8-111">Bu komut, bir metrik uyarı kuralında kullanılabilen basit bir metrik uyarı ölçütleri oluşturur</span><span class="sxs-lookup"><span data-stu-id="187a8-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="187a8-112">Örnek 2: dinamik bir metrik uyarı ölçütleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="187a8-112">Example 2: Create a dynamic metric alert criteria</span></span>

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

<span data-ttu-id="187a8-113">Bu komut, bir metrik uyarı kuralında kullanılabilecek bir dinamik ölçü uyarısı ölçütü oluşturur</span><span class="sxs-lookup"><span data-stu-id="187a8-113">This command creates a Dynamic metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="187a8-114">Örnek 3: daha karmaşık bir metrik uyarı ölçütü oluşturma</span><span class="sxs-lookup"><span data-stu-id="187a8-114">Example 3: Create a more complex metric alert criteria</span></span>

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

<span data-ttu-id="187a8-115">Bu komut kümesi, boyut seçimi içeren daha karmaşık bir metrik uyarı ölçütü oluşturur</span><span class="sxs-lookup"><span data-stu-id="187a8-115">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="187a8-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="187a8-116">PARAMETERS</span></span>

### <span data-ttu-id="187a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187a8-117">-DefaultProfile</span></span>
<span data-ttu-id="187a8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="187a8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="187a8-119">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="187a8-119">-DimensionSelection</span></span>
<span data-ttu-id="187a8-120">Boyut koşullarının listesi</span><span class="sxs-lookup"><span data-stu-id="187a8-120">List of dimension conditions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="187a8-121">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="187a8-121">-DynamicThreshold</span></span>
<span data-ttu-id="187a8-122">Dinamik Eşik türü kullanımıyla ilgili anahtar parametresi</span><span class="sxs-lookup"><span data-stu-id="187a8-122">Switch parameter for using Dynamic Threshold Type</span></span>

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

### <span data-ttu-id="187a8-123">-ExaminedAggregatedPointCount</span><span class="sxs-lookup"><span data-stu-id="187a8-123">-ExaminedAggregatedPointCount</span></span>
<span data-ttu-id="187a8-124">İncelenen toplam puan sayısı</span><span class="sxs-lookup"><span data-stu-id="187a8-124">The Total number of examined points</span></span>

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

### <span data-ttu-id="187a8-125">-Ignoredatabefore</span><span class="sxs-lookup"><span data-stu-id="187a8-125">-IgnoreDataBefore</span></span>
<span data-ttu-id="187a8-126">Ignoredatabefore parametresi</span><span class="sxs-lookup"><span data-stu-id="187a8-126">The IgnoreDataBefore parameter</span></span>

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

### <span data-ttu-id="187a8-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="187a8-127">-MetricName</span></span>
<span data-ttu-id="187a8-128">Kuralın ölçü adı</span><span class="sxs-lookup"><span data-stu-id="187a8-128">The metric name for rule</span></span>

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

### <span data-ttu-id="187a8-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="187a8-129">-MetricNamespace</span></span>
<span data-ttu-id="187a8-130">Ölçümün ad alanı</span><span class="sxs-lookup"><span data-stu-id="187a8-130">The Namespace of the metric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187a8-131">-İşleç</span><span class="sxs-lookup"><span data-stu-id="187a8-131">-Operator</span></span>
<span data-ttu-id="187a8-132">Kural koşulu işleci</span><span class="sxs-lookup"><span data-stu-id="187a8-132">The rule condition operator</span></span>

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

### <span data-ttu-id="187a8-133">Eşiği</span><span class="sxs-lookup"><span data-stu-id="187a8-133">-Threshold</span></span>
<span data-ttu-id="187a8-134">Kural koşulu eşiği</span><span class="sxs-lookup"><span data-stu-id="187a8-134">The threshold for rule condition</span></span>

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

### <span data-ttu-id="187a8-135">-Thresholdduyarlılık</span><span class="sxs-lookup"><span data-stu-id="187a8-135">-ThresholdSensitivity</span></span>
<span data-ttu-id="187a8-136">Kural koşulu için duyarlılık</span><span class="sxs-lookup"><span data-stu-id="187a8-136">The sensitivity for rule condition</span></span>

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

### <span data-ttu-id="187a8-137">-Timetoplamayı</span><span class="sxs-lookup"><span data-stu-id="187a8-137">-TimeAggregation</span></span>
<span data-ttu-id="187a8-138">Pencere aralığında birden çok ölçüm değerini aktarmak için kullanılan toplama işlemi</span><span class="sxs-lookup"><span data-stu-id="187a8-138">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

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

### <span data-ttu-id="187a8-139">-ViolationCount</span><span class="sxs-lookup"><span data-stu-id="187a8-139">-ViolationCount</span></span>
<span data-ttu-id="187a8-140">Uyarı oluşturmak için seçilen geri dönüş zamanı penceresinde gereken en az ihlal sayısı</span><span class="sxs-lookup"><span data-stu-id="187a8-140">The minimum number of violations required within the selected lookback time window required to raise an alert</span></span>

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

### <span data-ttu-id="187a8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187a8-141">CommonParameters</span></span>
<span data-ttu-id="187a8-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="187a8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187a8-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="187a8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187a8-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="187a8-144">INPUTS</span></span>

### <span data-ttu-id="187a8-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="187a8-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="187a8-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="187a8-146">OUTPUTS</span></span>

### <span data-ttu-id="187a8-147">Microsoft. Azure. Commands. Insights. outputclasses. ıpsmulw32</span><span class="sxs-lookup"><span data-stu-id="187a8-147">Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria</span></span>

## <span data-ttu-id="187a8-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="187a8-148">NOTES</span></span>

## <span data-ttu-id="187a8-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="187a8-149">RELATED LINKS</span></span>
