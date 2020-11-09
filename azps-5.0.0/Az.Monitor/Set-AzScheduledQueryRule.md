---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzScheduledQueryRule.md
ms.openlocfilehash: 0351d6920c4af7f781ef27f4dfbc36a13e0c50cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319869"
---
# <span data-ttu-id="b6559-101">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="b6559-101">Set-AzScheduledQueryRule</span></span>

## <span data-ttu-id="b6559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6559-102">SYNOPSIS</span></span>
<span data-ttu-id="b6559-103">Günlük uyarısı kuralını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="b6559-103">Updates a Log Alert Rule</span></span>

## <span data-ttu-id="b6559-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6559-104">SYNTAX</span></span>

### <span data-ttu-id="b6559-105">ByRuleName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6559-105">ByRuleName (Default)</span></span>
```
Set-AzScheduledQueryRule -Source <PSScheduledQueryRuleSource> [-Schedule <PSScheduledQueryRuleSchedule>]
 -Action <PSScheduledQueryRuleAlertingAction> -Location <String> [-Description <String>] -Name <String>
 -ResourceGroupName <String> [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6559-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b6559-106">ByInputObject</span></span>
```
Set-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-Source <PSScheduledQueryRuleSource>]
 [-Schedule <PSScheduledQueryRuleSchedule>] [-Action <PSScheduledQueryRuleAlertingAction>] [-Location <String>]
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6559-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b6559-107">ByResourceId</span></span>
```
Set-AzScheduledQueryRule -ResourceId <String> -Source <PSScheduledQueryRuleSource>
 [-Schedule <PSScheduledQueryRuleSchedule>] -Action <PSScheduledQueryRuleAlertingAction> -Location <String>
 [-Description <String>] [-Tag <Hashtable>] [-Enabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6559-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6559-108">DESCRIPTION</span></span>
<span data-ttu-id="b6559-109">Yerine koyma semantiği</span><span class="sxs-lookup"><span data-stu-id="b6559-109">Updates a Log Alert Rule by PUT semantics</span></span>

## <span data-ttu-id="b6559-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6559-110">EXAMPLES</span></span>

### <span data-ttu-id="b6559-111">Örnek 1: kural adına göre ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6559-111">Example 1: Set by rule name</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "log alert description" -Schedule $schedule -Source $source

Description       : log alert description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:45:04 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="b6559-112">Örnek 2: giriş nesnesine göre ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6559-112">Example 2: Set by Input Object</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -InputObject $sqr -Description "changed description"

Description       : changed description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:46:38 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="b6559-113">Örnek 3: kaynak kimliğiyle ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6559-113">Example 3: Set by resource Id</span></span>
```powershell
PS C:\> Set-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1" -Enabled $true -Location "centralindia" -Action $alertingAction -Description "change description again" -Schedule $schedule -Source $source

Description       : change description again
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:47:59 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="b6559-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6559-114">PARAMETERS</span></span>

### <span data-ttu-id="b6559-115">-Eylem</span><span class="sxs-lookup"><span data-stu-id="b6559-115">-Action</span></span>
<span data-ttu-id="b6559-116">Zamanlanmış sorgu kuralı uyarısı eylemi</span><span class="sxs-lookup"><span data-stu-id="b6559-116">The scheduled query rule Alerting Action</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="b6559-117">-AsJob</span></span>
<span data-ttu-id="b6559-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b6559-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6559-119">-DefaultProfile</span></span>
<span data-ttu-id="b6559-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b6559-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6559-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="b6559-121">-Description</span></span>
<span data-ttu-id="b6559-122">Bu uyarının açıklaması</span><span class="sxs-lookup"><span data-stu-id="b6559-122">The description for this alert</span></span>

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

### <span data-ttu-id="b6559-123">Özellikli</span><span class="sxs-lookup"><span data-stu-id="b6559-123">-Enabled</span></span>
<span data-ttu-id="b6559-124">Azure uyarı durumu-geçerli değerler-$true, $false</span><span class="sxs-lookup"><span data-stu-id="b6559-124">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6559-125">-InputObject</span></span>
<span data-ttu-id="b6559-126">Zamanlanmış sorgu kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="b6559-126">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="b6559-127">-Location</span></span>
<span data-ttu-id="b6559-128">Bu uyarının konumu</span><span class="sxs-lookup"><span data-stu-id="b6559-128">The location for this alert</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="b6559-129">-Name</span></span>
<span data-ttu-id="b6559-130">Uyarı adı</span><span class="sxs-lookup"><span data-stu-id="b6559-130">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6559-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6559-132">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b6559-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b6559-133">-ResourceId</span></span>
<span data-ttu-id="b6559-134">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b6559-134">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-135">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="b6559-135">-Schedule</span></span>
<span data-ttu-id="b6559-136">Zamanlanmış sorgu kuralı zamanlaması</span><span class="sxs-lookup"><span data-stu-id="b6559-136">The scheduled query rule schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-137">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="b6559-137">-Source</span></span>
<span data-ttu-id="b6559-138">Zamanlanmış sorgu kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="b6559-138">The scheduled query rule source</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByRuleName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b6559-139">-Tag</span></span>
<span data-ttu-id="b6559-140">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="b6559-140">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6559-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="b6559-141">-Confirm</span></span>
<span data-ttu-id="b6559-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b6559-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6559-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6559-143">-WhatIf</span></span>
<span data-ttu-id="b6559-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6559-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6559-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b6559-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6559-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6559-146">CommonParameters</span></span>
<span data-ttu-id="b6559-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6559-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6559-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b6559-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6559-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6559-149">INPUTS</span></span>

### <span data-ttu-id="b6559-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="b6559-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="b6559-151">System. String</span><span class="sxs-lookup"><span data-stu-id="b6559-151">System.String</span></span>

### <span data-ttu-id="b6559-152">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b6559-152">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

### <span data-ttu-id="b6559-153">Microsoft. Azure. Commands. Insights. OutputClasses. Psscheduledqueryrulezamanlama</span><span class="sxs-lookup"><span data-stu-id="b6559-153">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

### <span data-ttu-id="b6559-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="b6559-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAlertingAction</span></span>

## <span data-ttu-id="b6559-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6559-155">OUTPUTS</span></span>

### <span data-ttu-id="b6559-156">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="b6559-156">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="b6559-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6559-157">NOTES</span></span>

## <span data-ttu-id="b6559-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6559-158">RELATED LINKS</span></span>
