---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 8b56475d2510099b7873fa444a0dc78497aeb729
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268627"
---
# <span data-ttu-id="301c9-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="301c9-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="301c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="301c9-102">SYNOPSIS</span></span>
<span data-ttu-id="301c9-103">Belirtilen abonelik ve kaynak grubundaki belirtilen ada sahip ortamı siler.</span><span class="sxs-lookup"><span data-stu-id="301c9-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="301c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="301c9-104">SYNTAX</span></span>

### <span data-ttu-id="301c9-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="301c9-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="301c9-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="301c9-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="301c9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="301c9-107">DESCRIPTION</span></span>
<span data-ttu-id="301c9-108">Belirtilen abonelik ve kaynak grubundaki belirtilen ada sahip ortamı siler.</span><span class="sxs-lookup"><span data-stu-id="301c9-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="301c9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="301c9-109">EXAMPLES</span></span>

### <span data-ttu-id="301c9-110">Örnek 1: zaman serisi Insights ortamını ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="301c9-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="301c9-111">Bu komut, zaman serisi Öngörüler ortamını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="301c9-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="301c9-112">Örnek 2: nesne bazında bir zaman serisi Öngörüler ortamını kaldırma</span><span class="sxs-lookup"><span data-stu-id="301c9-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="301c9-113">Bu komut, zaman serisi Öngörüler ortamını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="301c9-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="301c9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="301c9-114">PARAMETERS</span></span>

### <span data-ttu-id="301c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301c9-115">-DefaultProfile</span></span>
<span data-ttu-id="301c9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="301c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="301c9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="301c9-117">-InputObject</span></span>
<span data-ttu-id="301c9-118">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="301c9-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="301c9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="301c9-119">-Name</span></span>
<span data-ttu-id="301c9-120">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="301c9-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c9-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="301c9-121">-PassThru</span></span>
<span data-ttu-id="301c9-122">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="301c9-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="301c9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301c9-123">-ResourceGroupName</span></span>
<span data-ttu-id="301c9-124">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="301c9-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="301c9-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="301c9-125">-SubscriptionId</span></span>
<span data-ttu-id="301c9-126">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="301c9-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="301c9-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="301c9-127">-Confirm</span></span>
<span data-ttu-id="301c9-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="301c9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301c9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301c9-129">-WhatIf</span></span>
<span data-ttu-id="301c9-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="301c9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301c9-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="301c9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301c9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301c9-132">CommonParameters</span></span>
<span data-ttu-id="301c9-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="301c9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301c9-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="301c9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301c9-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="301c9-135">INPUTS</span></span>

### <span data-ttu-id="301c9-136">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="301c9-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="301c9-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="301c9-137">OUTPUTS</span></span>

### <span data-ttu-id="301c9-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="301c9-138">System.Boolean</span></span>

## <span data-ttu-id="301c9-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="301c9-139">NOTES</span></span>

<span data-ttu-id="301c9-140">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="301c9-140">ALIASES</span></span>

<span data-ttu-id="301c9-141">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="301c9-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="301c9-142">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="301c9-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="301c9-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="301c9-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="301c9-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="301c9-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="301c9-145">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="301c9-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="301c9-146">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="301c9-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="301c9-147">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="301c9-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="301c9-148">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="301c9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="301c9-149">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="301c9-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="301c9-150">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="301c9-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="301c9-151">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="301c9-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="301c9-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="301c9-152">RELATED LINKS</span></span>

