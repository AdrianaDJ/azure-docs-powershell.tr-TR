---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275417"
---
# <span data-ttu-id="cf921-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="cf921-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="cf921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf921-102">SYNOPSIS</span></span>
<span data-ttu-id="cf921-103">İşlev uygulaması planını siler.</span><span class="sxs-lookup"><span data-stu-id="cf921-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="cf921-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf921-104">SYNTAX</span></span>

### <span data-ttu-id="cf921-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf921-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cf921-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="cf921-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cf921-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf921-107">DESCRIPTION</span></span>
<span data-ttu-id="cf921-108">İşlev uygulaması planını siler.</span><span class="sxs-lookup"><span data-stu-id="cf921-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="cf921-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf921-109">EXAMPLES</span></span>

### <span data-ttu-id="cf921-110">Örnek 1: ada göre bir işlev uygulaması planı alın ve silin.</span><span class="sxs-lookup"><span data-stu-id="cf921-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="cf921-111">Bu komut bir işlev uygulaması planını ada göre alır ve siler.</span><span class="sxs-lookup"><span data-stu-id="cf921-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="cf921-112">Örnek 2: ada göre bir işlev uygulaması planını silme.</span><span class="sxs-lookup"><span data-stu-id="cf921-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="cf921-113">Bu komut bir işlev uygulaması planını ada göre siler.</span><span class="sxs-lookup"><span data-stu-id="cf921-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="cf921-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf921-114">PARAMETERS</span></span>

### <span data-ttu-id="cf921-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf921-115">-DefaultProfile</span></span>
<span data-ttu-id="cf921-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf921-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf921-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cf921-117">-Force</span></span>
<span data-ttu-id="cf921-118">Cmdlet 'i, onay istemeden işlev uygulaması planını kaldırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="cf921-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cf921-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf921-119">-InputObject</span></span>
<span data-ttu-id="cf921-120">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cf921-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf921-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cf921-121">-Name</span></span>
<span data-ttu-id="cf921-122">İşlev uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="cf921-122">The name of function app.</span></span>

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

### <span data-ttu-id="cf921-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cf921-123">-PassThru</span></span>
<span data-ttu-id="cf921-124">Komut başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="cf921-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="cf921-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf921-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="cf921-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="cf921-126">-SubscriptionId</span></span>
<span data-ttu-id="cf921-127">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cf921-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="cf921-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf921-128">-Confirm</span></span>
<span data-ttu-id="cf921-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf921-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf921-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf921-130">-WhatIf</span></span>
<span data-ttu-id="cf921-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf921-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf921-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf921-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf921-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf921-133">CommonParameters</span></span>
<span data-ttu-id="cf921-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf921-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf921-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cf921-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf921-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf921-136">INPUTS</span></span>

### <span data-ttu-id="cf921-137">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ıappserviceplan</span><span class="sxs-lookup"><span data-stu-id="cf921-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="cf921-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf921-138">OUTPUTS</span></span>

### <span data-ttu-id="cf921-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf921-139">System.Boolean</span></span>

## <span data-ttu-id="cf921-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf921-140">NOTES</span></span>

<span data-ttu-id="cf921-141">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="cf921-141">ALIASES</span></span>

