---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096121"
---
# <span data-ttu-id="17448-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="17448-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="17448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17448-102">SYNOPSIS</span></span>
<span data-ttu-id="17448-103">Günlükleri belirli Application-Insights uygulamasından toplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17448-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="17448-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17448-104">SYNTAX</span></span>

### <span data-ttu-id="17448-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17448-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17448-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="17448-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17448-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="17448-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17448-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="17448-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17448-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="17448-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17448-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="17448-110">DESCRIPTION</span></span>
<span data-ttu-id="17448-111">**New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet 'i, belirli bir Application-Insights uygulamasının günlüklerinin koleksiyonunu etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="17448-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="17448-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17448-112">EXAMPLES</span></span>

### <span data-ttu-id="17448-113">Örnek 1: çalışma alanında Application-Insights veri kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="17448-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="17448-114">Bu komut, belirli bir günlük Analizi çalışma alanında belirli bir uygulamanın Application-Insights veri kaynağını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17448-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="17448-115">Bu işlem, belirtilen uygulamadaki Günlükler koleksiyonunu Log Analytics çalışma alanına getirir.</span><span class="sxs-lookup"><span data-stu-id="17448-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="17448-116">Örnek 2: uygulama kaynak kimliği tarafından çalışma alanı nesnesini alma ve uygulama Insights veri kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="17448-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="17448-117">Bu komut, Log Analytics çalışma alanı nesnesinin alınacağını ve uygulama kaynak kimliği tarafından ilişkili bir uygulama-Öngörüler veri kaynağı oluşturmak için çıktıyı geçirmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="17448-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="17448-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17448-118">PARAMETERS</span></span>

### <span data-ttu-id="17448-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="17448-119">-ApplicationName</span></span>
<span data-ttu-id="17448-120">Bağlantılı uygulamanın adı.</span><span class="sxs-lookup"><span data-stu-id="17448-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="17448-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17448-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="17448-122">Bağlantılı uygulamanın kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="17448-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="17448-123">-Applicationresourceıd</span><span class="sxs-lookup"><span data-stu-id="17448-123">-ApplicationResourceId</span></span>
<span data-ttu-id="17448-124">Bağlantılı uygulama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="17448-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="17448-125">-Applicationsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="17448-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="17448-126">Bağlantılı uygulamanın abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="17448-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="17448-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17448-127">-DefaultProfile</span></span>
<span data-ttu-id="17448-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17448-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17448-129">-Force</span><span class="sxs-lookup"><span data-stu-id="17448-129">-Force</span></span>
<span data-ttu-id="17448-130">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="17448-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="17448-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17448-131">-ResourceGroupName</span></span>
<span data-ttu-id="17448-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="17448-132">The resource group name.</span></span>

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

### <span data-ttu-id="17448-133">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="17448-133">-Workspace</span></span>
<span data-ttu-id="17448-134">Veri kaynağını içerecek çalışma alanı.</span><span class="sxs-lookup"><span data-stu-id="17448-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="17448-135">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="17448-135">-WorkspaceName</span></span>
<span data-ttu-id="17448-136">Veri kaynağını içerecek çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="17448-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="17448-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="17448-137">-Confirm</span></span>
<span data-ttu-id="17448-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17448-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17448-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17448-139">-WhatIf</span></span>
<span data-ttu-id="17448-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17448-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17448-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17448-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17448-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17448-142">CommonParameters</span></span>
<span data-ttu-id="17448-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17448-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17448-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17448-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17448-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17448-145">INPUTS</span></span>

### <span data-ttu-id="17448-146">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="17448-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="17448-147">System. String</span><span class="sxs-lookup"><span data-stu-id="17448-147">System.String</span></span>

## <span data-ttu-id="17448-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17448-148">OUTPUTS</span></span>

### <span data-ttu-id="17448-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="17448-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="17448-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17448-150">NOTES</span></span>

## <span data-ttu-id="17448-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17448-151">RELATED LINKS</span></span>
