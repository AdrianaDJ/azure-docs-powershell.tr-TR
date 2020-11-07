---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 3b0c9af411bace40d963158befcb7b178b638a3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751898"
---
# <span data-ttu-id="38802-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="38802-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="38802-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38802-102">SYNOPSIS</span></span>
<span data-ttu-id="38802-103">Ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="38802-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="38802-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38802-104">SYNTAX</span></span>

### <span data-ttu-id="38802-105">Byalanalanları Withforwardingparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38802-105">ByFieldsWithForwardingParameterSet (Default)</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38802-106">Byalanalanları Withredirectparameterset</span><span class="sxs-lookup"><span data-stu-id="38802-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38802-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="38802-107">DESCRIPTION</span></span>
<span data-ttu-id="38802-108">Ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="38802-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="38802-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38802-109">EXAMPLES</span></span>

### <span data-ttu-id="38802-110">Örnek 1: iletme kuralıyla ön kapı oluşturulması için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="38802-110">Example 1: Create a PSRoutingRuleObject for Front Door creation with a forwarding rule</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### <span data-ttu-id="38802-111">Örnek 2: bir yönlendirme kuralıyla ön kapı oluşturulması için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="38802-111">Example 2: Create a PSRoutingRuleObject for Front Door creation with a redirect rule</span></span>
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :

