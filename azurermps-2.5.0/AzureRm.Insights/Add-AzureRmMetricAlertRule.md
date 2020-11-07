---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermmetricalertrule
schema: 2.0.0
ms.openlocfilehash: a54be3a4879ebb2b4e8f880dd14bb50044a0820f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939388"
---
# <span data-ttu-id="9d3bf-101">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="9d3bf-101">Add-AzureRmMetricAlertRule</span></span>

## <span data-ttu-id="9d3bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="9d3bf-103">Bir metrik temelinde bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-103">Adds or updates a metric-based alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d3bf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d3bf-104">SYNTAX</span></span>

```
Add-AzureRmMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d3bf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d3bf-105">DESCRIPTION</span></span>
<span data-ttu-id="9d3bf-106">**Add-AzureRmMetricAlertRule** cmdlet 'i, metrik tabanlı bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-106">The **Add-AzureRmMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="9d3bf-107">Ek kural bir kaynak grubuyla ilişkilendirilir ve bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="9d3bf-108">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9d3bf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d3bf-109">EXAMPLES</span></span>

### <span data-ttu-id="9d3bf-110">Örnek 1: Web sitesine bir metrik uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="9d3bf-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="9d3bf-111">Bu komut Web sitesi için bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="9d3bf-112">Örnek 2: bir kuralı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9d3bf-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzureRMMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="9d3bf-113">Bu komut bir kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-113">This command disables a rule.</span></span>
<span data-ttu-id="9d3bf-114">Kural yoksa devre dışı olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="9d3bf-115">Kural varsa, bunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="9d3bf-116">Örnek 3: eylemlerle kural ekleme</span><span class="sxs-lookup"><span data-stu-id="9d3bf-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzureRmMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="9d3bf-117">Bu komut Web sitesi için bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="9d3bf-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d3bf-118">PARAMETERS</span></span>

### <span data-ttu-id="9d3bf-119">-Eylem</span><span class="sxs-lookup"><span data-stu-id="9d3bf-119">-Action</span></span>
<span data-ttu-id="9d3bf-120">Virgülle ayrılmış bir eylem listesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="9d3bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d3bf-121">-DefaultProfile</span></span>
<span data-ttu-id="9d3bf-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9d3bf-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d3bf-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9d3bf-123">-Description</span></span>
<span data-ttu-id="9d3bf-124">Kuralın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="9d3bf-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="9d3bf-125">-DisableRule</span></span>
<span data-ttu-id="9d3bf-126">Kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-126">Disables the rule.</span></span>
<span data-ttu-id="9d3bf-127">Bu parametreyi belirtmezseniz, kural etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="9d3bf-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="9d3bf-128">-Location</span></span>
<span data-ttu-id="9d3bf-129">Kuralın tanımlandığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="9d3bf-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="9d3bf-130">-MetricName</span></span>
<span data-ttu-id="9d3bf-131">Kuralın izlenme ölçümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="9d3bf-132">Bu parametreyi yalnızca metrik tabanlı kurallar için belirtin.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="9d3bf-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="9d3bf-133">-Name</span></span>
<span data-ttu-id="9d3bf-134">Kuralın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="9d3bf-135">-İşleç</span><span class="sxs-lookup"><span data-stu-id="9d3bf-135">-Operator</span></span>
<span data-ttu-id="9d3bf-136">Kural koşulunun ilişkisel işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="9d3bf-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9d3bf-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9d3bf-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="9d3bf-138">GreaterThan</span></span>
- <span data-ttu-id="9d3bf-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="9d3bf-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="9d3bf-140">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="9d3bf-140">LessThan</span></span>
- <span data-ttu-id="9d3bf-141">Gezi Bayramı</span><span class="sxs-lookup"><span data-stu-id="9d3bf-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="9d3bf-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d3bf-142">-ResourceGroupName</span></span>
<span data-ttu-id="9d3bf-143">Kuralın kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-143">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d3bf-144">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="9d3bf-144">-TargetResourceId</span></span>
<span data-ttu-id="9d3bf-145">Kuralın izlenme kaynağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="9d3bf-146">Not: var olan bir uyarı kuralı için bu özellik güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="9d3bf-147">Eşiği</span><span class="sxs-lookup"><span data-stu-id="9d3bf-147">-Threshold</span></span>
<span data-ttu-id="9d3bf-148">Kuralın eşiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="9d3bf-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="9d3bf-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="9d3bf-150">Kural değerlendirilirken zaman penceresine uygulanacak toplama işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="9d3bf-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="9d3bf-151">-WindowSize</span></span>
<span data-ttu-id="9d3bf-152">Kuralın verilerinin hesaplanması için zaman penceresi boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="9d3bf-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="9d3bf-153">-Confirm</span></span>
<span data-ttu-id="9d3bf-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d3bf-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d3bf-155">-WhatIf</span></span>
<span data-ttu-id="9d3bf-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d3bf-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d3bf-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d3bf-158">CommonParameters</span></span>
<span data-ttu-id="9d3bf-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d3bf-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d3bf-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d3bf-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d3bf-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d3bf-161">INPUTS</span></span>

### <span data-ttu-id="9d3bf-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="9d3bf-162">System.TimeSpan</span></span>

### <span data-ttu-id="9d3bf-163">Microsoft. Azure. Management. Monitor. Management. modeller. Conditionişleci</span><span class="sxs-lookup"><span data-stu-id="9d3bf-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="9d3bf-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="9d3bf-164">System.Double</span></span>

### <span data-ttu-id="9d3bf-165">System. String</span><span class="sxs-lookup"><span data-stu-id="9d3bf-165">System.String</span></span>

### <span data-ttu-id="9d3bf-166">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. TimeAggregationOperator, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9d3bf-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9d3bf-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9d3bf-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9d3bf-168">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. RuleAction, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9d3bf-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9d3bf-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d3bf-169">OUTPUTS</span></span>

### <span data-ttu-id="9d3bf-170">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9d3bf-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="9d3bf-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d3bf-171">NOTES</span></span>

## <span data-ttu-id="9d3bf-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d3bf-172">RELATED LINKS</span></span>

[<span data-ttu-id="9d3bf-173">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9d3bf-173">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9d3bf-174">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="9d3bf-174">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="9d3bf-175">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="9d3bf-175">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="9d3bf-176">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="9d3bf-176">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)

[<span data-ttu-id="9d3bf-177">Yeni-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="9d3bf-177">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="9d3bf-178">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="9d3bf-178">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)

[<span data-ttu-id="9d3bf-179">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="9d3bf-179">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


