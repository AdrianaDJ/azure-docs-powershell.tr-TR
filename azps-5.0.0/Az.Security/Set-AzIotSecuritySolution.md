---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278008"
---
# <span data-ttu-id="2f97d-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="2f97d-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="2f97d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f97d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f97d-103">IoT güvenlik çözümünü oluşturma veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2f97d-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="2f97d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f97d-104">SYNTAX</span></span>

### <span data-ttu-id="2f97d-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f97d-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f97d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2f97d-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f97d-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2f97d-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f97d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f97d-108">DESCRIPTION</span></span>
<span data-ttu-id="2f97d-109">Set-AzIotSecuritySolution cmdlet 'i, belirli bir IoT güvenlik çözümünü oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2f97d-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="2f97d-110">IoT güvenlik çözümü, tehditlere karşı korunmaya ve saptamasını engellemeye yardımcı olmak için IoT aygıtlarından ve IoT Hub 'dan güvenlik verilerini ve olayları toplar.</span><span class="sxs-lookup"><span data-stu-id="2f97d-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="2f97d-111">IoT güvenlik çözümünün adı, IoT Hub adı ile aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f97d-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="2f97d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f97d-112">EXAMPLES</span></span>

### <span data-ttu-id="2f97d-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2f97d-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

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
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="2f97d-114">"/Subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" kaynak kimliğiyle IoT Merkezi için yeni IoT güvenlik çözümü oluştur "" (çözümün adı, IoT Hub adıyla aynı olmalıdır)</span><span class="sxs-lookup"><span data-stu-id="2f97d-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="2f97d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f97d-115">PARAMETERS</span></span>

### <span data-ttu-id="2f97d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f97d-116">-DefaultProfile</span></span>
<span data-ttu-id="2f97d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f97d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f97d-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="2f97d-118">-DisabledDataSource</span></span>
<span data-ttu-id="2f97d-119">Devre dışı bırakılmış veri kaynakları.</span><span class="sxs-lookup"><span data-stu-id="2f97d-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f97d-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2f97d-120">-DisplayName</span></span>
<span data-ttu-id="2f97d-121">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="2f97d-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f97d-122">Özellikli</span><span class="sxs-lookup"><span data-stu-id="2f97d-122">-Enabled</span></span>
<span data-ttu-id="2f97d-123">Durumları.</span><span class="sxs-lookup"><span data-stu-id="2f97d-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f97d-124">-Export</span><span class="sxs-lookup"><span data-stu-id="2f97d-124">-Export</span></span>
<span data-ttu-id="2f97d-125">Verileri dışarı aktarma.</span><span class="sxs-lookup"><span data-stu-id="2f97d-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f97d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f97d-126">-InputObject</span></span>
<span data-ttu-id="2f97d-127">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2f97d-127">Input Object.</span></span>

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

### <span data-ttu-id="2f97d-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="2f97d-128">-IotHub</span></span>
<span data-ttu-id="2f97d-129">IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="2f97d-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f97d-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="2f97d-130">-Location</span></span>
<span data-ttu-id="2f97d-131">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="2f97d-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f97d-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="2f97d-132">-Name</span></span>
<span data-ttu-id="2f97d-133">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="2f97d-133">Resource name.</span></span>

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

### <span data-ttu-id="2f97d-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f97d-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="2f97d-135">Öneriler yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="2f97d-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="2f97d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f97d-136">-ResourceGroupName</span></span>
<span data-ttu-id="2f97d-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2f97d-137">Resource group name.</span></span>

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

### <span data-ttu-id="2f97d-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2f97d-138">-ResourceId</span></span>
<span data-ttu-id="2f97d-139">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2f97d-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="2f97d-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2f97d-140">-Tag</span></span>
<span data-ttu-id="2f97d-141">Akıllı.</span><span class="sxs-lookup"><span data-stu-id="2f97d-141">Tags.</span></span>

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

### <span data-ttu-id="2f97d-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="2f97d-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="2f97d-143">Maskelenmemiş IP günlüğe kaydetme durumu.</span><span class="sxs-lookup"><span data-stu-id="2f97d-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f97d-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="2f97d-144">-UserDefinedResource</span></span>
<span data-ttu-id="2f97d-145">Kullanıcı tanımlı kaynaklar.</span><span class="sxs-lookup"><span data-stu-id="2f97d-145">User defined resources.</span></span>

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

### <span data-ttu-id="2f97d-146">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="2f97d-146">-Workspace</span></span>
<span data-ttu-id="2f97d-147">Çalışma alanı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2f97d-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f97d-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="2f97d-148">-Confirm</span></span>
<span data-ttu-id="2f97d-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2f97d-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f97d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f97d-150">-WhatIf</span></span>
<span data-ttu-id="2f97d-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f97d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f97d-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2f97d-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f97d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f97d-153">CommonParameters</span></span>
<span data-ttu-id="2f97d-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f97d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f97d-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2f97d-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f97d-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f97d-156">INPUTS</span></span>

### <span data-ttu-id="2f97d-157">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="2f97d-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="2f97d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="2f97d-158">System.String</span></span>

### <span data-ttu-id="2f97d-159">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2f97d-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2f97d-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="2f97d-160">System.String[]</span></span>

### <span data-ttu-id="2f97d-161">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="2f97d-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="2f97d-162">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="2f97d-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="2f97d-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f97d-163">OUTPUTS</span></span>

### <span data-ttu-id="2f97d-164">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="2f97d-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="2f97d-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f97d-165">NOTES</span></span>

## <span data-ttu-id="2f97d-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f97d-166">RELATED LINKS</span></span>
