---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 142f1984b875b9ee298063708d654b97d7401fc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108188"
---
# <span data-ttu-id="55569-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="55569-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="55569-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55569-102">SYNOPSIS</span></span>
<span data-ttu-id="55569-103">V2 (klasik olmayan) ölçüm tabanlı bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="55569-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="55569-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55569-104">SYNTAX</span></span>

### <span data-ttu-id="55569-105">Wınalertbyresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55569-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="55569-106">Tüm</span><span class="sxs-lookup"><span data-stu-id="55569-106">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-ActionGroup <ActivityLogAlertActionGroup[]>] [-ActionGroupId <String[]>] [-DisableRule]
 [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55569-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55569-107">DESCRIPTION</span></span>
<span data-ttu-id="55569-108">**V2 (klasik olmayan) ölçüm tabanlı bir uyarı kuralı** ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="55569-108">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="55569-109">Ek kural bir kaynak grubuyla ilişkilendirilir ve bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="55569-109">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="55569-110">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="55569-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="55569-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55569-111">EXAMPLES</span></span>

### <span data-ttu-id="55569-112">Örnek 1: sanal makineye bir metrik uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="55569-112">Example 1: Add a metric alert rule to a virtual machine</span></span>

```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name PS3182019 -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1", "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM1,
                       /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/012345/providers/Microsoft.Compute/virtualMachines/VM2}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/PS3182019
Name                 : PS3182019
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="55569-113">Bu komut, sanal makine için bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55569-113">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="55569-114">$condition New-AzMetricAlertRuleV2Criteria cmdlet 'inin çıktıdır ve $act New-AzActionGroup cmdlet 'inin çıktıdır</span><span class="sxs-lookup"><span data-stu-id="55569-114">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="55569-115">Örnek 2: bir abonelikteki tüm sanal makineler için bir metrik uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="55569-115">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
```powershell
PS C:\> Add-AzMetricAlertRuleV2 -Name AllVM -ResourceGroupName xxxxRG -WindowSize 0:5 -Frequency 0:5 -TargetResourceScope "/subscriptions/00000000-0000-0000-0000-0000000" -TargetResourceType "Microsoft.Compute/virtualMachines" -TargetResourceRegion "eastus" -Description "This is description" -Severity 4 -ActionGroup $act -Condition $condition

Description          : This is description
Severity             : 4
Enabled              : True
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   : Microsoft.Compute/virtualMachines
TargetResourceRegion : eastus
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertMultipleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/xxxxRG/providers/Microsoft.Insights/metricAlerts/AllVM
Name                 : AllVM
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="55569-116">Bu komut, abonelikteki tüm sanal makineler için bir eastus</span><span class="sxs-lookup"><span data-stu-id="55569-116">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="55569-117">Örnek 3: ölçü uyarısı kuralını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="55569-117">Example 3: Disable a metric alert rule</span></span>
```powershell
PS C:\>Get-AzMetricAlertRuleV2 -ResourceGroupName alertstest  -Name TestAlertRule | Add-AzMetricAlertRuleV2 -DisableRule
Description          : This new Metric alert rule was created from Powershell version: 1.0.1
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/demo1}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/TestAlertRule
Name                 : TestAlertRule
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="55569-118">Bu komut bir metrik uyarı kuralını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="55569-118">This command disables a metric alert rule.</span></span> <span data-ttu-id="55569-119">Burada, Get-AzMetricAlertRuleV2 çıktısını Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="55569-119">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="55569-120">Örnek 4: boyutlarla bir metrik uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="55569-120">Example 4: Add a metric alert rule with dimensions</span></span>

```powershell
PS C:\>$act = New-AzActionGroup -ActionGroupId "/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo"
PS C:\>$dim1 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/name" -ValuesToInclude "gdtest"
PS C:\>$dim2 = New-AzMetricAlertRuleV2DimensionSelection -DimensionName "availabilityResult/location" -ValuesToInclude "*"
PS C:\>$criteria = New-AzMetricAlertRuleV2Criteria -MetricName "availabilityResults/availabilityPercentage" -DimensionSelection $dim1,$dim2 -TimeAggregation Average -Operator GreaterThan -Threshold 2
PS C:\>Add-AzMetricAlertRuleV2 -Name AlertWithDim -ResourceGroupName alertstest -WindowSize 00:05:00 -Frequency 00:05:00 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction" -Condition $criteria -ActionGroup $act -DisableRule -Severity 4
Description          : This new Metric alert rule was created from Powershell version: 1.0.0
Severity             : 4
Enabled              : False
Scopes               : {/subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/microsoft.insights/components/alertstestFunction}
EvaluationFrequency  : 00:05:00
WindowSize           : 00:05:00
TargetResourceType   :
TargetResourceRegion :
Criteria             : Microsoft.Azure.Management.Monitor.Models.MetricAlertSingleResourceMultipleMetricCriteria
AutoMitigate         :
Actions              : {/subscriptions/00000000-0000-0000-0000-0000000/resourcegroups/default-activitylogalerts/providers/microsoft.insights/actiongroups/actionGroupDemo}
LastUpdatedTime      :
Id                   : /subscriptions/00000000-0000-0000-0000-0000000/resourceGroups/alertstest/providers/Microsoft.Insights/metricAlerts/AlertWithDim
Name                 : AlertWithDim
Type                 : Microsoft.Insights/metricAlerts
Location             : global
Tags                 :
```

<span data-ttu-id="55569-121">Boyut değerlerini seçme veya birden çok ölçüte sahip olanlar gibi daha karmaşık bir metrik uyarı kuralı oluşturmak için New-AzMetricAlertRuleV2DimensionSelection ve yeni-AzMetricAlertRuleV2Criteria yardımcı cmdlet 'lerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55569-121">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="55569-122">Yukarıdaki cmdlet kümesi, boyutlarla birlikte bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55569-122">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="55569-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55569-123">PARAMETERS</span></span>

### <span data-ttu-id="55569-124">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="55569-124">-ActionGroup</span></span>
<span data-ttu-id="55569-125">Kuralın eylem grubu</span><span class="sxs-lookup"><span data-stu-id="55569-125">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-126">-Actiongroupıd</span><span class="sxs-lookup"><span data-stu-id="55569-126">-ActionGroupId</span></span>
<span data-ttu-id="55569-127">Kuralın eylem grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="55569-127">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-128">-Koşul</span><span class="sxs-lookup"><span data-stu-id="55569-128">-Condition</span></span>
<span data-ttu-id="55569-129">Kural koşulu</span><span class="sxs-lookup"><span data-stu-id="55569-129">The condition for rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]
Parameter Sets: (All)
Aliases: Criteria

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55569-130">-DefaultProfile</span></span>
<span data-ttu-id="55569-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55569-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55569-132">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="55569-132">-Description</span></span>
<span data-ttu-id="55569-133">Ölçü uyarısı kuralının açıklaması</span><span class="sxs-lookup"><span data-stu-id="55569-133">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="55569-134">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="55569-134">-DisableRule</span></span>
<span data-ttu-id="55569-135">Kuralı devre dışı bırak (durum) bayrağı</span><span class="sxs-lookup"><span data-stu-id="55569-135">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="55569-136">Frekans</span><span class="sxs-lookup"><span data-stu-id="55569-136">-Frequency</span></span>
<span data-ttu-id="55569-137">Kuralın değerlendirme sıklığı</span><span class="sxs-lookup"><span data-stu-id="55569-137">The evaluation frequency for rule</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: EvaluationFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="55569-138">-Name</span></span>
<span data-ttu-id="55569-139">Ölçü uyarısı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="55569-139">The name of metric alert rule</span></span>

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

### <span data-ttu-id="55569-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55569-140">-ResourceGroupName</span></span>
<span data-ttu-id="55569-141">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="55569-141">The Resource Group Name</span></span>

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

### <span data-ttu-id="55569-142">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="55569-142">-Severity</span></span>
<span data-ttu-id="55569-143">Ölçü uyarısı kuralının önem derecesi</span><span class="sxs-lookup"><span data-stu-id="55569-143">The severity for the metric alert rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-144">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="55569-144">-TargetResourceId</span></span>
<span data-ttu-id="55569-145">Kuralın hedef kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="55569-145">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-146">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="55569-146">-TargetResourceRegion</span></span>
<span data-ttu-id="55569-147">Kuralın hedef kaynak bölgesi</span><span class="sxs-lookup"><span data-stu-id="55569-147">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-148">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="55569-148">-TargetResourceScope</span></span>
<span data-ttu-id="55569-149">Kural için hedef kaynak kapsamı</span><span class="sxs-lookup"><span data-stu-id="55569-149">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-150">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="55569-150">-TargetResourceType</span></span>
<span data-ttu-id="55569-151">Kural için hedef kaynak türü</span><span class="sxs-lookup"><span data-stu-id="55569-151">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55569-152">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="55569-152">-WindowSize</span></span>
<span data-ttu-id="55569-153">Kural için pencere boyutu</span><span class="sxs-lookup"><span data-stu-id="55569-153">The window size for rule</span></span>

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

### <span data-ttu-id="55569-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="55569-154">-Confirm</span></span>
<span data-ttu-id="55569-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55569-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55569-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55569-156">-WhatIf</span></span>
<span data-ttu-id="55569-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55569-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55569-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55569-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55569-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55569-159">CommonParameters</span></span>
<span data-ttu-id="55569-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55569-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55569-161">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55569-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55569-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55569-162">INPUTS</span></span>

### <span data-ttu-id="55569-163">System. String</span><span class="sxs-lookup"><span data-stu-id="55569-163">System.String</span></span>

### <span data-ttu-id="55569-164">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="55569-164">System.TimeSpan</span></span>

### <span data-ttu-id="55569-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="55569-165">System.String[]</span></span>

### <span data-ttu-id="55569-166">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. ıpsmulw32, Microsoft. Azure.</span><span class="sxs-lookup"><span data-stu-id="55569-166">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="55569-167">Microsoft. Azure. Management. Monitor. modeller. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="55569-167">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="55569-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55569-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="55569-169">System. Int32</span><span class="sxs-lookup"><span data-stu-id="55569-169">System.Int32</span></span>

## <span data-ttu-id="55569-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55569-170">OUTPUTS</span></span>

### <span data-ttu-id="55569-171">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="55569-171">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="55569-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55569-172">NOTES</span></span>

## <span data-ttu-id="55569-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55569-173">RELATED LINKS</span></span>
