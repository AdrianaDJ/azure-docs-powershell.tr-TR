---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266196"
---
# <span data-ttu-id="5274f-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="5274f-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="5274f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5274f-102">SYNOPSIS</span></span>
<span data-ttu-id="5274f-103">Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki başvuru verileri kümesini siler</span><span class="sxs-lookup"><span data-stu-id="5274f-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="5274f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5274f-104">SYNTAX</span></span>

### <span data-ttu-id="5274f-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5274f-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5274f-106">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="5274f-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5274f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5274f-107">DESCRIPTION</span></span>
<span data-ttu-id="5274f-108">Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki başvuru verileri kümesini siler</span><span class="sxs-lookup"><span data-stu-id="5274f-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="5274f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5274f-109">EXAMPLES</span></span>

### <span data-ttu-id="5274f-110">Örnek 1: belirtilen başvuru verilerini adla ayarlayarak kaldırma</span><span class="sxs-lookup"><span data-stu-id="5274f-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="5274f-111">Bu komut, belirtilen başvuru veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5274f-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="5274f-112">Örnek 2: nesne kümesini belirtilen başvuru verilerini kaldırma</span><span class="sxs-lookup"><span data-stu-id="5274f-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="5274f-113">Bu komut, belirtilen başvuru veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5274f-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="5274f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5274f-114">PARAMETERS</span></span>

### <span data-ttu-id="5274f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5274f-115">-DefaultProfile</span></span>
<span data-ttu-id="5274f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5274f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5274f-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="5274f-117">-EnvironmentName</span></span>
<span data-ttu-id="5274f-118">Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.</span><span class="sxs-lookup"><span data-stu-id="5274f-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="5274f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5274f-119">-InputObject</span></span>
<span data-ttu-id="5274f-120">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5274f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5274f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5274f-121">-Name</span></span>
<span data-ttu-id="5274f-122">Belirtilen ortamla ilişkili saat serisi öngörüleri başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="5274f-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5274f-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5274f-123">-PassThru</span></span>
<span data-ttu-id="5274f-124">Komut başarılı olduğunda doğru verir</span><span class="sxs-lookup"><span data-stu-id="5274f-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5274f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5274f-125">-ResourceGroupName</span></span>
<span data-ttu-id="5274f-126">Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5274f-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="5274f-127">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5274f-127">-SubscriptionId</span></span>
<span data-ttu-id="5274f-128">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5274f-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5274f-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5274f-129">-Confirm</span></span>
<span data-ttu-id="5274f-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5274f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5274f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5274f-131">-WhatIf</span></span>
<span data-ttu-id="5274f-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5274f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5274f-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5274f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5274f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5274f-134">CommonParameters</span></span>
<span data-ttu-id="5274f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5274f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5274f-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5274f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5274f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5274f-137">INPUTS</span></span>

### <span data-ttu-id="5274f-138">Microsoft. Azure. PowerShell. cmdlet. W32.</span><span class="sxs-lookup"><span data-stu-id="5274f-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="5274f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5274f-139">OUTPUTS</span></span>

### <span data-ttu-id="5274f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5274f-140">System.Boolean</span></span>

## <span data-ttu-id="5274f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5274f-141">NOTES</span></span>

<span data-ttu-id="5274f-142">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5274f-142">ALIASES</span></span>

<span data-ttu-id="5274f-143">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="5274f-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5274f-144">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5274f-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5274f-145">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5274f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5274f-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="5274f-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5274f-147">`[AccessPolicyName <String>]`: Erişim ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="5274f-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="5274f-148">`[EnvironmentName <String>]`: Ortamın adı</span><span class="sxs-lookup"><span data-stu-id="5274f-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="5274f-149">`[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="5274f-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="5274f-150">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="5274f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5274f-151">`[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="5274f-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="5274f-152">`[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5274f-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="5274f-153">`[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5274f-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="5274f-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5274f-154">RELATED LINKS</span></span>

