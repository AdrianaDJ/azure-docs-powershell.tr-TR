---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azmetricalertrulev2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzMetricAlertRuleV2.md
ms.openlocfilehash: 25854c3432f0ea28ee5eb267013992fce977b06a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94105019"
---
# <span data-ttu-id="55f88-101">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="55f88-101">Add-AzMetricAlertRuleV2</span></span>

## <span data-ttu-id="55f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55f88-102">SYNOPSIS</span></span>
<span data-ttu-id="55f88-103">V2 (klasik olmayan) ölçüm tabanlı bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="55f88-103">Adds or updates a V2 (non-classic) metric-based alert rule.</span></span>

## <span data-ttu-id="55f88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55f88-104">SYNTAX</span></span>

### <span data-ttu-id="55f88-105">Wınalertbyresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55f88-105">CreateAlertByResourceId (Default)</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f88-106">Createalertbyresourceıdandactiongroup</span><span class="sxs-lookup"><span data-stu-id="55f88-106">CreateAlertByResourceIdAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f88-107">Createalertbyresourceıdandactiongroupıd</span><span class="sxs-lookup"><span data-stu-id="55f88-107">CreateAlertByResourceIdAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceId <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f88-108">Tüm</span><span class="sxs-lookup"><span data-stu-id="55f88-108">CreateAlertByScopes</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 [-DisableRule] [-Description <String>] -Severity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f88-109">CreateAlertByScopesAndActionGroup</span><span class="sxs-lookup"><span data-stu-id="55f88-109">CreateAlertByScopesAndActionGroup</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroup <ActivityLogAlertActionGroup[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f88-110">Createalertbyscopesandactiongroupıd</span><span class="sxs-lookup"><span data-stu-id="55f88-110">CreateAlertByScopesAndActionGroupId</span></span>
```
Add-AzMetricAlertRuleV2 -Name <String> -ResourceGroupName <String> -WindowSize <TimeSpan> -Frequency <TimeSpan>
 -TargetResourceScope <String[]> -TargetResourceType <String> -TargetResourceRegion <String>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria]>
 -ActionGroupId <String[]> [-DisableRule] [-Description <String>] -Severity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f88-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="55f88-111">DESCRIPTION</span></span>
<span data-ttu-id="55f88-112">**V2 (klasik olmayan) ölçüm tabanlı bir uyarı kuralı** ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="55f88-112">Adds or updates a **V2 (non-classic) metric-based alert rule**.</span></span> <span data-ttu-id="55f88-113">Ek kural bir kaynak grubuyla ilişkilendirilir ve bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="55f88-113">The added rule is associated with a resource group and has a name.</span></span> <span data-ttu-id="55f88-114">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="55f88-114">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="55f88-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55f88-115">EXAMPLES</span></span>

### <span data-ttu-id="55f88-116">Örnek 1: sanal makineye bir metrik uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="55f88-116">Example 1: Add a metric alert rule to a virtual machine</span></span>

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

<span data-ttu-id="55f88-117">Bu komut, sanal makine için bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55f88-117">This command creates a metric alert rule for a virtual machine.</span></span> <span data-ttu-id="55f88-118">$condition New-AzMetricAlertRuleV2Criteria cmdlet 'inin çıktıdır ve $act New-AzActionGroup cmdlet 'inin çıktıdır</span><span class="sxs-lookup"><span data-stu-id="55f88-118">$condition is the output of New-AzMetricAlertRuleV2Criteria cmdlet and $act is the output of New-AzActionGroup cmdlet</span></span>

### <span data-ttu-id="55f88-119">Örnek 2: bir abonelikteki tüm sanal makineler için bir metrik uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="55f88-119">Example 2: Add a metric alert rule for all virtual machines in a subscription</span></span>
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

<span data-ttu-id="55f88-120">Bu komut, abonelikteki tüm sanal makineler için bir eastus</span><span class="sxs-lookup"><span data-stu-id="55f88-120">This command creates a metric alert rule for all virtual machines in the subscription that are in eastus</span></span>

### <span data-ttu-id="55f88-121">Örnek 3: ölçü uyarısı kuralını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="55f88-121">Example 3: Disable a metric alert rule</span></span>
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

<span data-ttu-id="55f88-122">Bu komut bir metrik uyarı kuralını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="55f88-122">This command disables a metric alert rule.</span></span> <span data-ttu-id="55f88-123">Burada, Get-AzMetricAlertRuleV2 çıktısını Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="55f88-123">Here, we are piping output of Get-AzMetricAlertRuleV2 to Add-AzMetricAlertRuleV2</span></span> 

### <span data-ttu-id="55f88-124">Örnek 4: boyutlarla bir metrik uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="55f88-124">Example 4: Add a metric alert rule with dimensions</span></span>

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

<span data-ttu-id="55f88-125">Boyut değerlerini seçme veya birden çok ölçüte sahip olanlar gibi daha karmaşık bir metrik uyarı kuralı oluşturmak için New-AzMetricAlertRuleV2DimensionSelection ve yeni-AzMetricAlertRuleV2Criteria yardımcı cmdlet 'lerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="55f88-125">To create a more complex metric alert rule like the ones that involve selecting dimension values or have multiple criteria, you can use the helper cmdlets New-AzMetricAlertRuleV2DimensionSelection and New-AzMetricAlertRuleV2Criteria.</span></span>

<span data-ttu-id="55f88-126">Yukarıdaki cmdlet kümesi, boyutlarla birlikte bir metrik uyarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55f88-126">Above set of cmdlets will create a metric alert rule with dimensions.</span></span>

## <span data-ttu-id="55f88-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55f88-127">PARAMETERS</span></span>

### <span data-ttu-id="55f88-128">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="55f88-128">-ActionGroup</span></span>
<span data-ttu-id="55f88-129">Kuralın eylem grubu</span><span class="sxs-lookup"><span data-stu-id="55f88-129">The Action Group for rule</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]
Parameter Sets: CreateAlertByResourceIdAndActionGroup, CreateAlertByScopesAndActionGroup
Aliases: Actions

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f88-130">-Actiongroupıd</span><span class="sxs-lookup"><span data-stu-id="55f88-130">-ActionGroupId</span></span>
<span data-ttu-id="55f88-131">Kuralın eylem grubu kimliği</span><span class="sxs-lookup"><span data-stu-id="55f88-131">The Action Group id for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByResourceIdAndActionGroupId, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f88-132">-Koşul</span><span class="sxs-lookup"><span data-stu-id="55f88-132">-Condition</span></span>
<span data-ttu-id="55f88-133">Kural koşulu</span><span class="sxs-lookup"><span data-stu-id="55f88-133">The condition for rule</span></span>

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

### <span data-ttu-id="55f88-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f88-134">-DefaultProfile</span></span>
<span data-ttu-id="55f88-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55f88-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55f88-136">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="55f88-136">-Description</span></span>
<span data-ttu-id="55f88-137">Ölçü uyarısı kuralının açıklaması</span><span class="sxs-lookup"><span data-stu-id="55f88-137">The description of the metric alert rule</span></span>

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

### <span data-ttu-id="55f88-138">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="55f88-138">-DisableRule</span></span>
<span data-ttu-id="55f88-139">Kuralı devre dışı bırak (durum) bayrağı</span><span class="sxs-lookup"><span data-stu-id="55f88-139">The disable rule (status) flag</span></span>

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

### <span data-ttu-id="55f88-140">Frekans</span><span class="sxs-lookup"><span data-stu-id="55f88-140">-Frequency</span></span>
<span data-ttu-id="55f88-141">Kuralın değerlendirme sıklığı</span><span class="sxs-lookup"><span data-stu-id="55f88-141">The evaluation frequency for rule</span></span>

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

### <span data-ttu-id="55f88-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="55f88-142">-Name</span></span>
<span data-ttu-id="55f88-143">Ölçü uyarısı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="55f88-143">The name of metric alert rule</span></span>

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

### <span data-ttu-id="55f88-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f88-144">-ResourceGroupName</span></span>
<span data-ttu-id="55f88-145">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="55f88-145">The Resource Group Name</span></span>

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

### <span data-ttu-id="55f88-146">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="55f88-146">-Severity</span></span>
<span data-ttu-id="55f88-147">Ölçü uyarısı kuralının önem derecesi</span><span class="sxs-lookup"><span data-stu-id="55f88-147">The severity for the metric alert rule</span></span>

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

### <span data-ttu-id="55f88-148">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="55f88-148">-TargetResourceId</span></span>
<span data-ttu-id="55f88-149">Kuralın hedef kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="55f88-149">The target resource id for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByResourceId, CreateAlertByResourceIdAndActionGroup, CreateAlertByResourceIdAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f88-150">-TargetResourceRegion</span><span class="sxs-lookup"><span data-stu-id="55f88-150">-TargetResourceRegion</span></span>
<span data-ttu-id="55f88-151">Kuralın hedef kaynak bölgesi</span><span class="sxs-lookup"><span data-stu-id="55f88-151">The target resource region for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f88-152">-TargetResourceScope</span><span class="sxs-lookup"><span data-stu-id="55f88-152">-TargetResourceScope</span></span>
<span data-ttu-id="55f88-153">Kural için hedef kaynak kapsamı</span><span class="sxs-lookup"><span data-stu-id="55f88-153">The target resource scope for rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases: Scopes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f88-154">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="55f88-154">-TargetResourceType</span></span>
<span data-ttu-id="55f88-155">Kural için hedef kaynak türü</span><span class="sxs-lookup"><span data-stu-id="55f88-155">The target resource type for rule</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAlertByScopes, CreateAlertByScopesAndActionGroup, CreateAlertByScopesAndActionGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f88-156">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="55f88-156">-WindowSize</span></span>
<span data-ttu-id="55f88-157">Kural için pencere boyutu</span><span class="sxs-lookup"><span data-stu-id="55f88-157">The window size for rule</span></span>

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

### <span data-ttu-id="55f88-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="55f88-158">-Confirm</span></span>
<span data-ttu-id="55f88-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55f88-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f88-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f88-160">-WhatIf</span></span>
<span data-ttu-id="55f88-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55f88-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55f88-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55f88-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f88-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f88-163">CommonParameters</span></span>
<span data-ttu-id="55f88-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55f88-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f88-165">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="55f88-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f88-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55f88-166">INPUTS</span></span>

### <span data-ttu-id="55f88-167">System. String</span><span class="sxs-lookup"><span data-stu-id="55f88-167">System.String</span></span>

### <span data-ttu-id="55f88-168">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="55f88-168">System.TimeSpan</span></span>

### <span data-ttu-id="55f88-169">System. String []</span><span class="sxs-lookup"><span data-stu-id="55f88-169">System.String[]</span></span>

### <span data-ttu-id="55f88-170">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. ıpsmulw32, Microsoft. Azure.</span><span class="sxs-lookup"><span data-stu-id="55f88-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.IPSMultiMetricCriteria, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="55f88-171">Microsoft. Azure. Management. Monitor. modeller. ActivityLogAlertActionGroup []</span><span class="sxs-lookup"><span data-stu-id="55f88-171">Microsoft.Azure.Management.Monitor.Models.ActivityLogAlertActionGroup[]</span></span>

### <span data-ttu-id="55f88-172">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55f88-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="55f88-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="55f88-173">System.Int32</span></span>

## <span data-ttu-id="55f88-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55f88-174">OUTPUTS</span></span>

### <span data-ttu-id="55f88-175">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="55f88-175">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricAlertRuleV2</span></span>

## <span data-ttu-id="55f88-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55f88-176">NOTES</span></span>

## <span data-ttu-id="55f88-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55f88-177">RELATED LINKS</span></span>
