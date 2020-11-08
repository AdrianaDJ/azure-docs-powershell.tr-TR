---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzScheduledQueryRule.md
ms.openlocfilehash: 5cee29c5141a9fa5cce1af93f7c3ec1de487ffec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108998"
---
# <span data-ttu-id="f0a5e-101">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f0a5e-101">Get-AzScheduledQueryRule</span></span>

## <span data-ttu-id="f0a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a5e-103">Zamanlanmış sorgu kaynaklarını alır</span><span class="sxs-lookup"><span data-stu-id="f0a5e-103">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="f0a5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0a5e-104">SYNTAX</span></span>

### <span data-ttu-id="f0a5e-105">BySubscriptionOrResourceGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0a5e-105">BySubscriptionOrResourceGroup (Default)</span></span>
```
Get-AzScheduledQueryRule [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0a5e-106">ByRuleName</span><span class="sxs-lookup"><span data-stu-id="f0a5e-106">ByRuleName</span></span>
```
Get-AzScheduledQueryRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0a5e-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f0a5e-107">ByResourceId</span></span>
```
Get-AzScheduledQueryRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0a5e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0a5e-108">DESCRIPTION</span></span>
<span data-ttu-id="f0a5e-109">Zamanlanmış sorgu kaynaklarını alır</span><span class="sxs-lookup"><span data-stu-id="f0a5e-109">Gets Scheduled Query Resources</span></span>

## <span data-ttu-id="f0a5e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0a5e-110">EXAMPLES</span></span>

### <span data-ttu-id="f0a5e-111">Örnek 1: aboneliğe veya kaynak grubuna göre liste</span><span class="sxs-lookup"><span data-stu-id="f0a5e-111">Example 1: List by subscription or resource group</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup"

Description       : description 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}

Description       : description 2
Enabled           : true
LastUpdatedTime   : 15-Apr-19 6:57:00 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.Action
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule2
Name              : LogAlertRule2
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="f0a5e-112">Örnek 2: kural adına göre alma</span><span class="sxs-lookup"><span data-stu-id="f0a5e-112">Example 2: Get by rule name</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
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

### <span data-ttu-id="f0a5e-113">Örnek 3: kaynak kimliğiyle al</span><span class="sxs-lookup"><span data-stu-id="f0a5e-113">Example 3: Get by resource Id</span></span>
```powershell
PS C:\> Get-AzScheduledQueryRule -ResourceId "/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1"

Description       : desc 1
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:29:39 PM
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

## <span data-ttu-id="f0a5e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0a5e-114">PARAMETERS</span></span>

### <span data-ttu-id="f0a5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a5e-115">-DefaultProfile</span></span>
<span data-ttu-id="f0a5e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0a5e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0a5e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0a5e-117">-Name</span></span>
<span data-ttu-id="f0a5e-118">Uyarı kuralı adı</span><span class="sxs-lookup"><span data-stu-id="f0a5e-118">The alert rule name</span></span>

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

### <span data-ttu-id="f0a5e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0a5e-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0a5e-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f0a5e-120">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="f0a5e-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f0a5e-121">-ResourceId</span></span>
<span data-ttu-id="f0a5e-122">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f0a5e-122">The resource Id</span></span>

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

### <span data-ttu-id="f0a5e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a5e-123">CommonParameters</span></span>
<span data-ttu-id="f0a5e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0a5e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a5e-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f0a5e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a5e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0a5e-126">INPUTS</span></span>

### <span data-ttu-id="f0a5e-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f0a5e-127">None</span></span>

## <span data-ttu-id="f0a5e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0a5e-128">OUTPUTS</span></span>

### <span data-ttu-id="f0a5e-129">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="f0a5e-129">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="f0a5e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0a5e-130">NOTES</span></span>

## <span data-ttu-id="f0a5e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0a5e-131">RELATED LINKS</span></span>
