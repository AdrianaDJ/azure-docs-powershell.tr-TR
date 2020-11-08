---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: c7d8f46f42b1b42e4831540f5c68706c61ff78cf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276596"
---
# <span data-ttu-id="3d6e8-101">Get-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d6e8-101">Get-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="3d6e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6e8-103">Belirtilen ortamdaki belirtilen adla erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-103">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="3d6e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d6e8-104">SYNTAX</span></span>

### <span data-ttu-id="3d6e8-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d6e8-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d6e8-106">Al</span><span class="sxs-lookup"><span data-stu-id="3d6e8-106">Get</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d6e8-107">Getviaıdentity</span><span class="sxs-lookup"><span data-stu-id="3d6e8-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d6e8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d6e8-108">DESCRIPTION</span></span>
<span data-ttu-id="3d6e8-109">Belirtilen ortamdaki belirtilen adla erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-109">Gets the access policy with the specified name in the specified environment.</span></span>

## <span data-ttu-id="3d6e8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d6e8-110">EXAMPLES</span></span>

### <span data-ttu-id="3d6e8-111">Örnek 1: belirtilen ortamın altındaki tüm erişim ilkelerini listeleme</span><span class="sxs-lookup"><span data-stu-id="3d6e8-111">Example 1: List all access policies under a specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
policy002 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="3d6e8-112">Bu komut, belirli bir ortamın altındaki tüm erişim ilkelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-112">This command lists all access policies under a specified environment.</span></span>

### <span data-ttu-id="3d6e8-113">Örnek 2: adla belirtilen bir Access ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="3d6e8-113">Example 2: Get a specified access policy by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="3d6e8-114">Bu komut, belirtilen erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-114">This command gets a specified access policy.</span></span>

### <span data-ttu-id="3d6e8-115">Örnek 3: nesneye göre belirli bir Access ilkesi alma</span><span class="sxs-lookup"><span data-stu-id="3d6e8-115">Example 3: Get a specified access policy by object</span></span>
```powershell
PS C:\>$ap = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsi-envv8u56x -ResourceGroupName tsi-test-i01k5l -Name tsi-apilgj5y 
PS C:\>Get-AzTimeSeriesInsightsAccessPolicy -InputObject $ap

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="3d6e8-116">Bu komut, belirtilen erişim ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-116">This command gets a specified access policy.</span></span>

## <span data-ttu-id="3d6e8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d6e8-117">PARAMETERS</span></span>

### <span data-ttu-id="3d6e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d6e8-118">-DefaultProfile</span></span>
<span data-ttu-id="3d6e8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d6e8-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="3d6e8-120">-EnvironmentName</span></span>
<span data-ttu-id="3d6e8-121">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="3d6e8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d6e8-122">-InputObject</span></span>
<span data-ttu-id="3d6e8-123">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3d6e8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d6e8-124">-Name</span></span>
<span data-ttu-id="3d6e8-125">Belirtilen ortamla ilişkili saat serisi öngörüleri erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-125">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d6e8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d6e8-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d6e8-127">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="3d6e8-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3d6e8-128">-SubscriptionId</span></span>
<span data-ttu-id="3d6e8-129">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3d6e8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6e8-130">CommonParameters</span></span>
<span data-ttu-id="3d6e8-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6e8-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6e8-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d6e8-133">INPUTS</span></span>

### <span data-ttu-id="3d6e8-134">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="3d6e8-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d6e8-135">OUTPUTS</span></span>

### <span data-ttu-id="3d6e8-136">Microsoft. Azure. PowerShell. cmdlet. zaman</span><span class="sxs-lookup"><span data-stu-id="3d6e8-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="3d6e8-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d6e8-137">NOTES</span></span>

<span data-ttu-id="3d6e8-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="3d6e8-138">ALIASES</span></span>

<span data-ttu-id="3d6e8-139">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="3d6e8-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d6e8-140">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d6e8-141">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d6e8-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="3d6e8-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d6e8-143">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="3d6e8-144">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="3d6e8-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="3d6e8-145">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="3d6e8-146">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="3d6e8-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d6e8-147">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="3d6e8-148">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="3d6e8-149">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3d6e8-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="3d6e8-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d6e8-150">RELATED LINKS</span></span>

