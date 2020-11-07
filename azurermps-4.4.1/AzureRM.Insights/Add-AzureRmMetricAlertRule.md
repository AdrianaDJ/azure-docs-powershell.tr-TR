---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmMetricAlertRule.md
ms.openlocfilehash: 9a215195ada1d804d2c139ed748eb844df46eed5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764831"
---
# <span data-ttu-id="076f4-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="076f4-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="076f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="076f4-102">SYNOPSIS</span></span>
<span data-ttu-id="076f4-103">Bir metrik temelinde bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="076f4-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="076f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="076f4-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="076f4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="076f4-105">DESCRIPTION</span></span>
<span data-ttu-id="076f4-106">**Add-AzureRmMetricAlertRule** cmdlet 'i, metrik tabanlı bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="076f4-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="076f4-107">Ek kural bir kaynak grubuyla ilişkilendirilir ve bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="076f4-107">The added rule is associated with a resource group and has a name.</span></span>

## <span data-ttu-id="076f4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="076f4-108">EXAMPLES</span></span>

### <span data-ttu-id="076f4-109">Örnek 1: Web sitesine bir metrik uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="076f4-109">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="076f4-110">Bu komut Web sitesi için bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="076f4-110">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="076f4-111">Örnek 2: bir kuralı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="076f4-111">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="076f4-112">Bu komut bir kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="076f4-112">This command disables a rule.</span></span>
<span data-ttu-id="076f4-113">Kural yoksa devre dışı olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="076f4-113">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="076f4-114">Kural varsa, bunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="076f4-114">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="076f4-115">Örnek 3: eylemlerle kural ekleme</span><span class="sxs-lookup"><span data-stu-id="076f4-115">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="076f4-116">Bu komut Web sitesi için bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="076f4-116">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="076f4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="076f4-117">PARAMETERS</span></span>

### <span data-ttu-id="076f4-118">-Eylemler</span><span class="sxs-lookup"><span data-stu-id="076f4-118">-Actions</span></span>
<span data-ttu-id="076f4-119">Virgülle ayrılmış bir eylem listesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-119">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="076f4-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="076f4-120">-Description</span></span>
<span data-ttu-id="076f4-121">Kuralın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-121">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="076f4-122">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="076f4-122">-DisableRule</span></span>
<span data-ttu-id="076f4-123">Kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="076f4-123">Disables the rule.</span></span>
<span data-ttu-id="076f4-124">Bu parametreyi belirtmezseniz, kural etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="076f4-124">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="076f4-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="076f4-125">-Location</span></span>
<span data-ttu-id="076f4-126">Kuralın tanımlandığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="076f4-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="076f4-127">-MetricName</span></span>
<span data-ttu-id="076f4-128">Kuralın izlenme ölçümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-128">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="076f4-129">Bu parametreyi yalnızca metrik tabanlı kurallar için belirtin.</span><span class="sxs-lookup"><span data-stu-id="076f4-129">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="076f4-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="076f4-130">-Name</span></span>
<span data-ttu-id="076f4-131">Kuralın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-131">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="076f4-132">-İşleç</span><span class="sxs-lookup"><span data-stu-id="076f4-132">-Operator</span></span>
<span data-ttu-id="076f4-133">Kural koşulunun ilişkisel işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-133">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="076f4-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="076f4-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="076f4-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="076f4-135">GreaterThan</span></span>
- <span data-ttu-id="076f4-136">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="076f4-136">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="076f4-137">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="076f4-137">LessThan</span></span>
- <span data-ttu-id="076f4-138">Gezi Bayramı</span><span class="sxs-lookup"><span data-stu-id="076f4-138">LessThanOrEqual</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator
Parameter Sets: (All)
Aliases: 
Accepted values: GreaterThan, GreaterThanOrEqual, LessThan, LessThanOrEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="076f4-139">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="076f4-139">-ResourceGroup</span></span>
<span data-ttu-id="076f4-140">Kuralın kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-140">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="076f4-141">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="076f4-141">-TargetResourceId</span></span>
<span data-ttu-id="076f4-142">Kuralın izlenme kaynağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-142">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="076f4-143">Not: var olan bir uyarı kuralı için bu özellik güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="076f4-143">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="076f4-144">Eşiği</span><span class="sxs-lookup"><span data-stu-id="076f4-144">-Threshold</span></span>
<span data-ttu-id="076f4-145">Kuralın eşiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-145">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="076f4-146">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="076f4-146">-TimeAggregationOperator</span></span>
<span data-ttu-id="076f4-147">Kural değerlendirilirken zaman penceresine uygulanacak toplama işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-147">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator]
Parameter Sets: (All)
Aliases: 
Accepted values: Average, Minimum, Maximum, Total, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="076f4-148">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="076f4-148">-WindowSize</span></span>
<span data-ttu-id="076f4-149">Kuralın verilerinin hesaplanması için zaman penceresi boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="076f4-149">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="076f4-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="076f4-150">-DefaultProfile</span></span>
<span data-ttu-id="076f4-151">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="076f4-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="076f4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="076f4-152">CommonParameters</span></span>
<span data-ttu-id="076f4-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="076f4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="076f4-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="076f4-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="076f4-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="076f4-155">INPUTS</span></span>

## <span data-ttu-id="076f4-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="076f4-156">OUTPUTS</span></span>

### <span data-ttu-id="076f4-157">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="076f4-157">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="076f4-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="076f4-158">NOTES</span></span>

## <span data-ttu-id="076f4-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="076f4-159">RELATED LINKS</span></span>

[<span data-ttu-id="076f4-160">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="076f4-160">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="076f4-161">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="076f4-161">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="076f4-162">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="076f4-162">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="076f4-163">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="076f4-163">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="076f4-164">Yeni-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="076f4-164">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="076f4-165">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="076f4-165">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="076f4-166">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="076f4-166">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


