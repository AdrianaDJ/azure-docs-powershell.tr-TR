---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322591"
---
# <span data-ttu-id="d766e-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="d766e-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="d766e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d766e-102">SYNOPSIS</span></span>
<span data-ttu-id="d766e-103">Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki olay kaynağını siler</span><span class="sxs-lookup"><span data-stu-id="d766e-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="d766e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d766e-104">SYNTAX</span></span>

### <span data-ttu-id="d766e-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d766e-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d766e-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="d766e-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d766e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d766e-107">DESCRIPTION</span></span>
<span data-ttu-id="d766e-108">Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki olay kaynağını siler</span><span class="sxs-lookup"><span data-stu-id="d766e-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="d766e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d766e-109">EXAMPLES</span></span>

### <span data-ttu-id="d766e-110">Örnek 1: belirtilen olay kaynağını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="d766e-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="d766e-111">Bu, belirli bir olay kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d766e-111">This removes a specific event source.</span></span>

### <span data-ttu-id="d766e-112">Örnek 2: belirli bir olay kaynağını nesne ile kaldırma</span><span class="sxs-lookup"><span data-stu-id="d766e-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="d766e-113">Bu, belirli bir olay kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d766e-113">This removes a specific event source.</span></span>

## <span data-ttu-id="d766e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d766e-114">PARAMETERS</span></span>

### <span data-ttu-id="d766e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d766e-115">-DefaultProfile</span></span>
<span data-ttu-id="d766e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d766e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d766e-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="d766e-117">-EnvironmentName</span></span>
<span data-ttu-id="d766e-118">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="d766e-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d766e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d766e-119">-InputObject</span></span>
<span data-ttu-id="d766e-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d766e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d766e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d766e-121">-Name</span></span>
<span data-ttu-id="d766e-122">Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d766e-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d766e-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d766e-123">-PassThru</span></span>
<span data-ttu-id="d766e-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="d766e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d766e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d766e-125">-ResourceGroupName</span></span>
<span data-ttu-id="d766e-126">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d766e-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d766e-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d766e-127">-SubscriptionId</span></span>
<span data-ttu-id="d766e-128">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d766e-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d766e-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="d766e-129">-Confirm</span></span>
<span data-ttu-id="d766e-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d766e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d766e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d766e-131">-WhatIf</span></span>
<span data-ttu-id="d766e-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d766e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d766e-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d766e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d766e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d766e-134">CommonParameters</span></span>
<span data-ttu-id="d766e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d766e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d766e-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d766e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d766e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d766e-137">INPUTS</span></span>

### <span data-ttu-id="d766e-138">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="d766e-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="d766e-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d766e-139">OUTPUTS</span></span>

### <span data-ttu-id="d766e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d766e-140">System.Boolean</span></span>

## <span data-ttu-id="d766e-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d766e-141">NOTES</span></span>

<span data-ttu-id="d766e-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="d766e-142">ALIASES</span></span>

<span data-ttu-id="d766e-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="d766e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d766e-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d766e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d766e-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d766e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d766e-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="d766e-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d766e-147">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d766e-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="d766e-148">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="d766e-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="d766e-149">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="d766e-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="d766e-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="d766e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d766e-151">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="d766e-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="d766e-152">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d766e-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="d766e-153">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d766e-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d766e-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d766e-154">RELATED LINKS</span></span>

