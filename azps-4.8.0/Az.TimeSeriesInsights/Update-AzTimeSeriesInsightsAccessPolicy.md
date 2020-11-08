---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: e776b0e11fedd0b2903135b9b640c3b704706027
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267952"
---
# <span data-ttu-id="7ce1b-101">Update-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce1b-101">Update-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="7ce1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ce1b-102">SYNOPSIS</span></span>
<span data-ttu-id="7ce1b-103">Belirtilen abonelikte, kaynak grubunda ve ortamda belirtilen adla erişim ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-103">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="7ce1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ce1b-104">SYNTAX</span></span>

### <span data-ttu-id="7ce1b-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ce1b-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7ce1b-106">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="7ce1b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity> [-Description <String>]
 [-Role <AccessPolicyRole[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7ce1b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ce1b-107">DESCRIPTION</span></span>
<span data-ttu-id="7ce1b-108">Belirtilen abonelikte, kaynak grubunda ve ortamda belirtilen adla erişim ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-108">Updates the access policy with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="7ce1b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ce1b-109">EXAMPLES</span></span>

### <span data-ttu-id="7ce1b-110">Örnek 1: belirtilen Access ilkesini adıyla güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7ce1b-110">Example 1: Update a specified access policy by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup -Role Contributor,Reader

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="7ce1b-111">Bu komut belirtilen bir Access ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-111">This command updates a specified access policy.</span></span>

### <span data-ttu-id="7ce1b-112">Örnek 2: nesne ile belirtilen bir Access ilkesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7ce1b-112">Example 2: Update a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name policy001
PS C:\> Update-AzTimeSeriesInsightsAccessPolicy -InputObject $policy -Role Contributor

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="7ce1b-113">Bu komut belirtilen bir Access ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-113">This command updates a specified access policy.</span></span>

## <span data-ttu-id="7ce1b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ce1b-114">PARAMETERS</span></span>

### <span data-ttu-id="7ce1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ce1b-115">-DefaultProfile</span></span>
<span data-ttu-id="7ce1b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ce1b-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7ce1b-117">-Description</span></span>
<span data-ttu-id="7ce1b-118">Access ilkesinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-118">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce1b-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="7ce1b-119">-EnvironmentName</span></span>
<span data-ttu-id="7ce1b-120">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="7ce1b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ce1b-121">-InputObject</span></span>
<span data-ttu-id="7ce1b-122">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7ce1b-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ce1b-123">-Name</span></span>
<span data-ttu-id="7ce1b-124">Belirtilen ortamla ilişkili saat serisi öngörüleri erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-124">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce1b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ce1b-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ce1b-126">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="7ce1b-127">-Role</span><span class="sxs-lookup"><span data-stu-id="7ce1b-127">-Role</span></span>
<span data-ttu-id="7ce1b-128">Anapara atanan rollerin listesi.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-128">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ce1b-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7ce1b-129">-SubscriptionId</span></span>
<span data-ttu-id="7ce1b-130">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7ce1b-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ce1b-131">-Confirm</span></span>
<span data-ttu-id="7ce1b-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ce1b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ce1b-133">-WhatIf</span></span>
<span data-ttu-id="7ce1b-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ce1b-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ce1b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ce1b-136">CommonParameters</span></span>
<span data-ttu-id="7ce1b-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ce1b-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ce1b-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ce1b-139">INPUTS</span></span>

### <span data-ttu-id="7ce1b-140">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="7ce1b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ce1b-141">OUTPUTS</span></span>

### <span data-ttu-id="7ce1b-142">Microsoft. Azure. PowerShell. cmdlet. zaman</span><span class="sxs-lookup"><span data-stu-id="7ce1b-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="7ce1b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ce1b-143">NOTES</span></span>

<span data-ttu-id="7ce1b-144">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="7ce1b-144">ALIASES</span></span>

<span data-ttu-id="7ce1b-145">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="7ce1b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7ce1b-146">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7ce1b-147">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7ce1b-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="7ce1b-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7ce1b-149">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="7ce1b-150">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="7ce1b-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="7ce1b-151">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="7ce1b-152">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="7ce1b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7ce1b-153">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="7ce1b-154">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="7ce1b-155">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7ce1b-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="7ce1b-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ce1b-156">RELATED LINKS</span></span>

