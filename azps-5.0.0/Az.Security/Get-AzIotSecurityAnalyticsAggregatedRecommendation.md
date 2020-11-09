---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322109"
---
# <span data-ttu-id="1ffc9-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="1ffc9-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="1ffc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ffc9-102">SYNOPSIS</span></span>
<span data-ttu-id="1ffc9-103">IoT güvenliğini sağlayın toplu öneri</span><span class="sxs-lookup"><span data-stu-id="1ffc9-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="1ffc9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ffc9-104">SYNTAX</span></span>

### <span data-ttu-id="1ffc9-105">SolutionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ffc9-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ffc9-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="1ffc9-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ffc9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ffc9-107">DESCRIPTION</span></span>
<span data-ttu-id="1ffc9-108">Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet, IoT Hub aygıtlarında bir veya birden çok Birleşik öneri döndürür.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="1ffc9-109">Toplanmış bir önerisinin adı türü</span><span class="sxs-lookup"><span data-stu-id="1ffc9-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="1ffc9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ffc9-110">EXAMPLES</span></span>

### <span data-ttu-id="1ffc9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1ffc9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="1ffc9-112">"IoT_OpenPorts" güvenlik çözümünde "MyResourceGroup" ve kaynak grubu "MyResourceGroup" toplanmış önerisini alma</span><span class="sxs-lookup"><span data-stu-id="1ffc9-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="1ffc9-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1ffc9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="1ffc9-114">"MyResourceGroup" güvenlik çözümünde toplu önerilerin listesini alma</span><span class="sxs-lookup"><span data-stu-id="1ffc9-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="1ffc9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ffc9-115">PARAMETERS</span></span>

### <span data-ttu-id="1ffc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ffc9-116">-DefaultProfile</span></span>
<span data-ttu-id="1ffc9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ffc9-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ffc9-118">-Name</span></span>
<span data-ttu-id="1ffc9-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffc9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ffc9-120">-ResourceGroupName</span></span>
<span data-ttu-id="1ffc9-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-121">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffc9-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="1ffc9-122">-SolutionName</span></span>
<span data-ttu-id="1ffc9-123">Çözüm adı</span><span class="sxs-lookup"><span data-stu-id="1ffc9-123">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ffc9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ffc9-124">CommonParameters</span></span>
<span data-ttu-id="1ffc9-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ffc9-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1ffc9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ffc9-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ffc9-127">INPUTS</span></span>

### <span data-ttu-id="1ffc9-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1ffc9-128">None</span></span>

## <span data-ttu-id="1ffc9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ffc9-129">OUTPUTS</span></span>

### <span data-ttu-id="1ffc9-130">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutionanalytics. Psiotsecurityaggregotönerisi</span><span class="sxs-lookup"><span data-stu-id="1ffc9-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="1ffc9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ffc9-131">NOTES</span></span>

## <span data-ttu-id="1ffc9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ffc9-132">RELATED LINKS</span></span>
