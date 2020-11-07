---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricalertrulev2criteria
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricAlertRuleV2Criteria.md
ms.openlocfilehash: 16687824216fa0014d59b78a96d22a4da8a19fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915611"
---
# <span data-ttu-id="d1416-101">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="d1416-101">New-AzMetricAlertRuleV2Criteria</span></span>

## <span data-ttu-id="d1416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1416-102">SYNOPSIS</span></span>
<span data-ttu-id="d1416-103">Yeni bir metrik uyarısı oluşturmak için kullanılabilecek bir yerel ölçüt nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="d1416-103">Creates a local criteria object that can be used to create a new metric alert</span></span>

## <span data-ttu-id="d1416-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1416-104">SYNTAX</span></span>

### <span data-ttu-id="d1416-105">StaticThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1416-105">StaticThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String> -Threshold <Double>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1416-106">DynamicThresholdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1416-106">DynamicThresholdParameterSet</span></span>
```
New-AzMetricAlertRuleV2Criteria -MetricName <String> [-MetricNamespace <String>]
 [-DimensionSelection <PSMetricDimension[]>] -TimeAggregation <String> -Operator <String>
 -DynamicThreshold <String> [-Sensitivity <String>] [-FailingPeriod <Int32>] [-TotalPeriod <Int32>]
 [-IgnoreDataBefore <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1416-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1416-107">DESCRIPTION</span></span>
<span data-ttu-id="d1416-108">**New-AzMetricAlertRuleV2Criteria** cmdlet 'i, yeni bir metrik uyarı kuralı oluşturan bir giriş Add-AzMetricAlertRuleV2 cmdlet 'i olarak kullanılmak üzere yerel bir metrik ölçüt nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d1416-108">The **New-AzMetricAlertRuleV2Criteria** cmdlet creates a local metric criteria object to be used as an input Add-AzMetricAlertRuleV2 cmdlet which creates a new metric alert rule.</span></span>

## <span data-ttu-id="d1416-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1416-109">EXAMPLES</span></span>

### <span data-ttu-id="d1416-110">Örnek 1: basit bir metrik uyarı ölçütleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="d1416-110">Example 1: Create a simple metric alert criteria</span></span>

```powershell
PS C:\> New-AzMetricAlertRuleV2Criteria -MetricName "Percentage CPU" -MetricNameSpace "Microsoft.Compute/virtualMachines" -TimeAggregation Average -Operator GreaterThan -Threshold 5

Name                 : metric1
MetricName           : Percentage CPU
MetricNamespace      : Microsoft.Compute/virtualMachines
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 5
Dimensions           :
AdditionalProperties :
```

<span data-ttu-id="d1416-111">Bu komut, bir metrik uyarı kuralında kullanılabilen basit bir metrik uyarı ölçütleri oluşturur</span><span class="sxs-lookup"><span data-stu-id="d1416-111">This command creates a simple metric alert criteria that can be used in a metric alert rule</span></span>

### <span data-ttu-id="d1416-112">Örnek 2: daha karmaşık bir metrik uyarı ölçütleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="d1416-112">Example 2: Create a more complex metric alert criteria</span></span>

```powershell
PS C:\>New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest" | New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -TimeAggregation Average -Operator GreaterThan -Threshold 2
Name                 : metric1
MetricName           : availabilityResults/availabilityPercentage
MetricNamespace      :
OperatorProperty     : GreaterThan
TimeAggregation      : Average
Threshold            : 2
Dimensions           : {availabilityResult/name}
AdditionalProperties :
```

<span data-ttu-id="d1416-113">Bu komut kümesi, boyut seçimi içeren daha karmaşık bir metrik uyarı ölçütü oluşturur</span><span class="sxs-lookup"><span data-stu-id="d1416-113">This set of commands creates a more complex metric alert criteria which includes dimension selection</span></span>

## <span data-ttu-id="d1416-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1416-114">PARAMETERS</span></span>

### <span data-ttu-id="d1416-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1416-115">-DefaultProfile</span></span>
<span data-ttu-id="d1416-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1416-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-117">-DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="d1416-117">-DimensionSelection</span></span>
<span data-ttu-id="d1416-118">Boyut koşullarının listesi</span><span class="sxs-lookup"><span data-stu-id="d1416-118">List of dimension conditions</span></span>

```yaml
Type: PSMetricDimension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-119">-DynamicThreshold</span><span class="sxs-lookup"><span data-stu-id="d1416-119">-DynamicThreshold</span></span>
<span data-ttu-id="d1416-120">Kural koşulu için dinamik eşik</span><span class="sxs-lookup"><span data-stu-id="d1416-120">The Dynamic Threshold for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-121">-Failingdönemi</span><span class="sxs-lookup"><span data-stu-id="d1416-121">-FailingPeriod</span></span>
<span data-ttu-id="d1416-122">Kural koşulu için başarısız olan süre</span><span class="sxs-lookup"><span data-stu-id="d1416-122">The Failing Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-123">-Ignoredatabefore</span><span class="sxs-lookup"><span data-stu-id="d1416-123">-IgnoreDataBefore</span></span>
<span data-ttu-id="d1416-124">Ignoredatabefore parametresi</span><span class="sxs-lookup"><span data-stu-id="d1416-124">The IgnoreDataBefore parameter</span></span>

