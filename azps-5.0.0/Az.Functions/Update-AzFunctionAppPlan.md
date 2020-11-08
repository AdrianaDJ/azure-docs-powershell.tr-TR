---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275404"
---
# <span data-ttu-id="6b516-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="6b516-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="6b516-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b516-102">SYNOPSIS</span></span>
<span data-ttu-id="6b516-103">Bir işlev App Service planını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b516-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="6b516-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b516-104">SYNTAX</span></span>

### <span data-ttu-id="6b516-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b516-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6b516-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="6b516-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b516-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b516-107">DESCRIPTION</span></span>
<span data-ttu-id="6b516-108">Bir işlev App Service planını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6b516-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="6b516-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b516-109">EXAMPLES</span></span>

### <span data-ttu-id="6b516-110">Örnek 1: bir App Service planını yirmimaksimum çalışanı olan SKU 'yu EP2.</span><span class="sxs-lookup"><span data-stu-id="6b516-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="6b516-111">Bu komut, bir App Service planını yirmimaksimum çalışan SKU 'yu EP2.</span><span class="sxs-lookup"><span data-stu-id="6b516-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="6b516-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b516-112">PARAMETERS</span></span>

### <span data-ttu-id="6b516-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="6b516-113">-AsJob</span></span>
<span data-ttu-id="6b516-114">Komutu iş olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="6b516-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="6b516-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b516-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="6b516-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b516-116">-InputObject</span></span>
<span data-ttu-id="6b516-117">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b516-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b516-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="6b516-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="6b516-119">App Service planı için en fazla çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="6b516-119">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b516-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="6b516-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="6b516-121">App Service planı için en az çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="6b516-121">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b516-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b516-122">-Name</span></span>
<span data-ttu-id="6b516-123">App Service planının adı.</span><span class="sxs-lookup"><span data-stu-id="6b516-123">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b516-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6b516-124">-NoWait</span></span>
<span data-ttu-id="6b516-125">Komutu zaman uyumsuz olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="6b516-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="6b516-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b516-126">-ResourceGroupName</span></span>
<span data-ttu-id="6b516-127">Kaynağın ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6b516-127">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b516-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="6b516-128">-Sku</span></span>
<span data-ttu-id="6b516-129">Plan SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="6b516-129">The plan sku.</span></span>
<span data-ttu-id="6b516-130">Geçerli girdiler: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="6b516-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="6b516-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6b516-131">-SubscriptionId</span></span>
<span data-ttu-id="6b516-132">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6b516-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b516-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6b516-133">-Tag</span></span>
<span data-ttu-id="6b516-134">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="6b516-134">Resource tags.</span></span>

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

### <span data-ttu-id="6b516-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b516-135">-Confirm</span></span>
<span data-ttu-id="6b516-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b516-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b516-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b516-137">-WhatIf</span></span>
<span data-ttu-id="6b516-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b516-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b516-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b516-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b516-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b516-140">CommonParameters</span></span>
<span data-ttu-id="6b516-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b516-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b516-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6b516-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b516-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b516-143">INPUTS</span></span>

### <span data-ttu-id="6b516-144">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ıappserviceplan</span><span class="sxs-lookup"><span data-stu-id="6b516-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="6b516-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b516-145">OUTPUTS</span></span>

### <span data-ttu-id="6b516-146">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ıappserviceplan</span><span class="sxs-lookup"><span data-stu-id="6b516-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="6b516-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b516-147">NOTES</span></span>

<span data-ttu-id="6b516-148">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6b516-148">ALIASES</span></span>

