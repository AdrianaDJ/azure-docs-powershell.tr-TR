---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: e87487e55ce285aa5c430dabaa274ee70c34ba00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266195"
---
# <span data-ttu-id="be623-101">Update-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="be623-101">Update-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="be623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be623-102">SYNOPSIS</span></span>
<span data-ttu-id="be623-103">Belirtilen abonelikte, kaynak grubunda ve ortamda olay kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be623-103">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="be623-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be623-104">SYNTAX</span></span>

### <span data-ttu-id="be623-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be623-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="be623-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="be623-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be623-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="be623-107">DESCRIPTION</span></span>
<span data-ttu-id="be623-108">Belirtilen abonelikte, kaynak grubunda ve ortamda olay kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be623-108">Updates the event source with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="be623-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be623-109">EXAMPLES</span></span>

### <span data-ttu-id="be623-110">Örnek 1: belirtilen olay kaynağını ada göre güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="be623-110">Example 1: Update a specified event source by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup -Tag @{"tgk"="001"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="be623-111">Bu komut, belirli bir olay kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be623-111">This command updates a specific event source.</span></span>

### <span data-ttu-id="be623-112">Örnek 3: belirtilen olay kaynağını nesne ile güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="be623-112">Example 3: Update a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Update-AzTimeSeriesInsightsEventSource -InputObject $es -Tag @{"tgb"="002"}

ConsumerGroupName     : testgroup2
EventSourceResourceId : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup2/providers/Microsoft.Devices/IotHubs/iotname001
Id                    : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest001/eventsources/iots001
IotHubName            : iotname001
KeyName               : RootManageSharedAccessKey
Kind                  : Microsoft.IoTHub
Location              : eastus
Name                  : iots001
Tag                   : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimestampPropertyName :
Type                  : Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="be623-113">Bu komut, belirli bir olay kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be623-113">This command updates a specific event source.</span></span>

## <span data-ttu-id="be623-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be623-114">PARAMETERS</span></span>

### <span data-ttu-id="be623-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be623-115">-DefaultProfile</span></span>
<span data-ttu-id="be623-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be623-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be623-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="be623-117">-EnvironmentName</span></span>
<span data-ttu-id="be623-118">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="be623-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be623-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be623-119">-InputObject</span></span>
<span data-ttu-id="be623-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be623-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be623-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="be623-121">-Name</span></span>
<span data-ttu-id="be623-122">Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="be623-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be623-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be623-123">-ResourceGroupName</span></span>
<span data-ttu-id="be623-124">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="be623-124">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be623-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="be623-125">-SubscriptionId</span></span>
<span data-ttu-id="be623-126">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="be623-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be623-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="be623-127">-Tag</span></span>
<span data-ttu-id="be623-128">Olay kaynağı için ek özellik çiftleri</span><span class="sxs-lookup"><span data-stu-id="be623-128">Key-value pairs of additional properties for the event source.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be623-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="be623-129">-Confirm</span></span>
<span data-ttu-id="be623-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be623-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be623-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be623-131">-WhatIf</span></span>
<span data-ttu-id="be623-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be623-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be623-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be623-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be623-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be623-134">CommonParameters</span></span>
<span data-ttu-id="be623-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be623-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be623-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="be623-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be623-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be623-137">INPUTS</span></span>

### <span data-ttu-id="be623-138">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="be623-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="be623-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be623-139">OUTPUTS</span></span>

### <span data-ttu-id="be623-140">Microsoft. Azure. PowerShell. cmdlet. Timeseriesınsights. model. Api20200515. ıeventsourceresource</span><span class="sxs-lookup"><span data-stu-id="be623-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="be623-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be623-141">NOTES</span></span>

<span data-ttu-id="be623-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="be623-142">ALIASES</span></span>

<span data-ttu-id="be623-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="be623-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="be623-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="be623-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="be623-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="be623-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="be623-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="be623-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="be623-147">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="be623-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="be623-148">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="be623-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="be623-149">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="be623-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="be623-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="be623-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="be623-151">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="be623-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="be623-152">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="be623-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="be623-153">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="be623-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="be623-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be623-154">RELATED LINKS</span></span>

