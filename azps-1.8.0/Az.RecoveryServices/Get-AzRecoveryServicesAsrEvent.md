---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 0c7b80c77d91f8b92fc4ab03f715412ac061b9fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759744"
---
# <span data-ttu-id="2c167-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="2c167-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="2c167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c167-102">SYNOPSIS</span></span>
<span data-ttu-id="2c167-103">Kasadaki Azure Site kurtarma olaylarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="2c167-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="2c167-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c167-104">SYNTAX</span></span>

### <span data-ttu-id="2c167-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2c167-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c167-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2c167-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c167-107">Byfabricıd</span><span class="sxs-lookup"><span data-stu-id="2c167-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c167-108">ByName</span><span class="sxs-lookup"><span data-stu-id="2c167-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c167-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c167-109">DESCRIPTION</span></span>
<span data-ttu-id="2c167-110">**Get-AzRecoveryServicesAsrEvent** , belirtilen seçim filtrelerine bağlı olarak kasadaki olayların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2c167-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="2c167-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c167-111">EXAMPLES</span></span>

### <span data-ttu-id="2c167-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c167-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="2c167-113">Tüm olayların listesi.</span><span class="sxs-lookup"><span data-stu-id="2c167-113">List of all events.</span></span>

### <span data-ttu-id="2c167-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2c167-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="2c167-115">Olayı ada göre alın.</span><span class="sxs-lookup"><span data-stu-id="2c167-115">Get event by name.</span></span>

### <span data-ttu-id="2c167-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2c167-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="2c167-117">Etkilenen nesne için olay listesi.</span><span class="sxs-lookup"><span data-stu-id="2c167-117">List of event for affected Object.</span></span>

### <span data-ttu-id="2c167-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="2c167-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="2c167-119">Zaman başlangıç saati ve bitiş saati arasındaki olay listesi, önem düzeyi ve sistem durumu türü VmHealth.</span><span class="sxs-lookup"><span data-stu-id="2c167-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="2c167-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c167-120">PARAMETERS</span></span>

### <span data-ttu-id="2c167-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="2c167-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="2c167-122">Arama için AffectedObject FriendlyName 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c167-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c167-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c167-123">-DefaultProfile</span></span>
<span data-ttu-id="2c167-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c167-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c167-125">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="2c167-125">-EndTime</span></span>
<span data-ttu-id="2c167-126">Ara penceresinin bitiş saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c167-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="2c167-127">Yalnızca belirtilen süreden önce oluşan olayları almak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="2c167-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c167-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="2c167-128">-EventType</span></span>
<span data-ttu-id="2c167-129">Olayları olay türüne göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="2c167-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c167-130">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="2c167-130">-Fabric</span></span>
<span data-ttu-id="2c167-131">Olayları belirtilen yapıya göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="2c167-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c167-132">-Fabricıd</span><span class="sxs-lookup"><span data-stu-id="2c167-132">-FabricId</span></span>
<span data-ttu-id="2c167-133">Filtrelemek için Fabricıd 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c167-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c167-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c167-134">-Name</span></span>
<span data-ttu-id="2c167-135">Arama için olayın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c167-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c167-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2c167-136">-ResourceId</span></span>
<span data-ttu-id="2c167-137">Etkinliğin etkinlik kodu.</span><span class="sxs-lookup"><span data-stu-id="2c167-137">Specifes the event ReourceId of event.</span></span>

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

### <span data-ttu-id="2c167-138">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="2c167-138">-Severity</span></span>
<span data-ttu-id="2c167-139">Filtre uygulanacak etkinlik önemi.</span><span class="sxs-lookup"><span data-stu-id="2c167-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c167-140">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="2c167-140">-StartTime</span></span>
<span data-ttu-id="2c167-141">Ara penceresinin başlangıç saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2c167-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="2c167-142">Yalnızca belirtilen süreden sonra oluşan olayları almak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="2c167-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c167-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c167-143">CommonParameters</span></span>
<span data-ttu-id="2c167-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c167-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c167-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c167-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c167-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c167-146">INPUTS</span></span>

### <span data-ttu-id="2c167-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2c167-147">System.String</span></span>

## <span data-ttu-id="2c167-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c167-148">OUTPUTS</span></span>

### <span data-ttu-id="2c167-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASREvent</span><span class="sxs-lookup"><span data-stu-id="2c167-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="2c167-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c167-150">NOTES</span></span>

## <span data-ttu-id="2c167-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c167-151">RELATED LINKS</span></span>
