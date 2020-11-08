---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268927"
---
# <span data-ttu-id="82609-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="82609-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="82609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82609-102">SYNOPSIS</span></span>
<span data-ttu-id="82609-103">Belirtilen ortamdaki belirtilen adla başvuru veri kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="82609-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="82609-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82609-104">SYNTAX</span></span>

### <span data-ttu-id="82609-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="82609-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="82609-106">Al</span><span class="sxs-lookup"><span data-stu-id="82609-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="82609-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="82609-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="82609-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="82609-108">DESCRIPTION</span></span>
<span data-ttu-id="82609-109">Belirtilen ortamdaki belirtilen adla başvuru veri kümesini alır.</span><span class="sxs-lookup"><span data-stu-id="82609-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="82609-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82609-110">EXAMPLES</span></span>

### <span data-ttu-id="82609-111">Örnek 1: belirtilen ortamın altındaki tüm başvuru veri kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="82609-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="82609-112">Bu komut, belirtilen ortamdaki tüm başvuru veri kümelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="82609-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="82609-113">Örnek 2: adla ayarlanan bir başvuru verilerini alma</span><span class="sxs-lookup"><span data-stu-id="82609-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="82609-114">Bu komut, belirli bir başvuru verileri kümesi alır.</span><span class="sxs-lookup"><span data-stu-id="82609-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="82609-115">Örnek 3: nesne kümesi</span><span class="sxs-lookup"><span data-stu-id="82609-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="82609-116">Bu komut, belirli bir başvuru verileri kümesi alır.</span><span class="sxs-lookup"><span data-stu-id="82609-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="82609-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82609-117">PARAMETERS</span></span>

### <span data-ttu-id="82609-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82609-118">-DefaultProfile</span></span>
<span data-ttu-id="82609-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82609-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82609-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="82609-120">-EnvironmentName</span></span>
<span data-ttu-id="82609-121">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="82609-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="82609-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82609-122">-InputObject</span></span>
<span data-ttu-id="82609-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="82609-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="82609-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="82609-124">-Name</span></span>
<span data-ttu-id="82609-125">Belirtilen ortamla ilişkili saat serisi öngörüleri başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="82609-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82609-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82609-126">-ResourceGroupName</span></span>
<span data-ttu-id="82609-127">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="82609-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="82609-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="82609-128">-SubscriptionId</span></span>
<span data-ttu-id="82609-129">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="82609-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="82609-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82609-130">CommonParameters</span></span>
<span data-ttu-id="82609-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82609-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82609-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="82609-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82609-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82609-133">INPUTS</span></span>

### <span data-ttu-id="82609-134">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="82609-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="82609-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82609-135">OUTPUTS</span></span>

### <span data-ttu-id="82609-136">Microsoft. Azure. PowerShell. cmdlet. zaman</span><span class="sxs-lookup"><span data-stu-id="82609-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="82609-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82609-137">NOTES</span></span>

<span data-ttu-id="82609-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="82609-138">ALIASES</span></span>

<span data-ttu-id="82609-139">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="82609-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="82609-140">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="82609-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="82609-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="82609-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="82609-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="82609-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="82609-143">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="82609-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="82609-144">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="82609-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="82609-145">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="82609-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="82609-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="82609-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="82609-147">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="82609-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="82609-148">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="82609-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="82609-149">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="82609-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="82609-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82609-150">RELATED LINKS</span></span>

