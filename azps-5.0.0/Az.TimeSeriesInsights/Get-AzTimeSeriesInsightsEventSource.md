---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 5590a89b22c0adc3dfb2df88e6b977dec268a822
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277906"
---
# <span data-ttu-id="0de22-101">Get-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="0de22-101">Get-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="0de22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0de22-102">SYNOPSIS</span></span>
<span data-ttu-id="0de22-103">Belirtilen ortamdaki belirtilen ada sahip olay kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="0de22-103">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="0de22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0de22-104">SYNTAX</span></span>

### <span data-ttu-id="0de22-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0de22-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0de22-106">Al</span><span class="sxs-lookup"><span data-stu-id="0de22-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0de22-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="0de22-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0de22-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0de22-108">DESCRIPTION</span></span>
<span data-ttu-id="0de22-109">Belirtilen ortamdaki belirtilen ada sahip olay kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="0de22-109">Gets the event source with the specified name in the specified environment.</span></span>

## <span data-ttu-id="0de22-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0de22-110">EXAMPLES</span></span>

### <span data-ttu-id="0de22-111">Örnek 1: belirtilen ortamdaki tüm olay kaynaklarını listeler</span><span class="sxs-lookup"><span data-stu-id="0de22-111">Example 1: List all event sources under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001

ConsumerGroupName     : testgroup2
EventHubName          : hubname001
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.EventHub/namespaces/spacename001/eventhubs/hu 
                        bname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/estest001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus
Name                  : estest001
ServiceBusNamespace   : spacename001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve 
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="0de22-112">Bu komut, belirtilen ortamların altındaki tüm olay kaynaklarını listeler.</span><span class="sxs-lookup"><span data-stu-id="0de22-112">This command lists all event sources under the specified environments.</span></span>

### <span data-ttu-id="0de22-113">Örnek 2: adla belirtilen bir olay kaynağını alma</span><span class="sxs-lookup"><span data-stu-id="0de22-113">Example 2: Get a specified event source by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -EnvironmentName tsitest001 -Name iots001

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eve
                        ntsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="0de22-114">Bu komut belirli bir olay kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="0de22-114">This command gets a specific event source.</span></span>

### <span data-ttu-id="0de22-115">Örnek 3: belirli bir olay kaynağını nesneye alma</span><span class="sxs-lookup"><span data-stu-id="0de22-115">Example 3: Get a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsi-esrfyi9h
PS C:\> Get-AzTimeSeriesInsightsEventSource -InputObject $es

ConsumerGroupName     : tsi-test-i01k5l
EventHubName          : eventhubname-d2rvmp
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.EventHub/namespaces/eventhubspace-0t3khp/eventhubs/eventhubname-d2rvmp
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x/eventsources/tsi-esrfyi9h
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.EventHub
Location              : eastus2
Name                  : tsi-esrfyi9h
ServiceBusNamespace   : eventhubspace-0t3khp
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="0de22-116">Bu komut belirli bir olay kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="0de22-116">This command gets a specific event source.</span></span>

## <span data-ttu-id="0de22-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0de22-117">PARAMETERS</span></span>

### <span data-ttu-id="0de22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0de22-118">-DefaultProfile</span></span>
<span data-ttu-id="0de22-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0de22-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de22-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="0de22-120">-EnvironmentName</span></span>
<span data-ttu-id="0de22-121">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="0de22-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de22-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0de22-122">-InputObject</span></span>
<span data-ttu-id="0de22-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0de22-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0de22-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="0de22-124">-Name</span></span>
<span data-ttu-id="0de22-125">Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0de22-125">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de22-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0de22-126">-ResourceGroupName</span></span>
<span data-ttu-id="0de22-127">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0de22-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de22-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0de22-128">-SubscriptionId</span></span>
<span data-ttu-id="0de22-129">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0de22-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0de22-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0de22-130">CommonParameters</span></span>
<span data-ttu-id="0de22-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0de22-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0de22-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0de22-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0de22-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0de22-133">INPUTS</span></span>

### <span data-ttu-id="0de22-134">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="0de22-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="0de22-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0de22-135">OUTPUTS</span></span>

### <span data-ttu-id="0de22-136">Microsoft. Azure. PowerShell. cmdlet. Timeseriesınsights. model. Api20200515. ıeventsourceresource</span><span class="sxs-lookup"><span data-stu-id="0de22-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="0de22-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0de22-137">NOTES</span></span>

<span data-ttu-id="0de22-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0de22-138">ALIASES</span></span>

<span data-ttu-id="0de22-139">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="0de22-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0de22-140">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0de22-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0de22-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0de22-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0de22-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="0de22-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0de22-143">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="0de22-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="0de22-144">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="0de22-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="0de22-145">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="0de22-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="0de22-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="0de22-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0de22-147">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="0de22-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="0de22-148">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0de22-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="0de22-149">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0de22-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0de22-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0de22-150">RELATED LINKS</span></span>

