---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266194"
---
# <span data-ttu-id="37478-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="37478-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="37478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37478-102">SYNOPSIS</span></span>
<span data-ttu-id="37478-103">Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki başvuru verileri kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="37478-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="37478-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37478-104">SYNTAX</span></span>

### <span data-ttu-id="37478-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37478-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="37478-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="37478-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37478-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="37478-107">DESCRIPTION</span></span>
<span data-ttu-id="37478-108">Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki başvuru verileri kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="37478-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="37478-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37478-109">EXAMPLES</span></span>

### <span data-ttu-id="37478-110">Örnek 1: belirtilen başvuru verilerini adla ayarlama</span><span class="sxs-lookup"><span data-stu-id="37478-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="37478-111">Bu komut belirtilen başvuru veri kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="37478-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="37478-112">Örnek 2: belirtilen başvuru verilerini nesne bazında güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="37478-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="37478-113">Bu komut belirtilen başvuru veri kümesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="37478-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="37478-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37478-114">PARAMETERS</span></span>

### <span data-ttu-id="37478-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37478-115">-DefaultProfile</span></span>
<span data-ttu-id="37478-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37478-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37478-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="37478-117">-EnvironmentName</span></span>
<span data-ttu-id="37478-118">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="37478-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="37478-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37478-119">-InputObject</span></span>
<span data-ttu-id="37478-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37478-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="37478-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="37478-121">-Name</span></span>
<span data-ttu-id="37478-122">Belirtilen ortamla ilişkili saat serisi öngörüleri başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="37478-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37478-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37478-123">-ResourceGroupName</span></span>
<span data-ttu-id="37478-124">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="37478-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="37478-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="37478-125">-SubscriptionId</span></span>
<span data-ttu-id="37478-126">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="37478-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="37478-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="37478-127">-Tag</span></span>
<span data-ttu-id="37478-128">Başvuru verileri kümesi için ek özelliklerin anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="37478-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="37478-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="37478-129">-Confirm</span></span>
<span data-ttu-id="37478-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="37478-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37478-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37478-131">-WhatIf</span></span>
<span data-ttu-id="37478-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37478-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37478-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="37478-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37478-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37478-134">CommonParameters</span></span>
<span data-ttu-id="37478-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37478-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37478-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="37478-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37478-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37478-137">INPUTS</span></span>

### <span data-ttu-id="37478-138">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="37478-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="37478-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37478-139">OUTPUTS</span></span>

### <span data-ttu-id="37478-140">Microsoft. Azure. PowerShell. cmdlet. zaman</span><span class="sxs-lookup"><span data-stu-id="37478-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="37478-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37478-141">NOTES</span></span>

<span data-ttu-id="37478-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="37478-142">ALIASES</span></span>

<span data-ttu-id="37478-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="37478-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="37478-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="37478-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37478-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37478-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="37478-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="37478-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37478-147">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="37478-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="37478-148">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="37478-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="37478-149">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="37478-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="37478-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="37478-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37478-151">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="37478-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="37478-152">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="37478-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="37478-153">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="37478-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="37478-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37478-154">RELATED LINKS</span></span>

