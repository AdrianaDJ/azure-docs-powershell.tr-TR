---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 92ef4802ce842fa88389da19f1b5ba1aacf84b3e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759851"
---
# <span data-ttu-id="04930-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="04930-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="04930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04930-102">SYNOPSIS</span></span>
<span data-ttu-id="04930-103">Günlükleri belirli Application-Insights uygulamasından toplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04930-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="04930-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04930-104">SYNTAX</span></span>

### <span data-ttu-id="04930-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04930-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04930-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="04930-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04930-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="04930-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04930-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="04930-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04930-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="04930-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04930-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="04930-110">DESCRIPTION</span></span>
<span data-ttu-id="04930-111">**New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet 'i, belirli bir Application-Insights uygulamasının günlüklerinin koleksiyonunu etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="04930-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="04930-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04930-112">EXAMPLES</span></span>

### <span data-ttu-id="04930-113">Örnek 1: çalışma alanında Application-Insights veri kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="04930-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="04930-114">Bu komut, belirli bir günlük Analizi Workpsace içinde belirli bir uygulamanın Application-Insights veri kaynağını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04930-114">This command creates an application-insights data source of a given application in a given log analytics workpsace.</span></span> <span data-ttu-id="04930-115">Bu işlem, verilen uygulamadaki günlük koleksiyonunun Log Analytics Workpsace.</span><span class="sxs-lookup"><span data-stu-id="04930-115">This enables the collection of logs from given application to the log analytics workpsace.</span></span>

### <span data-ttu-id="04930-116">Örnek 2: uygulama kaynak kimliği tarafından çalışma alanı nesnesini alma ve uygulama Insights veri kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="04930-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="04930-117">Bu komut, Log Analytics çalışma alanı nesnesinin alınacağını ve uygulama kaynak kimliği tarafından ilişkili bir uygulama-Öngörüler veri kaynağı oluşturmak için çıktıyı geçirmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="04930-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="04930-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04930-118">PARAMETERS</span></span>

### <span data-ttu-id="04930-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="04930-119">-ApplicationName</span></span>
<span data-ttu-id="04930-120">Bağlantılı uygulamanın adı.</span><span class="sxs-lookup"><span data-stu-id="04930-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04930-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04930-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="04930-122">Bağlantılı uygulamanın kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="04930-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04930-123">-Applicationresourceıd</span><span class="sxs-lookup"><span data-stu-id="04930-123">-ApplicationResourceId</span></span>
<span data-ttu-id="04930-124">Bağlantılı uygulama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="04930-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04930-125">-Applicationsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="04930-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="04930-126">Bağlantılı uygulamanın abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="04930-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04930-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04930-127">-DefaultProfile</span></span>
<span data-ttu-id="04930-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04930-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04930-129">-Force</span><span class="sxs-lookup"><span data-stu-id="04930-129">-Force</span></span>
<span data-ttu-id="04930-130">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="04930-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="04930-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04930-131">-ResourceGroupName</span></span>
<span data-ttu-id="04930-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="04930-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04930-133">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="04930-133">-Workspace</span></span>
<span data-ttu-id="04930-134">Veri kaynağını içerecek çalışma alanı.</span><span class="sxs-lookup"><span data-stu-id="04930-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04930-135">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="04930-135">-WorkspaceName</span></span>
<span data-ttu-id="04930-136">Veri kaynağını içerecek çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="04930-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04930-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="04930-137">-Confirm</span></span>
<span data-ttu-id="04930-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04930-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04930-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04930-139">-WhatIf</span></span>
<span data-ttu-id="04930-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04930-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04930-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04930-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04930-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04930-142">CommonParameters</span></span>
<span data-ttu-id="04930-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04930-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04930-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04930-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04930-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04930-145">INPUTS</span></span>

### <span data-ttu-id="04930-146">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="04930-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="04930-147">System. String</span><span class="sxs-lookup"><span data-stu-id="04930-147">System.String</span></span>

## <span data-ttu-id="04930-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04930-148">OUTPUTS</span></span>

### <span data-ttu-id="04930-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="04930-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="04930-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04930-150">NOTES</span></span>

## <span data-ttu-id="04930-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04930-151">RELATED LINKS</span></span>
