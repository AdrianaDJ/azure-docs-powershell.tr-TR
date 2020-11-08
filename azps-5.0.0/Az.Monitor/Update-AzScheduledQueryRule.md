---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280027"
---
# <span data-ttu-id="c1cb5-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="c1cb5-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="c1cb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="c1cb5-103">Günlük uyarısı kuralını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c1cb5-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="c1cb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1cb5-104">SYNTAX</span></span>

### <span data-ttu-id="c1cb5-105">ByRuleName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c1cb5-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1cb5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c1cb5-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1cb5-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="c1cb5-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1cb5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1cb5-108">DESCRIPTION</span></span>
<span data-ttu-id="c1cb5-109">Bu komut yalnızca "etkin" özelliğini güncelleştiren bir günlük uyarısı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c1cb5-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="c1cb5-110">Diğer özellikleri güncelleştirmek için [set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) komutunu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="c1cb5-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="c1cb5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1cb5-111">EXAMPLES</span></span>

### <span data-ttu-id="c1cb5-112">Örnek 1: kural adına göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c1cb5-112">Example 1: Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
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

### <span data-ttu-id="c1cb5-113">Örnek 2: giriş nesnesine göre güncelleştir</span><span class="sxs-lookup"><span data-stu-id="c1cb5-113">Example 2: Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
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

### <span data-ttu-id="c1cb5-114">Örnek 3: kaynak kimliğiyle güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c1cb5-114">Example 3: Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
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

## <span data-ttu-id="c1cb5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1cb5-115">PARAMETERS</span></span>

### <span data-ttu-id="c1cb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1cb5-116">-DefaultProfile</span></span>
<span data-ttu-id="c1cb5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c1cb5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1cb5-118">Özellikli</span><span class="sxs-lookup"><span data-stu-id="c1cb5-118">-Enabled</span></span>
<span data-ttu-id="c1cb5-119">Azure uyarı durumu-geçerli değerler-$true, $false</span><span class="sxs-lookup"><span data-stu-id="c1cb5-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1cb5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1cb5-120">-InputObject</span></span>
<span data-ttu-id="c1cb5-121">Zamanlanmış sorgu kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="c1cb5-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="c1cb5-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c1cb5-122">-Name</span></span>
<span data-ttu-id="c1cb5-123">Uyarı adı</span><span class="sxs-lookup"><span data-stu-id="c1cb5-123">The alert name</span></span>

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

### <span data-ttu-id="c1cb5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1cb5-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1cb5-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c1cb5-125">The resource group name</span></span>

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

### <span data-ttu-id="c1cb5-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c1cb5-126">-ResourceId</span></span>
<span data-ttu-id="c1cb5-127">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c1cb5-127">The resource Id</span></span>

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

### <span data-ttu-id="c1cb5-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c1cb5-128">-Confirm</span></span>
<span data-ttu-id="c1cb5-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c1cb5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1cb5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1cb5-130">-WhatIf</span></span>
<span data-ttu-id="c1cb5-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c1cb5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1cb5-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c1cb5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1cb5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1cb5-133">CommonParameters</span></span>
<span data-ttu-id="c1cb5-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1cb5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1cb5-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c1cb5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1cb5-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1cb5-136">INPUTS</span></span>

### <span data-ttu-id="c1cb5-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="c1cb5-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="c1cb5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c1cb5-138">System.String</span></span>

## <span data-ttu-id="c1cb5-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1cb5-139">OUTPUTS</span></span>

### <span data-ttu-id="c1cb5-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="c1cb5-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="c1cb5-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1cb5-141">NOTES</span></span>

## <span data-ttu-id="c1cb5-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1cb5-142">RELATED LINKS</span></span>
