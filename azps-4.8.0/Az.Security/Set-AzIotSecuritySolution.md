---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266369"
---
# <span data-ttu-id="fda61-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="fda61-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="fda61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fda61-102">SYNOPSIS</span></span>
<span data-ttu-id="fda61-103">IoT güvenlik çözümünü oluşturma veya güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fda61-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="fda61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fda61-104">SYNTAX</span></span>

### <span data-ttu-id="fda61-105">ResourceGroupLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fda61-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda61-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fda61-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda61-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="fda61-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda61-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fda61-108">DESCRIPTION</span></span>
<span data-ttu-id="fda61-109">Set-AzIotSecuritySolution cmdlet 'i, belirli bir IoT güvenlik çözümünü oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fda61-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="fda61-110">IoT güvenlik çözümü, tehditlere karşı korunmaya ve saptamasını engellemeye yardımcı olmak için IoT aygıtlarından ve IoT Hub 'dan güvenlik verilerini ve olayları toplar.</span><span class="sxs-lookup"><span data-stu-id="fda61-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="fda61-111">IoT güvenlik çözümünün adı, IoT Hub adı ile aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fda61-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="fda61-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fda61-112">EXAMPLES</span></span>

### <span data-ttu-id="fda61-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fda61-113">Example 1</span></span>
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

<span data-ttu-id="fda61-114">"/Subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" kaynak kimliğiyle IoT Merkezi için yeni IoT güvenlik çözümü oluştur "" (çözümün adı, IoT Hub adıyla aynı olmalıdır)</span><span class="sxs-lookup"><span data-stu-id="fda61-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="fda61-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fda61-115">PARAMETERS</span></span>

### <span data-ttu-id="fda61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda61-116">-DefaultProfile</span></span>
<span data-ttu-id="fda61-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fda61-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fda61-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="fda61-118">-DisabledDataSource</span></span>
<span data-ttu-id="fda61-119">Devre dışı bırakılmış veri kaynakları.</span><span class="sxs-lookup"><span data-stu-id="fda61-119">Disabled data sources.</span></span>

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

### <span data-ttu-id="fda61-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fda61-120">-DisplayName</span></span>
<span data-ttu-id="fda61-121">Görünen ad.</span><span class="sxs-lookup"><span data-stu-id="fda61-121">Display name.</span></span>

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

### <span data-ttu-id="fda61-122">Özellikli</span><span class="sxs-lookup"><span data-stu-id="fda61-122">-Enabled</span></span>
<span data-ttu-id="fda61-123">Durumları.</span><span class="sxs-lookup"><span data-stu-id="fda61-123">Status .</span></span>

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

### <span data-ttu-id="fda61-124">-Export</span><span class="sxs-lookup"><span data-stu-id="fda61-124">-Export</span></span>
<span data-ttu-id="fda61-125">Verileri dışarı aktarma.</span><span class="sxs-lookup"><span data-stu-id="fda61-125">Export data.</span></span>

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

### <span data-ttu-id="fda61-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fda61-126">-InputObject</span></span>
<span data-ttu-id="fda61-127">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fda61-127">Input Object.</span></span>

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

### <span data-ttu-id="fda61-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="fda61-128">-IotHub</span></span>
<span data-ttu-id="fda61-129">IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="fda61-129">Iot hubs.</span></span>

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

### <span data-ttu-id="fda61-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="fda61-130">-Location</span></span>
<span data-ttu-id="fda61-131">Konumuyla.</span><span class="sxs-lookup"><span data-stu-id="fda61-131">Location.</span></span>

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

### <span data-ttu-id="fda61-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="fda61-132">-Name</span></span>
<span data-ttu-id="fda61-133">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="fda61-133">Resource name.</span></span>

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

### <span data-ttu-id="fda61-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="fda61-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="fda61-135">Öneriler yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="fda61-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="fda61-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda61-136">-ResourceGroupName</span></span>
<span data-ttu-id="fda61-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fda61-137">Resource group name.</span></span>

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

### <span data-ttu-id="fda61-138">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fda61-138">-ResourceId</span></span>
<span data-ttu-id="fda61-139">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fda61-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="fda61-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fda61-140">-Tag</span></span>
<span data-ttu-id="fda61-141">Akıllı.</span><span class="sxs-lookup"><span data-stu-id="fda61-141">Tags.</span></span>

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

### <span data-ttu-id="fda61-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="fda61-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="fda61-143">Maskelenmemiş IP günlüğe kaydetme durumu.</span><span class="sxs-lookup"><span data-stu-id="fda61-143">Unmasked ip logging status.</span></span>

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

### <span data-ttu-id="fda61-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="fda61-144">-UserDefinedResource</span></span>
<span data-ttu-id="fda61-145">Kullanıcı tanımlı kaynaklar.</span><span class="sxs-lookup"><span data-stu-id="fda61-145">User defined resources.</span></span>

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

### <span data-ttu-id="fda61-146">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="fda61-146">-Workspace</span></span>
<span data-ttu-id="fda61-147">Çalışma alanı KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fda61-147">Workspace ID.</span></span>

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

### <span data-ttu-id="fda61-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="fda61-148">-Confirm</span></span>
<span data-ttu-id="fda61-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fda61-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda61-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda61-150">-WhatIf</span></span>
<span data-ttu-id="fda61-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fda61-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fda61-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fda61-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fda61-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda61-153">CommonParameters</span></span>
<span data-ttu-id="fda61-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fda61-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda61-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fda61-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda61-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fda61-156">INPUTS</span></span>

### <span data-ttu-id="fda61-157">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="fda61-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="fda61-158">System. String</span><span class="sxs-lookup"><span data-stu-id="fda61-158">System.String</span></span>

### <span data-ttu-id="fda61-159">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fda61-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fda61-160">System. String []</span><span class="sxs-lookup"><span data-stu-id="fda61-160">System.String[]</span></span>

### <span data-ttu-id="fda61-161">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="fda61-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="fda61-162">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSRecommendationConfiguration []</span><span class="sxs-lookup"><span data-stu-id="fda61-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="fda61-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fda61-163">OUTPUTS</span></span>

### <span data-ttu-id="fda61-164">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="fda61-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="fda61-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fda61-165">NOTES</span></span>

## <span data-ttu-id="fda61-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fda61-166">RELATED LINKS</span></span>