```
<span data-ttu-id="38802-112">Ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="38802-112">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="38802-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38802-113">PARAMETERS</span></span>

### <span data-ttu-id="38802-114">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="38802-114">-AcceptedProtocol</span></span>
<span data-ttu-id="38802-115">Bu kuralla eşleşecek iletişim kuralı düzenleri.</span><span class="sxs-lookup"><span data-stu-id="38802-115">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="38802-116">Varsayılan değer: {https, http}</span><span class="sxs-lookup"><span data-stu-id="38802-116">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-117">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="38802-117">-BackendPoolName</span></span>
<span data-ttu-id="38802-118">Bu kuralın yönlendirme yolu</span><span class="sxs-lookup"><span data-stu-id="38802-118">Resource id of the BackendPool which this rule routes to</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-119">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="38802-119">-CustomForwardingPath</span></span>
<span data-ttu-id="38802-120">Bu kuralla eşleşen kaynak yollarını yeniden yazmak için kullanılan özel yol.</span><span class="sxs-lookup"><span data-stu-id="38802-120">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="38802-121">Gelen yolu kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="38802-121">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-122">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="38802-122">-CustomFragment</span></span>
<span data-ttu-id="38802-123">Redirect URL 'ye eklenecek parça.</span><span class="sxs-lookup"><span data-stu-id="38802-123">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="38802-124">Parça, # ' dan sonra gelen URL 'nin bölümüdür.</span><span class="sxs-lookup"><span data-stu-id="38802-124">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="38802-125">#.</span><span class="sxs-lookup"><span data-stu-id="38802-125">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-126">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="38802-126">-CustomHost</span></span>
<span data-ttu-id="38802-127">Yeniden yönlendirilecek ev.</span><span class="sxs-lookup"><span data-stu-id="38802-127">Host to redirect.</span></span> <span data-ttu-id="38802-128">Hedef ana bilgisayar olarak gelen ana bilgisayarı kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="38802-128">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-129">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="38802-129">-CustomPath</span></span>
<span data-ttu-id="38802-130">Yeniden yönlendirilecek tam yol.</span><span class="sxs-lookup"><span data-stu-id="38802-130">The full path to redirect.</span></span> <span data-ttu-id="38802-131">Yol boş olamaz ve ile başlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="38802-131">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="38802-132">Gelen yolunu hedef yol olarak kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="38802-132">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-133">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="38802-133">-CustomQueryString</span></span>
<span data-ttu-id="38802-134">Yönlendirme URL 'sine yerleştirilecek sorgu dizeleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="38802-134">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="38802-135">Bu değeri ayarlamak, var olan sorgu dizesinin yerini alır; gelen sorgu dizesini korumak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="38802-135">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="38802-136">Sorgu dizesi <key>=</span><span class="sxs-lookup"><span data-stu-id="38802-136">Query string must be in <key>=</span></span><value> <span data-ttu-id="38802-137">formatlamak.</span><span class="sxs-lookup"><span data-stu-id="38802-137">format.</span></span> <span data-ttu-id="38802-138">İlk</span><span class="sxs-lookup"><span data-stu-id="38802-138">The first ?</span></span> <span data-ttu-id="38802-139">& otomatik olarak eklenir; böylece bunları öne eklemeyin, ancak birden çok sorgu dizesini & ile ayrı ayrı yapın.</span><span class="sxs-lookup"><span data-stu-id="38802-139">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38802-140">-DefaultProfile</span></span>
<span data-ttu-id="38802-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38802-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-142">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="38802-142">-DynamicCompression</span></span>
<span data-ttu-id="38802-143">Önbelleğe alma etkinleştirildiğinde önbelleğe alınan içerikte dinamik sıkıştırmanın etkinleştirilip etkinleştirilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="38802-143">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="38802-144">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="38802-144">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-145">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="38802-145">-EnableCaching</span></span>
<span data-ttu-id="38802-146">Bu yol için önbelleğe almanın etkinleştirilip etkinleştirilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="38802-146">Whether to enable caching for this route.</span></span> <span data-ttu-id="38802-147">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="38802-147">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-148">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="38802-148">-EnabledState</span></span>
<span data-ttu-id="38802-149">Bu kuralın kullanımını etkinleştirip etkinleştirmeyeceğinizi.</span><span class="sxs-lookup"><span data-stu-id="38802-149">Whether to enable use of this rule.</span></span>
<span data-ttu-id="38802-150">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="38802-150">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-151">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="38802-151">-ForwardingProtocol</span></span>
<span data-ttu-id="38802-152">Trafiği backends varsayılan değerine iletirken kullanılacak protokol</span><span class="sxs-lookup"><span data-stu-id="38802-152">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-153">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="38802-153">-FrontDoorName</span></span>
<span data-ttu-id="38802-154">Bu yönlendirme kuralının ait olduğu ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="38802-154">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="38802-155">-Frontendenvseçpointname</span><span class="sxs-lookup"><span data-stu-id="38802-155">-FrontendEndpointName</span></span>
<span data-ttu-id="38802-156">Bu kuralla ilişkili ön uç uç noktalarının adları</span><span class="sxs-lookup"><span data-stu-id="38802-156">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-157">-Ad</span><span class="sxs-lookup"><span data-stu-id="38802-157">-Name</span></span>
<span data-ttu-id="38802-158">Yönlendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="38802-158">RoutingRule name.</span></span>

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

### <span data-ttu-id="38802-159">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="38802-159">-PatternToMatch</span></span>
<span data-ttu-id="38802-160">Kuralın yol desenleri, yolun son/son ucunda olanlar dışında \* içermemelidir.</span><span class="sxs-lookup"><span data-stu-id="38802-160">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="38802-161">Varsayılan değer/\*</span><span class="sxs-lookup"><span data-stu-id="38802-161">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-162">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="38802-162">-QueryParameterStripDirective</span></span>
<span data-ttu-id="38802-163">Önbellek anahtarı oluşturulurken URL sorgu koşullarının kullanımı.</span><span class="sxs-lookup"><span data-stu-id="38802-163">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="38802-164">Varsayılan değer StripAll</span><span class="sxs-lookup"><span data-stu-id="38802-164">Default value is StripAll</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-165">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="38802-165">-RedirectProtocol</span></span>
<span data-ttu-id="38802-166">Trafiğin yönlendirileceği hedefin protokolü.</span><span class="sxs-lookup"><span data-stu-id="38802-166">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="38802-167">Varsayılan değer, MatchRequest</span><span class="sxs-lookup"><span data-stu-id="38802-167">Default value is MatchRequest</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-168">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="38802-168">-RedirectType</span></span>
<span data-ttu-id="38802-169">Kuralı trafiği yeniden yönlendirmede kullanacağı yeniden yönlendirme türü.</span><span class="sxs-lookup"><span data-stu-id="38802-169">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="38802-170">Varsayılan değer taşındı</span><span class="sxs-lookup"><span data-stu-id="38802-170">Default Value is Moved</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38802-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38802-171">-ResourceGroupName</span></span>
<span data-ttu-id="38802-172">RoutingRule 'un içinde oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="38802-172">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="38802-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38802-173">CommonParameters</span></span>
<span data-ttu-id="38802-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38802-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38802-175">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="38802-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38802-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38802-176">INPUTS</span></span>

### <span data-ttu-id="38802-177">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="38802-177">None</span></span>

## <span data-ttu-id="38802-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38802-178">OUTPUTS</span></span>

### <span data-ttu-id="38802-179">Microsoft. Azure. Commands. Frontkapısı. modeller. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="38802-179">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="38802-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38802-180">NOTES</span></span>

## <span data-ttu-id="38802-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38802-181">RELATED LINKS</span></span>

<span data-ttu-id="38802-182">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="38802-182">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>