<span data-ttu-id="6b516-149">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="6b516-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b516-150">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b516-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b516-151">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b516-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b516-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="6b516-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="6b516-153">`Location <String>`: Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="6b516-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="6b516-154">`[Kind <String>]`: Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="6b516-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="6b516-155">`[Tag <IResourceTags>]`: Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="6b516-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="6b516-156">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b516-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="6b516-157">`[Capacity <Int32?>]`: Kaynağa atanmış geçerli örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="6b516-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="6b516-158">`[FreeOfferExpirationTime <DateTime?>]`: Sunucu grubunun ücretsiz teklifinin süresi dolduğunda geçen saat.</span><span class="sxs-lookup"><span data-stu-id="6b516-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="6b516-159">`[HostingEnvironmentProfileId <String>]`: App Service ortamının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6b516-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="6b516-160">`[HyperV <Boolean?>]`: Hyper-V kapsayıcı uygulama hizmeti planı Eğer <code>true</code> değilse <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="6b516-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="6b516-161">`[IsSpot <Boolean?>]`: <code>true</code> Bu App Service planı, nokta örneklerinin sahibi.</span><span class="sxs-lookup"><span data-stu-id="6b516-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="6b516-162">`[IsXenon <Boolean?>]`: Geçersiz: Hyper-V kapsayıcı uygulama hizmeti planı varsa <code>true</code> , <code>false</code> Aksi halde.</span><span class="sxs-lookup"><span data-stu-id="6b516-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="6b516-163">`[MaximumElasticWorkerCount <Int32?>]`: Bu Eladascaleenabled App Service planı için izin verilen toplam çalışan sayısı üst sınırı</span><span class="sxs-lookup"><span data-stu-id="6b516-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="6b516-164">`[PerSiteScaling <Boolean?>]`: <code>true</code> Bu App Service planına atanmış uygulamalar bağımsız olarak ölçeklendirilemez.</span><span class="sxs-lookup"><span data-stu-id="6b516-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="6b516-165"><code>false</code>Bu App Service planına atanmış uygulamalar planın tüm örneklerine ölçeklendirecektir.</span><span class="sxs-lookup"><span data-stu-id="6b516-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="6b516-166">`[Reserved <Boolean?>]`: Linux App Service planı yoksa <code>true</code> <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="6b516-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="6b516-167">`[SkuCapability <ICapability[]>]`: SKU 'nun özellikleri, örneğin Traffic Manager 'ı etkinleştirmi?</span><span class="sxs-lookup"><span data-stu-id="6b516-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="6b516-168">`[Name <String>]`: SKU özelliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="6b516-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="6b516-169">`[Reason <String>]`: SKU özelliğinin nedeni.</span><span class="sxs-lookup"><span data-stu-id="6b516-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="6b516-170">`[Value <String>]`: SKU özelliğinin değeri.</span><span class="sxs-lookup"><span data-stu-id="6b516-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="6b516-171">`[SkuCapacityDefault <Int32?>]`: Bu App Service planı SKU 'SU için varsayılan çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="6b516-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="6b516-172">`[SkuCapacityMaximum <Int32?>]`: Bu App Service planı SKU 'sunda maksimum çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="6b516-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="6b516-173">`[SkuCapacityMinimum <Int32?>]`: Bu App Service planı SKU 'sunda en az çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="6b516-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="6b516-174">`[SkuCapacityScaleType <String>]`: Bir App Service planı için kullanılabilir ölçeklendirme yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="6b516-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="6b516-175">`[SkuFamily <String>]`: Kaynak SKU 'nun aile kodu.</span><span class="sxs-lookup"><span data-stu-id="6b516-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="6b516-176">`[SkuLocation <String[]>]`: SKU 'nun konumları.</span><span class="sxs-lookup"><span data-stu-id="6b516-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="6b516-177">`[SkuName <String>]`: Kaynak SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="6b516-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="6b516-178">`[SkuSize <String>]`: Kaynak SKU 'nun boyut belirticisi.</span><span class="sxs-lookup"><span data-stu-id="6b516-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="6b516-179">`[SkuTier <String>]`: Kaynak SKU 'nun hizmet katmanı.</span><span class="sxs-lookup"><span data-stu-id="6b516-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="6b516-180">`[SpotExpirationTime <DateTime?>]`: Sunucu grubunun süresi dolduğunda saat.</span><span class="sxs-lookup"><span data-stu-id="6b516-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="6b516-181">Yalnızca bir nokta sunucusu grubuysa geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="6b516-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="6b516-182">`[TargetWorkerCount <Int32?>]`: Çalışan sayısını ölçeklendirme.</span><span class="sxs-lookup"><span data-stu-id="6b516-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="6b516-183">`[TargetWorkerSizeId <Int32?>]`: Çalışan boyutu</span><span class="sxs-lookup"><span data-stu-id="6b516-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="6b516-184">`[WorkerTierName <String>]`: App Service planına atanan hedef çalışan katmanı.</span><span class="sxs-lookup"><span data-stu-id="6b516-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="6b516-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b516-185">RELATED LINKS</span></span>

