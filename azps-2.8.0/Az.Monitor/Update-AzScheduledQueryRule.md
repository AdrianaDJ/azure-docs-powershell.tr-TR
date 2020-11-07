---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 0a2214abfd6e48dc96ad675610a85a0ec7e8e5fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932145"
---
# <span data-ttu-id="5f700-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="5f700-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="5f700-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f700-102">SYNOPSIS</span></span>
<span data-ttu-id="5f700-103">Günlük uyarısı kuralını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="5f700-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="5f700-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f700-104">SYNTAX</span></span>

### <span data-ttu-id="5f700-105">ByRuleName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5f700-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f700-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f700-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f700-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="5f700-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f700-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f700-108">DESCRIPTION</span></span>
<span data-ttu-id="5f700-109">Bu komut yalnızca "etkin" özelliğini güncelleştiren bir günlük uyarısı kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5f700-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="5f700-110">Diğer özellikleri güncelleştirmek için, bkz: "set-AzScheduledQueryRule" komutu.</span><span class="sxs-lookup"><span data-stu-id="5f700-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="5f700-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f700-111">EXAMPLES</span></span>

### <span data-ttu-id="5f700-112">Örnek 1-kural adına göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5f700-112">Example 1 - Update by rule name</span></span>
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

### <span data-ttu-id="5f700-113">Örnek 2-giriş nesnesine göre güncelleştir</span><span class="sxs-lookup"><span data-stu-id="5f700-113">Example 2 - Update by input object</span></span>
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

### <span data-ttu-id="5f700-114">Örnek 3-kaynak koduna göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5f700-114">Example 3 - Update by resource Id</span></span>
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

## <span data-ttu-id="5f700-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f700-115">PARAMETERS</span></span>

### <span data-ttu-id="5f700-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f700-116">-DefaultProfile</span></span>
<span data-ttu-id="5f700-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f700-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f700-118">Özellikli</span><span class="sxs-lookup"><span data-stu-id="5f700-118">-Enabled</span></span>
<span data-ttu-id="5f700-119">Azure uyarı durumu-geçerli değerler-$true, $false</span><span class="sxs-lookup"><span data-stu-id="5f700-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="5f700-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f700-120">-InputObject</span></span>
<span data-ttu-id="5f700-121">Zamanlanmış sorgu kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="5f700-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="5f700-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="5f700-122">-Name</span></span>
<span data-ttu-id="5f700-123">Uyarı adı</span><span class="sxs-lookup"><span data-stu-id="5f700-123">The alert name</span></span>

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

### <span data-ttu-id="5f700-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f700-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f700-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5f700-125">The resource group name</span></span>

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

### <span data-ttu-id="5f700-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5f700-126">-ResourceId</span></span>
<span data-ttu-id="5f700-127">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="5f700-127">The resource Id</span></span>

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

### <span data-ttu-id="5f700-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f700-128">-Confirm</span></span>
<span data-ttu-id="5f700-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f700-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f700-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f700-130">-WhatIf</span></span>
<span data-ttu-id="5f700-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f700-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f700-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f700-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f700-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f700-133">CommonParameters</span></span>
<span data-ttu-id="5f700-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f700-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f700-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f700-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f700-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f700-136">INPUTS</span></span>

### <span data-ttu-id="5f700-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="5f700-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="5f700-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5f700-138">System.String</span></span>

## <span data-ttu-id="5f700-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f700-139">OUTPUTS</span></span>

### <span data-ttu-id="5f700-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="5f700-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="5f700-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f700-141">NOTES</span></span>

## <span data-ttu-id="5f700-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f700-142">RELATED LINKS</span></span>
