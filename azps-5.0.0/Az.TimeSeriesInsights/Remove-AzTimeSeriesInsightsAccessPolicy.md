---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276496"
---
# <span data-ttu-id="54685-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="54685-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="54685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54685-102">SYNOPSIS</span></span>
<span data-ttu-id="54685-103">Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki erişim ilkesini siler</span><span class="sxs-lookup"><span data-stu-id="54685-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="54685-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54685-104">SYNTAX</span></span>

### <span data-ttu-id="54685-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54685-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="54685-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="54685-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="54685-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="54685-107">DESCRIPTION</span></span>
<span data-ttu-id="54685-108">Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki erişim ilkesini siler</span><span class="sxs-lookup"><span data-stu-id="54685-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="54685-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54685-109">EXAMPLES</span></span>

### <span data-ttu-id="54685-110">Örnek 1: belirtilen bir Access ilkesini ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="54685-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="54685-111">Bu komut belirtilen Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="54685-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="54685-112">Örnek 2: nesne ile belirtilen bir Access ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="54685-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="54685-113">Bu komut belirtilen Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="54685-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="54685-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54685-114">PARAMETERS</span></span>

### <span data-ttu-id="54685-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54685-115">-DefaultProfile</span></span>
<span data-ttu-id="54685-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54685-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54685-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="54685-117">-EnvironmentName</span></span>
<span data-ttu-id="54685-118">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="54685-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="54685-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54685-119">-InputObject</span></span>
<span data-ttu-id="54685-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54685-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="54685-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="54685-121">-Name</span></span>
<span data-ttu-id="54685-122">Belirtilen ortamla ilişkili saat serisi öngörüleri erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="54685-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54685-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="54685-123">-PassThru</span></span>
<span data-ttu-id="54685-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="54685-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="54685-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54685-125">-ResourceGroupName</span></span>
<span data-ttu-id="54685-126">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="54685-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="54685-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="54685-127">-SubscriptionId</span></span>
<span data-ttu-id="54685-128">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="54685-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="54685-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="54685-129">-Confirm</span></span>
<span data-ttu-id="54685-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54685-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54685-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54685-131">-WhatIf</span></span>
<span data-ttu-id="54685-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54685-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54685-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54685-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54685-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54685-134">CommonParameters</span></span>
<span data-ttu-id="54685-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54685-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54685-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="54685-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54685-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54685-137">INPUTS</span></span>

### <span data-ttu-id="54685-138">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="54685-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="54685-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54685-139">OUTPUTS</span></span>

### <span data-ttu-id="54685-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="54685-140">System.Boolean</span></span>

## <span data-ttu-id="54685-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54685-141">NOTES</span></span>

<span data-ttu-id="54685-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="54685-142">ALIASES</span></span>

<span data-ttu-id="54685-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="54685-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="54685-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="54685-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="54685-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="54685-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="54685-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="54685-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="54685-147">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="54685-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="54685-148">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="54685-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="54685-149">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="54685-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="54685-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="54685-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="54685-151">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="54685-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="54685-152">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="54685-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="54685-153">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="54685-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="54685-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54685-154">RELATED LINKS</span></span>