```yaml
Type: DateTime
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="d1416-125">-MetricName</span></span>
<span data-ttu-id="d1416-126">Kuralın ölçü adı</span><span class="sxs-lookup"><span data-stu-id="d1416-126">The metric name for rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-127">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="d1416-127">-MetricNamespace</span></span>
<span data-ttu-id="d1416-128">Ölçümün ad alanı</span><span class="sxs-lookup"><span data-stu-id="d1416-128">The Namespace of the metric</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-129">-İşleç</span><span class="sxs-lookup"><span data-stu-id="d1416-129">-Operator</span></span>
<span data-ttu-id="d1416-130">Kural koşulu işleci</span><span class="sxs-lookup"><span data-stu-id="d1416-130">The rule condition operator</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-131">Duyarlılığı</span><span class="sxs-lookup"><span data-stu-id="d1416-131">-Sensitivity</span></span>
<span data-ttu-id="d1416-132">Kural koşulu için duyarlılık</span><span class="sxs-lookup"><span data-stu-id="d1416-132">The sensitivity for rule condition</span></span>

```yaml
Type: String
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-133">Eşiği</span><span class="sxs-lookup"><span data-stu-id="d1416-133">-Threshold</span></span>
<span data-ttu-id="d1416-134">Kural koşulu eşiği</span><span class="sxs-lookup"><span data-stu-id="d1416-134">The threshold for rule condition</span></span>

```yaml
Type: Double
Parameter Sets: StaticThresholdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-135">-Timetoplamayı</span><span class="sxs-lookup"><span data-stu-id="d1416-135">-TimeAggregation</span></span>
<span data-ttu-id="d1416-136">Pencere aralığında birden çok ölçüm değerini aktarmak için kullanılan toplama işlemi</span><span class="sxs-lookup"><span data-stu-id="d1416-136">The aggregation operation used to roll up multiple metric values across the window interval</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-137">-Toplamdönem</span><span class="sxs-lookup"><span data-stu-id="d1416-137">-TotalPeriod</span></span>
<span data-ttu-id="d1416-138">Kural koşulunun toplam dönemi</span><span class="sxs-lookup"><span data-stu-id="d1416-138">The Total Period for rule condition</span></span>

```yaml
Type: Int32
Parameter Sets: DynamicThresholdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1416-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1416-139">CommonParameters</span></span>
<span data-ttu-id="d1416-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1416-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d1416-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1416-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1416-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1416-142">INPUTS</span></span>

### <span data-ttu-id="d1416-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDimension []</span><span class="sxs-lookup"><span data-stu-id="d1416-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDimension[]</span></span>

## <span data-ttu-id="d1416-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1416-144">OUTPUTS</span></span>

### <span data-ttu-id="d1416-145">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricCriteria</span><span class="sxs-lookup"><span data-stu-id="d1416-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricCriteria</span></span>

## <span data-ttu-id="d1416-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1416-146">NOTES</span></span>

## <span data-ttu-id="d1416-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1416-147">RELATED LINKS</span></span>
