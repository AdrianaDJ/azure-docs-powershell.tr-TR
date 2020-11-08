---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275741"
---
# <span data-ttu-id="611bd-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="611bd-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="611bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="611bd-102">SYNOPSIS</span></span>
<span data-ttu-id="611bd-103">Belirtilen abonelik ve kaynak grubunda belirtilen ada sahip ortamı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="611bd-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="611bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="611bd-104">SYNTAX</span></span>

### <span data-ttu-id="611bd-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="611bd-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="611bd-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="611bd-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="611bd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="611bd-107">DESCRIPTION</span></span>
<span data-ttu-id="611bd-108">Belirtilen abonelik ve kaynak grubunda belirtilen ada sahip ortamı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="611bd-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="611bd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="611bd-109">EXAMPLES</span></span>

### <span data-ttu-id="611bd-110">Örnek 1: Gen1 saati</span><span class="sxs-lookup"><span data-stu-id="611bd-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

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
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="611bd-111">Bu komut, Gen1 saat serisi öngörülerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="611bd-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="611bd-112">Örnek 2: Gen1 saati</span><span class="sxs-lookup"><span data-stu-id="611bd-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

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
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="611bd-113">Bu komut, Gen1 saat serisi öngörülerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="611bd-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="611bd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="611bd-114">PARAMETERS</span></span>

### <span data-ttu-id="611bd-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="611bd-115">-AsJob</span></span>
<span data-ttu-id="611bd-116">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="611bd-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611bd-117">-DefaultProfile</span></span>
<span data-ttu-id="611bd-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="611bd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="611bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="611bd-119">-InputObject</span></span>
<span data-ttu-id="611bd-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="611bd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="611bd-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="611bd-121">-Name</span></span>
<span data-ttu-id="611bd-122">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="611bd-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="611bd-123">-NoWait</span></span>
<span data-ttu-id="611bd-124">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="611bd-124">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="611bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="611bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="611bd-126">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="611bd-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="611bd-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="611bd-127">-SubscriptionId</span></span>
<span data-ttu-id="611bd-128">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="611bd-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="611bd-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="611bd-129">-Tag</span></span>
<span data-ttu-id="611bd-130">Ortamdaki ek özelliklerin anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="611bd-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="611bd-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="611bd-131">-Confirm</span></span>
<span data-ttu-id="611bd-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="611bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="611bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="611bd-133">-WhatIf</span></span>
<span data-ttu-id="611bd-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="611bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="611bd-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="611bd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="611bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611bd-136">CommonParameters</span></span>
<span data-ttu-id="611bd-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="611bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611bd-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="611bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611bd-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="611bd-139">INPUTS</span></span>

### <span data-ttu-id="611bd-140">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="611bd-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="611bd-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="611bd-141">OUTPUTS</span></span>

### <span data-ttu-id="611bd-142">Microsoft. Azure. PowerShell. cmdlet. zaman</span><span class="sxs-lookup"><span data-stu-id="611bd-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="611bd-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="611bd-143">NOTES</span></span>

<span data-ttu-id="611bd-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="611bd-144">ALIASES</span></span>

<span data-ttu-id="611bd-145">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="611bd-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="611bd-146">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="611bd-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="611bd-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="611bd-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="611bd-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="611bd-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="611bd-149">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="611bd-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="611bd-150">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="611bd-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="611bd-151">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="611bd-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="611bd-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="611bd-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="611bd-153">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="611bd-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="611bd-154">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="611bd-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="611bd-155">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="611bd-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="611bd-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="611bd-156">RELATED LINKS</span></span>

