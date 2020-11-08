---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108743"
---
# <span data-ttu-id="963e6-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="963e6-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="963e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="963e6-102">SYNOPSIS</span></span>
<span data-ttu-id="963e6-103">IoT güvenlik çözümünde aşağıdaki özelliklerden birini veya daha fazlasını güncelleştirin: Etiketler, öneri yapılandırması, Kullanıcı tanımlı kaynaklar</span><span class="sxs-lookup"><span data-stu-id="963e6-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="963e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="963e6-104">SYNTAX</span></span>

### <span data-ttu-id="963e6-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="963e6-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="963e6-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="963e6-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="963e6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="963e6-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="963e6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="963e6-108">DESCRIPTION</span></span>
<span data-ttu-id="963e6-109">Update-AzIotSecuritySolution cmdlet 'i, belirli bir IoT güvenlik çözümünde aşağıdaki özelliklerden bir veya daha fazlasını güncelleştirin: Etiketler, öneri yapılandırması, Kullanıcı tanımlı kaynaklar.</span><span class="sxs-lookup"><span data-stu-id="963e6-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="963e6-110">IoT güvenlik çözümünün içinde yalnızca belirtilen özellikler güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="963e6-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="963e6-111">IoT güvenlik çözümü, tehditlere karşı korunmaya ve saptamasını engellemeye yardımcı olmak için IoT aygıtlarından ve IoT Hub 'dan güvenlik verilerini ve olayları toplar.</span><span class="sxs-lookup"><span data-stu-id="963e6-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="963e6-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="963e6-112">EXAMPLES</span></span>

### <span data-ttu-id="963e6-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="963e6-113">Example 1</span></span>
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

<span data-ttu-id="963e6-114">IoT güvenlik çözümünü "MyResourceGroup" kaynak grubundan öneri yapılandırması ve Kullanıcı tanımlı kaynaklar ile güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="963e6-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="963e6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="963e6-115">PARAMETERS</span></span>

### <span data-ttu-id="963e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="963e6-116">-DefaultProfile</span></span>
<span data-ttu-id="963e6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="963e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="963e6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="963e6-118">-InputObject</span></span>
<span data-ttu-id="963e6-119">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="963e6-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="963e6-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="963e6-120">-Name</span></span>
<span data-ttu-id="963e6-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="963e6-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="963e6-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="963e6-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="963e6-123">Öneriler yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="963e6-123">Recommendations configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="963e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="963e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="963e6-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="963e6-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="963e6-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="963e6-126">-ResourceId</span></span>
<span data-ttu-id="963e6-127">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="963e6-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="963e6-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="963e6-128">-Tag</span></span>
<span data-ttu-id="963e6-129">Akıllı.</span><span class="sxs-lookup"><span data-stu-id="963e6-129">Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="963e6-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="963e6-130">-UserDefinedResource</span></span>
<span data-ttu-id="963e6-131">Kullanıcı tanımlı kaynaklar.</span><span class="sxs-lookup"><span data-stu-id="963e6-131">User defined resources.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="963e6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="963e6-132">-Confirm</span></span>
<span data-ttu-id="963e6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="963e6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="963e6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="963e6-134">-WhatIf</span></span>
<span data-ttu-id="963e6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="963e6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="963e6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="963e6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="963e6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="963e6-137">CommonParameters</span></span>
<span data-ttu-id="963e6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="963e6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="963e6-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="963e6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="963e6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="963e6-140">INPUTS</span></span>

### <span data-ttu-id="963e6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="963e6-141">System.String</span></span>

### <span data-ttu-id="963e6-142">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="963e6-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="963e6-143">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="963e6-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="963e6-144">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="963e6-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="963e6-145">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="963e6-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="963e6-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="963e6-146">OUTPUTS</span></span>

### <span data-ttu-id="963e6-147">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="963e6-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="963e6-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="963e6-148">NOTES</span></span>

## <span data-ttu-id="963e6-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="963e6-149">RELATED LINKS</span></span>
