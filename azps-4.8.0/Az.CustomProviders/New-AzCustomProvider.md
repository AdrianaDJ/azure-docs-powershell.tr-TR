---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274600"
---
# <span data-ttu-id="890b6-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="890b6-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="890b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="890b6-102">SYNOPSIS</span></span>
<span data-ttu-id="890b6-103">Özel kaynak sağlayıcısını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="890b6-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="890b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="890b6-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="890b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="890b6-105">DESCRIPTION</span></span>
<span data-ttu-id="890b6-106">Özel kaynak sağlayıcısını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="890b6-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="890b6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="890b6-107">EXAMPLES</span></span>

### <span data-ttu-id="890b6-108">Örnek 1: özel sağlayıcı oluşturma</span><span class="sxs-lookup"><span data-stu-id="890b6-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="890b6-109">Özel kaynak sağlayıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="890b6-109">Create a custom resource provider</span></span>

### <span data-ttu-id="890b6-110">Örnek 2: ilişkilendirmelere sahip özel bir sağlayıcı oluşturma</span><span class="sxs-lookup"><span data-stu-id="890b6-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="890b6-111">Özel sağlayıcı ilişkilendirmeleri için yol içeren özel bir sağlayıcı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="890b6-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="890b6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="890b6-112">PARAMETERS</span></span>

### <span data-ttu-id="890b6-113">-Eylem</span><span class="sxs-lookup"><span data-stu-id="890b6-113">-Action</span></span>
<span data-ttu-id="890b6-114">Özel kaynak sağlayıcısının uyguladığı eylemlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="890b6-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="890b6-115">Oluşturmak için, eylem özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="890b6-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890b6-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="890b6-116">-AsJob</span></span>
<span data-ttu-id="890b6-117">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="890b6-117">Run the command as a job</span></span>

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

### <span data-ttu-id="890b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890b6-118">-DefaultProfile</span></span>
<span data-ttu-id="890b6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="890b6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="890b6-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="890b6-120">-Location</span></span>
<span data-ttu-id="890b6-121">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="890b6-121">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890b6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="890b6-122">-Name</span></span>
<span data-ttu-id="890b6-123">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="890b6-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890b6-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="890b6-124">-NoWait</span></span>
<span data-ttu-id="890b6-125">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="890b6-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="890b6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="890b6-126">-ResourceGroupName</span></span>
<span data-ttu-id="890b6-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="890b6-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890b6-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="890b6-128">-ResourceType</span></span>
<span data-ttu-id="890b6-129">Özel kaynak sağlayıcısının uyguladığı kaynak türlerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="890b6-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="890b6-130">Oluşturmak için, RESOURCETYPE özelliklerinin notlar bölümü 'ne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="890b6-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890b6-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="890b6-131">-SubscriptionId</span></span>
<span data-ttu-id="890b6-132">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="890b6-132">The Azure subscription ID.</span></span>
<span data-ttu-id="890b6-133">Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="890b6-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890b6-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="890b6-134">-Tag</span></span>
<span data-ttu-id="890b6-135">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="890b6-135">Resource tags</span></span>

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

### <span data-ttu-id="890b6-136">-Doğrulama</span><span class="sxs-lookup"><span data-stu-id="890b6-136">-Validation</span></span>
<span data-ttu-id="890b6-137">Özel kaynak sağlayıcısının isteklerinde çalışacak doğrulama listesi.</span><span class="sxs-lookup"><span data-stu-id="890b6-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="890b6-138">Oluşturmak için, doğrulama özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="890b6-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="890b6-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="890b6-139">-Confirm</span></span>
<span data-ttu-id="890b6-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="890b6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="890b6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="890b6-141">-WhatIf</span></span>
<span data-ttu-id="890b6-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="890b6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="890b6-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="890b6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="890b6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890b6-144">CommonParameters</span></span>
<span data-ttu-id="890b6-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="890b6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890b6-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="890b6-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890b6-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="890b6-147">INPUTS</span></span>

## <span data-ttu-id="890b6-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="890b6-148">OUTPUTS</span></span>

### <span data-ttu-id="890b6-149">Microsoft. Azure. PowerShell. cmdlet. CustomProviders. modeller. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="890b6-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="890b6-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="890b6-150">NOTES</span></span>

<span data-ttu-id="890b6-151">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="890b6-151">ALIASES</span></span>

<span data-ttu-id="890b6-152">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="890b6-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="890b6-153">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="890b6-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="890b6-154">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="890b6-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="890b6-155">EYLEM <ıcustomrpactionroutedefinition [] >: özel kaynak sağlayıcısının uyguladığı eylemlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="890b6-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="890b6-156">`Endpoint <String>`: Özel kaynak sağlayıcısının proxy tarafından istek aldığı yol tanımı uç noktası URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="890b6-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="890b6-157">Bu, düz bir URI biçiminde (örneğin, ' https://testendpoint/ ') veya bir yol üzerinden yönlendirme için belirtilebilir (örneğin, ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="890b6-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="890b6-158">`Name <String>`: Yol tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="890b6-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="890b6-159">Bu, ARM uzantısının adı olur (örneğin, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name} ')</span><span class="sxs-lookup"><span data-stu-id="890b6-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="890b6-160">`[RoutingType <ActionRouting?>]`: Eylem istekleri için desteklenen yönlendirme türleri.</span><span class="sxs-lookup"><span data-stu-id="890b6-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="890b6-161">RESOURCETYPE <ıcustomrpresourcetyperoutedefinition [] >: özel kaynak sağlayıcısının uyguladığı kaynak türlerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="890b6-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="890b6-162">`Endpoint <String>`: Özel kaynak sağlayıcısının proxy tarafından istek aldığı yol tanımı uç noktası URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="890b6-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="890b6-163">Bu, düz bir URI biçiminde (örneğin, ' https://testendpoint/ ') veya bir yol üzerinden yönlendirme için belirtilebilir (örneğin, ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="890b6-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="890b6-164">`Name <String>`: Yol tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="890b6-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="890b6-165">Bu, ARM uzantısının adı olur (örneğin, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name} ')</span><span class="sxs-lookup"><span data-stu-id="890b6-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="890b6-166">`[RoutingType <ResourceTypeRouting?>]`: Kaynak istekleri için desteklenen yönlendirme türleri.</span><span class="sxs-lookup"><span data-stu-id="890b6-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="890b6-167">DOĞRULAMA <ıcustomrpdoğrulamaları [] >: özel kaynak sağlayıcısının isteklerinde çalışacak doğrulama listesi.</span><span class="sxs-lookup"><span data-stu-id="890b6-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="890b6-168">`Specification <String>`: Doğrulama belirtiminin bağlantısı.</span><span class="sxs-lookup"><span data-stu-id="890b6-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="890b6-169">Belirtim raw.githubusercontent.com üzerinde barındırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="890b6-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="890b6-170">`[ValidationType <ValidationType?>]`: Eşleşen bir istekte çalışacak doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="890b6-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="890b6-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="890b6-171">RELATED LINKS</span></span>

