---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A90564B5-57D7-48EB-976D-38C03D930289
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRule.md
ms.openlocfilehash: ed5649ead1c0e043ed3d97cb957d6b405967f450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915715"
---
# <span data-ttu-id="ac663-101">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ac663-101">Add-AzMetricAlertRule</span></span>

## <span data-ttu-id="ac663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac663-102">SYNOPSIS</span></span>
<span data-ttu-id="ac663-103">Bir metrik temelinde bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ac663-103">Adds or updates a metric-based alert rule.</span></span>

## <span data-ttu-id="ac663-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac663-104">SYNTAX</span></span>

```
Add-AzMetricAlertRule -WindowSize <TimeSpan> -Operator <ConditionOperator> -Threshold <Double>
 -TargetResourceId <String> -MetricName <String> -TimeAggregationOperator <TimeAggregationOperator>
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac663-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac663-105">DESCRIPTION</span></span>
<span data-ttu-id="ac663-106">**Add-AzMetricAlertRule** cmdlet 'i, metrik tabanlı bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ac663-106">The **Add-AzMetricAlertRule** cmdlet adds or updates a metric-based alert rule.</span></span>
<span data-ttu-id="ac663-107">Ek kural bir kaynak grubuyla ilişkilendirilir ve bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="ac663-107">The added rule is associated with a resource group and has a name.</span></span>
<span data-ttu-id="ac663-108">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="ac663-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="ac663-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac663-109">EXAMPLES</span></span>

### <span data-ttu-id="ac663-110">Örnek 1: Web sitesine bir metrik uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="ac663-110">Example 1: Add a metric alert rule to a website</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -Description "Pura Vida" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
33574ccf-0b01-43b4-aa97-87e6bbcf1c11                                                                         Created
```

<span data-ttu-id="ac663-111">Bu komut Web sitesi için bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac663-111">This command creates a metric alert rule for a website.</span></span>

### <span data-ttu-id="ac663-112">Örnek 2: bir kuralı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="ac663-112">Example 2: Disable a rule</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup Default-Web-EastUS -Operator GreaterThan -Threshold 2 -WindowSize 00:05:00 -MetricName "Requests" -TimeAggregationOperator Total 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
96c489f1-8529-46e1-a76d-2c1463ca3116                                                                                 OK
```

<span data-ttu-id="ac663-113">Bu komut bir kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ac663-113">This command disables a rule.</span></span>
<span data-ttu-id="ac663-114">Kural yoksa devre dışı olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac663-114">If the rule does not exist, it creates it disabled.</span></span>
<span data-ttu-id="ac663-115">Kural varsa, bunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ac663-115">If the rule exists, then it just disables it.</span></span>

### <span data-ttu-id="ac663-116">Örnek 3: eylemlerle kural ekleme</span><span class="sxs-lookup"><span data-stu-id="ac663-116">Example 3: Add a rule with actions</span></span>
```
PS C:\>Add-AzMetricAlertRule -Name "metricRule5" -Location "East US" -ResourceGroup "Default-Web-EastUS" -Operator GreaterThan -Threshold 1 -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -MetricName "Requests" -TimeAggregationOperator Total
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="ac663-117">Bu komut Web sitesi için bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac663-117">This command creates a metric alert rule for a website.</span></span>

## <span data-ttu-id="ac663-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac663-118">PARAMETERS</span></span>

### <span data-ttu-id="ac663-119">-Eylem</span><span class="sxs-lookup"><span data-stu-id="ac663-119">-Action</span></span>
<span data-ttu-id="ac663-120">Virgülle ayrılmış bir eylem listesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-120">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="ac663-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac663-121">-DefaultProfile</span></span>
<span data-ttu-id="ac663-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ac663-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac663-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ac663-123">-Description</span></span>
<span data-ttu-id="ac663-124">Kuralın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-124">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="ac663-125">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="ac663-125">-DisableRule</span></span>
<span data-ttu-id="ac663-126">Kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="ac663-126">Disables the rule.</span></span>
<span data-ttu-id="ac663-127">Bu parametreyi belirtmezseniz, kural etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac663-127">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="ac663-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="ac663-128">-Location</span></span>
<span data-ttu-id="ac663-129">Kuralın tanımlandığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-129">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="ac663-130">-MetricName</span><span class="sxs-lookup"><span data-stu-id="ac663-130">-MetricName</span></span>
<span data-ttu-id="ac663-131">Kuralın izlenme ölçümünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-131">Specifies the name of the metric the rule is monitoring.</span></span>
<span data-ttu-id="ac663-132">Bu parametreyi yalnızca metrik tabanlı kurallar için belirtin.</span><span class="sxs-lookup"><span data-stu-id="ac663-132">Specify this parameter only for metric-based rules.</span></span>

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

