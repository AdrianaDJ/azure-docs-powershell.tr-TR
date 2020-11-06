---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: b9933a3dd5b5fd370f6ba603809ad428dc9585c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591923"
---
# <span data-ttu-id="65d23-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="65d23-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="65d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65d23-102">SYNOPSIS</span></span>
<span data-ttu-id="65d23-103">Kasadaki Azure Site kurtarma olaylarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="65d23-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65d23-104">SYNTAX</span></span>

### <span data-ttu-id="65d23-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65d23-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65d23-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="65d23-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65d23-107">Byfabricıd</span><span class="sxs-lookup"><span data-stu-id="65d23-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65d23-108">ByName</span><span class="sxs-lookup"><span data-stu-id="65d23-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65d23-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="65d23-109">DESCRIPTION</span></span>
<span data-ttu-id="65d23-110">**Get-AzureRmRecoveryServicesAsrEvent** , belirtilen seçim filtrelerine bağlı olarak kasadaki olayların listesini alır.</span><span class="sxs-lookup"><span data-stu-id="65d23-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="65d23-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65d23-111">EXAMPLES</span></span>

### <span data-ttu-id="65d23-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="65d23-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="65d23-113">Tüm olayların listesi.</span><span class="sxs-lookup"><span data-stu-id="65d23-113">List of all events.</span></span>

### <span data-ttu-id="65d23-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="65d23-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


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

<span data-ttu-id="65d23-115">Olayı ada göre alın.</span><span class="sxs-lookup"><span data-stu-id="65d23-115">Get event by name.</span></span>

### <span data-ttu-id="65d23-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="65d23-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="65d23-117">Etkilenen nesne için olay listesi.</span><span class="sxs-lookup"><span data-stu-id="65d23-117">List of event for affected Object.</span></span>

### <span data-ttu-id="65d23-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="65d23-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="65d23-119">Zaman başlangıç saati ve bitiş saati arasındaki olay listesi, önem düzeyi ve sistem durumu türü VmHealth.</span><span class="sxs-lookup"><span data-stu-id="65d23-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="65d23-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65d23-120">PARAMETERS</span></span>

### <span data-ttu-id="65d23-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="65d23-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="65d23-122">Arama için AffectedObject FriendlyName 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="65d23-122">Specifies AffectedObject FriendlyName for the search.</span></span>

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

### <span data-ttu-id="65d23-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d23-123">-DefaultProfile</span></span>
<span data-ttu-id="65d23-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65d23-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65d23-125">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="65d23-125">-EndTime</span></span>
<span data-ttu-id="65d23-126">Ara penceresinin bitiş saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65d23-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="65d23-127">Yalnızca belirtilen süreden önce oluşan olayları almak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="65d23-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

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

### <span data-ttu-id="65d23-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="65d23-128">-EventType</span></span>
<span data-ttu-id="65d23-129">Olayları olay türüne göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="65d23-129">Filter events by the event type.</span></span>

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

### <span data-ttu-id="65d23-130">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="65d23-130">-Fabric</span></span>
<span data-ttu-id="65d23-131">Olayları belirtilen yapıya göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="65d23-131">Filter events by the specified fabric.</span></span>

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

### <span data-ttu-id="65d23-132">-Fabricıd</span><span class="sxs-lookup"><span data-stu-id="65d23-132">-FabricId</span></span>
<span data-ttu-id="65d23-133">Filtrelemek için Fabricıd 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="65d23-133">Specifies the fabricId to filter.</span></span>

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

### <span data-ttu-id="65d23-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="65d23-134">-Name</span></span>
<span data-ttu-id="65d23-135">Arama için olayın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65d23-135">Specifies name of the event for search.</span></span>

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

### <span data-ttu-id="65d23-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="65d23-136">-ResourceId</span></span>
<span data-ttu-id="65d23-137">Etkinliğin etkinlik kodu.</span><span class="sxs-lookup"><span data-stu-id="65d23-137">Specifes the event ReourceId of event.</span></span>

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

### <span data-ttu-id="65d23-138">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="65d23-138">-Severity</span></span>
<span data-ttu-id="65d23-139">Filtre uygulanacak etkinlik önemi.</span><span class="sxs-lookup"><span data-stu-id="65d23-139">Event severity to filter on.</span></span>

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

### <span data-ttu-id="65d23-140">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="65d23-140">-StartTime</span></span>
<span data-ttu-id="65d23-141">Ara penceresinin başlangıç saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65d23-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="65d23-142">Yalnızca belirtilen süreden sonra oluşan olayları almak için bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="65d23-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

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

### <span data-ttu-id="65d23-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d23-143">CommonParameters</span></span>
<span data-ttu-id="65d23-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65d23-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d23-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65d23-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d23-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65d23-146">INPUTS</span></span>

### <span data-ttu-id="65d23-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="65d23-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="65d23-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65d23-148">OUTPUTS</span></span>

### <span data-ttu-id="65d23-149">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASREvent, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="65d23-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="65d23-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65d23-150">NOTES</span></span>

## <span data-ttu-id="65d23-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65d23-151">RELATED LINKS</span></span>
