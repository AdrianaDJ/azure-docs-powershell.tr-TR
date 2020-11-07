---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: 15b847034300d01df354cc7512305ffd3cab8279
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753657"
---
# <span data-ttu-id="c4842-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="c4842-101">Set-AzActionRule</span></span>

## <span data-ttu-id="c4842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4842-102">SYNOPSIS</span></span>
<span data-ttu-id="c4842-103">Eylem kuralı oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="c4842-103">Create or update an action rule.</span></span>

## <span data-ttu-id="c4842-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4842-104">SYNTAX</span></span>

### <span data-ttu-id="c4842-105">BySimplifiedFormatDiagnosticsActionRule (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4842-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4842-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c4842-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4842-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="c4842-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4842-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="c4842-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4842-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4842-109">DESCRIPTION</span></span>
<span data-ttu-id="c4842-110">**Set-AzActionRule** bir eylem kuralı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c4842-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="c4842-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4842-111">EXAMPLES</span></span>

### <span data-ttu-id="c4842-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4842-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="c4842-113">Bu cmdlet, Supression için bir eylem kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4842-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="c4842-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c4842-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="c4842-115">Bu cmdlet eylem grubu için bir eylem kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4842-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="c4842-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c4842-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="c4842-117">Bu cmdlet Tanılama ayarları için bir eylem kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c4842-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="c4842-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4842-118">PARAMETERS</span></span>

