---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279739"
---
# <span data-ttu-id="f062d-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="f062d-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="f062d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f062d-102">SYNOPSIS</span></span>
<span data-ttu-id="f062d-103">Belirtilen abonelik ve kaynak grubunda belirtilen ada sahip ortamı alır.</span><span class="sxs-lookup"><span data-stu-id="f062d-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f062d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f062d-104">SYNTAX</span></span>

### <span data-ttu-id="f062d-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f062d-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f062d-106">Al</span><span class="sxs-lookup"><span data-stu-id="f062d-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f062d-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="f062d-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f062d-108">Listeniz</span><span class="sxs-lookup"><span data-stu-id="f062d-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f062d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f062d-109">DESCRIPTION</span></span>
<span data-ttu-id="f062d-110">Belirtilen abonelik ve kaynak grubunda belirtilen ada sahip ortamı alır.</span><span class="sxs-lookup"><span data-stu-id="f062d-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f062d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f062d-111">EXAMPLES</span></span>

### <span data-ttu-id="f062d-112">Örnek 1: zaman serisi Öngörüler ortamı alma</span><span class="sxs-lookup"><span data-stu-id="f062d-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="f062d-113">Bu komut, zaman serisi öngörüleri ortamını alır.</span><span class="sxs-lookup"><span data-stu-id="f062d-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="f062d-114">Örnek 2: tüm zaman serisi Öngörüler ortamlarını listeleyin</span><span class="sxs-lookup"><span data-stu-id="f062d-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="f062d-115">Bu komut, bir kaynak grubundaki tüm bir dizi öngörü ortamlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="f062d-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="f062d-116">Örnek 3: nesneye göre zaman serisi Öngörüler</span><span class="sxs-lookup"><span data-stu-id="f062d-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="f062d-117">Bu komut, zaman serisi öngörüleri ortamlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f062d-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="f062d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f062d-118">PARAMETERS</span></span>

### <span data-ttu-id="f062d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f062d-119">-DefaultProfile</span></span>
<span data-ttu-id="f062d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f062d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f062d-121">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="f062d-121">-Expand</span></span>
<span data-ttu-id="f062d-122">$Expand = durum ayarı, zaman serisi öngörüleri hizmetindeki ortamın iç hizmetlerinin durumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="f062d-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f062d-123">-InputObject</span></span>
<span data-ttu-id="f062d-124">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f062d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f062d-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="f062d-125">-Name</span></span>
<span data-ttu-id="f062d-126">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="f062d-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f062d-127">-ResourceGroupName</span></span>
<span data-ttu-id="f062d-128">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f062d-128">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f062d-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="f062d-129">-SubscriptionId</span></span>
<span data-ttu-id="f062d-130">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f062d-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f062d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f062d-131">CommonParameters</span></span>
<span data-ttu-id="f062d-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f062d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f062d-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f062d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f062d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f062d-134">INPUTS</span></span>

### <span data-ttu-id="f062d-135">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="f062d-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="f062d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f062d-136">OUTPUTS</span></span>

### <span data-ttu-id="f062d-137">Microsoft. Azure. PowerShell. cmdlet. zaman</span><span class="sxs-lookup"><span data-stu-id="f062d-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="f062d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f062d-138">NOTES</span></span>

<span data-ttu-id="f062d-139">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="f062d-139">ALIASES</span></span>

<span data-ttu-id="f062d-140">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="f062d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f062d-141">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f062d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f062d-142">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f062d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f062d-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="f062d-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f062d-144">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="f062d-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="f062d-145">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="f062d-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="f062d-146">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="f062d-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="f062d-147">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="f062d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f062d-148">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="f062d-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="f062d-149">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f062d-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="f062d-150">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f062d-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f062d-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f062d-151">RELATED LINKS</span></span>

