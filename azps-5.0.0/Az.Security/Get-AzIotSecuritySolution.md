---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecuritySolution.md
ms.openlocfilehash: 338486954fe04b6497eb82bc5a11dbede1b25709
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279468"
---
# <span data-ttu-id="02d43-101">Get-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="02d43-101">Get-AzIotSecuritySolution</span></span>

## <span data-ttu-id="02d43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02d43-102">SYNOPSIS</span></span>
<span data-ttu-id="02d43-103">IoT güvenlik çözümünü edinin</span><span class="sxs-lookup"><span data-stu-id="02d43-103">Get IoT security solution</span></span>

## <span data-ttu-id="02d43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02d43-104">SYNTAX</span></span>

### <span data-ttu-id="02d43-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02d43-105">SubscriptionScope (Default)</span></span>
```
Get-AzIotSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02d43-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="02d43-106">ResourceGroupScope</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02d43-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="02d43-107">ResourceGroupLevelResource</span></span>
```
Get-AzIotSecuritySolution -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02d43-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="02d43-108">ResourceId</span></span>
```
Get-AzIotSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02d43-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="02d43-109">DESCRIPTION</span></span>
<span data-ttu-id="02d43-110">Get-AzIotSecuritySolution cmdlet 'i, bir veya daha fazla IoT güvenlik çözümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="02d43-110">The Get-AzIotSecuritySolution cmdlet returns one or more iot security solutions.</span></span> <span data-ttu-id="02d43-111">IoT güvenlik çözümü, tehditlere karşı korunmaya ve saptamasını engellemeye yardımcı olmak için IoT aygıtlarından ve IoT Hub 'dan güvenlik verilerini ve olayları toplar.</span><span class="sxs-lookup"><span data-stu-id="02d43-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="02d43-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02d43-112">EXAMPLES</span></span>

### <span data-ttu-id="02d43-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02d43-113">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "centraluseuap"
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

<span data-ttu-id="02d43-114">"MyResourceGroup" kaynak grubunda "MySample" çözümünü edinin</span><span class="sxs-lookup"><span data-stu-id="02d43-114">Get the solution "MySample" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="02d43-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="02d43-115">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecuritySolution -ResourceGroupName "MyResourceGroup"

Array of security solution items as shown is example 1
```

<span data-ttu-id="02d43-116">"MyResourceGroup" kaynak grubundaki tüm güvenlik çözümlerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="02d43-116">Get list of all security solutions in resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="02d43-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02d43-117">PARAMETERS</span></span>

### <span data-ttu-id="02d43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02d43-118">-DefaultProfile</span></span>
<span data-ttu-id="02d43-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02d43-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02d43-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="02d43-120">-Name</span></span>
<span data-ttu-id="02d43-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="02d43-121">Resource name.</span></span>

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

### <span data-ttu-id="02d43-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02d43-122">-ResourceGroupName</span></span>
<span data-ttu-id="02d43-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="02d43-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02d43-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02d43-124">-ResourceId</span></span>
<span data-ttu-id="02d43-125">Komutu çağırmak istediğiniz güvenlik kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="02d43-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="02d43-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02d43-126">CommonParameters</span></span>
<span data-ttu-id="02d43-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02d43-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02d43-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02d43-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02d43-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02d43-129">INPUTS</span></span>

### <span data-ttu-id="02d43-130">System. String</span><span class="sxs-lookup"><span data-stu-id="02d43-130">System.String</span></span>

## <span data-ttu-id="02d43-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02d43-131">OUTPUTS</span></span>

### <span data-ttu-id="02d43-132">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutions. PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="02d43-132">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="02d43-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02d43-133">NOTES</span></span>

## <span data-ttu-id="02d43-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02d43-134">RELATED LINKS</span></span>