### <span data-ttu-id="ac663-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="ac663-133">-Name</span></span>
<span data-ttu-id="ac663-134">Kuralın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-134">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="ac663-135">-İşleç</span><span class="sxs-lookup"><span data-stu-id="ac663-135">-Operator</span></span>
<span data-ttu-id="ac663-136">Kural koşulunun ilişkisel işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-136">Specifies the relational operator for the condition of the rule.</span></span>
<span data-ttu-id="ac663-137">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ac663-137">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ac663-138">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="ac663-138">GreaterThan</span></span>
- <span data-ttu-id="ac663-139">GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="ac663-139">GreaterThanOrEqual</span></span>
-  <span data-ttu-id="ac663-140">Küçüktür</span><span class="sxs-lookup"><span data-stu-id="ac663-140">LessThan</span></span>
- <span data-ttu-id="ac663-141">Gezi Bayramı</span><span class="sxs-lookup"><span data-stu-id="ac663-141">LessThanOrEqual</span></span>

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

### <span data-ttu-id="ac663-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac663-142">-ResourceGroupName</span></span>
<span data-ttu-id="ac663-143">Kuralın kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-143">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="ac663-144">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="ac663-144">-TargetResourceId</span></span>
<span data-ttu-id="ac663-145">Kuralın izlenme kaynağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-145">Specifies the ID of the resource the rule is monitoring.</span></span> <span data-ttu-id="ac663-146">Not: var olan bir uyarı kuralı için bu özellik güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="ac663-146">NOTE: This property cannot be updated for an existing alert rule.</span></span>

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

### <span data-ttu-id="ac663-147">Eşiği</span><span class="sxs-lookup"><span data-stu-id="ac663-147">-Threshold</span></span>
<span data-ttu-id="ac663-148">Kuralın eşiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-148">Specifies the threshold of the rule.</span></span>

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

### <span data-ttu-id="ac663-149">-TimeAggregationOperator</span><span class="sxs-lookup"><span data-stu-id="ac663-149">-TimeAggregationOperator</span></span>
<span data-ttu-id="ac663-150">Kural değerlendirilirken zaman penceresine uygulanacak toplama işlecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-150">Specifies the aggregation operator to apply to the time window when the rule is being evaluated.</span></span>

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

### <span data-ttu-id="ac663-151">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="ac663-151">-WindowSize</span></span>
<span data-ttu-id="ac663-152">Kuralın verilerinin hesaplanması için zaman penceresi boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac663-152">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="ac663-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="ac663-153">-Confirm</span></span>
<span data-ttu-id="ac663-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ac663-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac663-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac663-155">-WhatIf</span></span>
<span data-ttu-id="ac663-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac663-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac663-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ac663-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac663-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac663-158">CommonParameters</span></span>
<span data-ttu-id="ac663-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac663-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac663-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac663-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac663-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac663-161">INPUTS</span></span>

### <span data-ttu-id="ac663-162">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="ac663-162">System.TimeSpan</span></span>

### <span data-ttu-id="ac663-163">Microsoft. Azure. Management. Monitor. Management. modeller. Conditionişleci</span><span class="sxs-lookup"><span data-stu-id="ac663-163">Microsoft.Azure.Management.Monitor.Management.Models.ConditionOperator</span></span>

### <span data-ttu-id="ac663-164">System. Double</span><span class="sxs-lookup"><span data-stu-id="ac663-164">System.Double</span></span>

### <span data-ttu-id="ac663-165">System. String</span><span class="sxs-lookup"><span data-stu-id="ac663-165">System.String</span></span>

### <span data-ttu-id="ac663-166">System. Nullable ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. TimeAggregationOperator, Microsoft. Azure. PowerShell. cmdlet. Monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ac663-166">System.Nullable\`1[[Microsoft.Azure.Management.Monitor.Management.Models.TimeAggregationOperator, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ac663-167">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ac663-167">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ac663-168">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. RuleAction, Microsoft. Azure. PowerShell. cmdlet. Monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ac663-168">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ac663-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac663-169">OUTPUTS</span></span>

### <span data-ttu-id="ac663-170">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ac663-170">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="ac663-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac663-171">NOTES</span></span>

## <span data-ttu-id="ac663-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac663-172">RELATED LINKS</span></span>

[<span data-ttu-id="ac663-173">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="ac663-173">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="ac663-174">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ac663-174">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="ac663-175">Get-Azalera</span><span class="sxs-lookup"><span data-stu-id="ac663-175">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="ac663-176">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="ac663-176">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)

[<span data-ttu-id="ac663-177">Yeni-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="ac663-177">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="ac663-178">Yeni-Azalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="ac663-178">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)

[<span data-ttu-id="ac663-179">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="ac663-179">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)