### <span data-ttu-id="c4842-119">-Actiongroupıd</span><span class="sxs-lookup"><span data-stu-id="c4842-119">-ActionGroupId</span></span>
<span data-ttu-id="c4842-120">Bildirilecek eylem grubu kimliği.</span><span class="sxs-lookup"><span data-stu-id="c4842-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="c4842-121">-ActionRuleType</span></span>
<span data-ttu-id="c4842-122">JSON biçiminde eylem kuralı</span><span class="sxs-lookup"><span data-stu-id="c4842-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="c4842-123">-AlertContextCondition</span></span>
<span data-ttu-id="c4842-124">Beklenen biçim \< \> : \< Örneğin, virgülle ayrılmış değerler listesi \> } Örneğin.</span><span class="sxs-lookup"><span data-stu-id="c4842-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c4842-125">İçerir: smartgroups</span><span class="sxs-lookup"><span data-stu-id="c4842-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-126">-Alertruleıdcondition</span><span class="sxs-lookup"><span data-stu-id="c4842-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="c4842-127">Beklenen biçim \< \> : \< Örneğin, virgülle ayrılmış değerler listesi \> } Örneğin.</span><span class="sxs-lookup"><span data-stu-id="c4842-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c4842-128">Eşittir:/abonelikler/ad825170-845c-47dB-8f00-11978947b089/resourceGroups/abvarma/Providers/Microsoft. Insights/metricAlerts/test-MRMC-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="c4842-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4842-129">-DefaultProfile</span></span>
<span data-ttu-id="c4842-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4842-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4842-131">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c4842-131">-Description</span></span>
<span data-ttu-id="c4842-132">Eylem kuralının açıklaması</span><span class="sxs-lookup"><span data-stu-id="c4842-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="c4842-133">-DescriptionCondition</span></span>
<span data-ttu-id="c4842-134">Beklenen biçim \< \> : \< Örneğin, virgülle ayrılmış değerler listesi \> } Örneğin.</span><span class="sxs-lookup"><span data-stu-id="c4842-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c4842-135">İçerir: test uyarısı</span><span class="sxs-lookup"><span data-stu-id="c4842-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4842-136">-InputObject</span></span>
<span data-ttu-id="c4842-137">Eylem kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="c4842-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="c4842-138">-MonitorCondition</span></span>
<span data-ttu-id="c4842-139">Beklenen biçim \< \> : \< Örneğin, virgülle ayrılmış değerler listesi \> } Örneğin.</span><span class="sxs-lookup"><span data-stu-id="c4842-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c4842-140">Notals: çözüldü</span><span class="sxs-lookup"><span data-stu-id="c4842-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="c4842-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="c4842-142">Beklenen biçim \< \> : \< Örneğin, virgülle ayrılmış değerler listesi \> } Örneğin.</span><span class="sxs-lookup"><span data-stu-id="c4842-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c4842-143">Eşittir: platform, Log Analytics</span><span class="sxs-lookup"><span data-stu-id="c4842-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4842-144">-Name</span></span>
<span data-ttu-id="c4842-145">Eylem kuralı adı</span><span class="sxs-lookup"><span data-stu-id="c4842-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="c4842-146">-ReccurenceType</span></span>
<span data-ttu-id="c4842-147">Bastırma uygulanması gereken süreyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4842-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="c4842-148">-ReccurentValue</span></span>
<span data-ttu-id="c4842-149">Varsa, değerleri yeniden toplayın. Haftalık- \[ 1 durumunda, 2 \] aylık- \[ 1, 3, 5, 30 durumunda\]</span><span class="sxs-lookup"><span data-stu-id="c4842-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4842-150">-ResourceGroupName</span></span>
<span data-ttu-id="c4842-151">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c4842-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-152">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="c4842-152">-Scope</span></span>
<span data-ttu-id="c4842-153">Virgülle ayrılmış değerler listesi</span><span class="sxs-lookup"><span data-stu-id="c4842-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="c4842-154">-SeverityCondition</span></span>
<span data-ttu-id="c4842-155">Beklenen biçim \< \> : \< Örneğin, virgülle ayrılmış değerler listesi \> } Örneğin.</span><span class="sxs-lookup"><span data-stu-id="c4842-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c4842-156">Eşittir: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="c4842-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-157">-Durum</span><span class="sxs-lookup"><span data-stu-id="c4842-157">-Status</span></span>
<span data-ttu-id="c4842-158">Eylem kuralının durumu.</span><span class="sxs-lookup"><span data-stu-id="c4842-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-159">-Suppressionbitişsaati</span><span class="sxs-lookup"><span data-stu-id="c4842-159">-SuppressionEndTime</span></span>
<span data-ttu-id="c4842-160">Bitiş zamanı gizmi</span><span class="sxs-lookup"><span data-stu-id="c4842-160">Suppression End Time.</span></span>
<span data-ttu-id="c4842-161">Supression, günlük, haftada bir veya ayda bir kez daha 12/09/2018 06:00:00</span><span class="sxs-lookup"><span data-stu-id="c4842-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="c4842-162">-SuppressionStartTime</span></span>
<span data-ttu-id="c4842-163">Başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="c4842-163">Suppression Start Time.</span></span>
<span data-ttu-id="c4842-164">Supression, günlük, haftada bir veya ayda bir kez daha 12/09/2018 06:00:00</span><span class="sxs-lookup"><span data-stu-id="c4842-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-165">-Targetresourcettypeınfo</span><span class="sxs-lookup"><span data-stu-id="c4842-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="c4842-166">Beklenen biçim \< \> : \< Örneğin, virgülle ayrılmış değerler listesi \> } Örneğin.</span><span class="sxs-lookup"><span data-stu-id="c4842-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="c4842-167">İçerir: sanal makineler, depolama hesabı</span><span class="sxs-lookup"><span data-stu-id="c4842-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4842-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4842-168">-Confirm</span></span>
<span data-ttu-id="c4842-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4842-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4842-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4842-170">-WhatIf</span></span>
<span data-ttu-id="c4842-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4842-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4842-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4842-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4842-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4842-173">CommonParameters</span></span>
<span data-ttu-id="c4842-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4842-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4842-175">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c4842-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4842-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4842-176">INPUTS</span></span>

### <span data-ttu-id="c4842-177">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="c4842-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="c4842-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4842-178">OUTPUTS</span></span>

### <span data-ttu-id="c4842-179">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="c4842-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="c4842-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4842-180">NOTES</span></span>

## <span data-ttu-id="c4842-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4842-181">RELATED LINKS</span></span>