<span data-ttu-id="cf921-142">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="cf921-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cf921-143">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cf921-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf921-144">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cf921-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cf921-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="cf921-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="cf921-146">`Location <String>`: Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="cf921-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="cf921-147">`[Kind <String>]`: Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="cf921-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="cf921-148">`[Tag <IResourceTags>]`: Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="cf921-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="cf921-149">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf921-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cf921-150">`[Capacity <Int32?>]`: Kaynağa atanmış geçerli örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="cf921-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="cf921-151">`[FreeOfferExpirationTime <DateTime?>]`: Sunucu grubunun ücretsiz teklifinin süresi dolduğunda geçen saat.</span><span class="sxs-lookup"><span data-stu-id="cf921-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="cf921-152">`[HostingEnvironmentProfileId <String>]`: App Service ortamının kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cf921-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="cf921-153">`[HyperV <Boolean?>]`: Hyper-V kapsayıcı uygulama hizmeti planı Eğer <code>true</code> değilse <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf921-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="cf921-154">`[IsSpot <Boolean?>]`: <code>true</code> Bu App Service planı, nokta örneklerinin sahibi.</span><span class="sxs-lookup"><span data-stu-id="cf921-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="cf921-155">`[IsXenon <Boolean?>]`: Geçersiz: Hyper-V kapsayıcı uygulama hizmeti planı varsa <code>true</code> , <code>false</code> Aksi halde.</span><span class="sxs-lookup"><span data-stu-id="cf921-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="cf921-156">`[MaximumElasticWorkerCount <Int32?>]`: Bu Eladascaleenabled App Service planı için izin verilen toplam çalışan sayısı üst sınırı</span><span class="sxs-lookup"><span data-stu-id="cf921-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="cf921-157">`[PerSiteScaling <Boolean?>]`: <code>true</code> Bu App Service planına atanmış uygulamalar bağımsız olarak ölçeklendirilemez.</span><span class="sxs-lookup"><span data-stu-id="cf921-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="cf921-158"><code>false</code>Bu App Service planına atanmış uygulamalar planın tüm örneklerine ölçeklendirecektir.</span><span class="sxs-lookup"><span data-stu-id="cf921-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="cf921-159">`[Reserved <Boolean?>]`: Linux App Service planı yoksa <code>true</code> <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="cf921-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="cf921-160">`[SkuCapability <ICapability[]>]`: SKU 'nun özellikleri, örneğin Traffic Manager 'ı etkinleştirmi?</span><span class="sxs-lookup"><span data-stu-id="cf921-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="cf921-161">`[Name <String>]`: SKU özelliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="cf921-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="cf921-162">`[Reason <String>]`: SKU özelliğinin nedeni.</span><span class="sxs-lookup"><span data-stu-id="cf921-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="cf921-163">`[Value <String>]`: SKU özelliğinin değeri.</span><span class="sxs-lookup"><span data-stu-id="cf921-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="cf921-164">`[SkuCapacityDefault <Int32?>]`: Bu App Service planı SKU 'SU için varsayılan çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="cf921-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="cf921-165">`[SkuCapacityMaximum <Int32?>]`: Bu App Service planı SKU 'sunda maksimum çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="cf921-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="cf921-166">`[SkuCapacityMinimum <Int32?>]`: Bu App Service planı SKU 'sunda en az çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="cf921-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="cf921-167">`[SkuCapacityScaleType <String>]`: Bir App Service planı için kullanılabilir ölçeklendirme yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="cf921-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="cf921-168">`[SkuFamily <String>]`: Kaynak SKU 'nun aile kodu.</span><span class="sxs-lookup"><span data-stu-id="cf921-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="cf921-169">`[SkuLocation <String[]>]`: SKU 'nun konumları.</span><span class="sxs-lookup"><span data-stu-id="cf921-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="cf921-170">`[SkuName <String>]`: Kaynak SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="cf921-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="cf921-171">`[SkuSize <String>]`: Kaynak SKU 'nun boyut belirticisi.</span><span class="sxs-lookup"><span data-stu-id="cf921-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="cf921-172">`[SkuTier <String>]`: Kaynak SKU 'nun hizmet katmanı.</span><span class="sxs-lookup"><span data-stu-id="cf921-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="cf921-173">`[SpotExpirationTime <DateTime?>]`: Sunucu grubunun süresi dolduğunda saat.</span><span class="sxs-lookup"><span data-stu-id="cf921-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="cf921-174">Yalnızca bir nokta sunucusu grubuysa geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="cf921-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="cf921-175">`[TargetWorkerCount <Int32?>]`: Çalışan sayısını ölçeklendirme.</span><span class="sxs-lookup"><span data-stu-id="cf921-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="cf921-176">`[TargetWorkerSizeId <Int32?>]`: Çalışan boyutu</span><span class="sxs-lookup"><span data-stu-id="cf921-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="cf921-177">`[WorkerTierName <String>]`: App Service planına atanan hedef çalışan katmanı.</span><span class="sxs-lookup"><span data-stu-id="cf921-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="cf921-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf921-178">RELATED LINKS</span></span>

