---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273986"
---
# <span data-ttu-id="91e05-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="91e05-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="91e05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e05-102">SYNOPSIS</span></span>
<span data-ttu-id="91e05-103">IoT güvenliğini sağlayın toplu öneri</span><span class="sxs-lookup"><span data-stu-id="91e05-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="91e05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91e05-104">SYNTAX</span></span>

### <span data-ttu-id="91e05-105">SolutionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="91e05-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91e05-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="91e05-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91e05-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="91e05-107">DESCRIPTION</span></span>
<span data-ttu-id="91e05-108">Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet, IoT Hub aygıtlarında bir veya birden çok Birleşik öneri döndürür.</span><span class="sxs-lookup"><span data-stu-id="91e05-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="91e05-109">Toplanmış bir önerisinin adı türü</span><span class="sxs-lookup"><span data-stu-id="91e05-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="91e05-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91e05-110">EXAMPLES</span></span>

### <span data-ttu-id="91e05-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91e05-111">Example 1</span></span>
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

<span data-ttu-id="91e05-112">"IoT_OpenPorts" güvenlik çözümünde "MyResourceGroup" ve kaynak grubu "MyResourceGroup" toplanmış önerisini alma</span><span class="sxs-lookup"><span data-stu-id="91e05-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="91e05-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="91e05-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="91e05-114">"MyResourceGroup" güvenlik çözümünde toplu önerilerin listesini alma</span><span class="sxs-lookup"><span data-stu-id="91e05-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="91e05-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91e05-115">PARAMETERS</span></span>

### <span data-ttu-id="91e05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e05-116">-DefaultProfile</span></span>
<span data-ttu-id="91e05-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91e05-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91e05-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="91e05-118">-Name</span></span>
<span data-ttu-id="91e05-119">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="91e05-119">Resource name.</span></span>

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

### <span data-ttu-id="91e05-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e05-120">-ResourceGroupName</span></span>
<span data-ttu-id="91e05-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="91e05-121">Resource group name.</span></span>

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

### <span data-ttu-id="91e05-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="91e05-122">-SolutionName</span></span>
<span data-ttu-id="91e05-123">Çözüm adı</span><span class="sxs-lookup"><span data-stu-id="91e05-123">Solution name</span></span>

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

### <span data-ttu-id="91e05-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e05-124">CommonParameters</span></span>
<span data-ttu-id="91e05-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91e05-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e05-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="91e05-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e05-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91e05-127">INPUTS</span></span>

### <span data-ttu-id="91e05-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="91e05-128">None</span></span>

## <span data-ttu-id="91e05-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91e05-129">OUTPUTS</span></span>

### <span data-ttu-id="91e05-130">Microsoft. Azure. Commands. Security. model. ıotsecuritysolutionanalytics. Psiotsecurityaggregotönerisi</span><span class="sxs-lookup"><span data-stu-id="91e05-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="91e05-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91e05-131">NOTES</span></span>

## <span data-ttu-id="91e05-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91e05-132">RELATED LINKS</span></span>
