---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: 02291202966ab832bf11edbd59a1504c001c948e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916715"
---
# <span data-ttu-id="3a6cb-101">New-AzFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="3a6cb-101">New-AzFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="3a6cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a6cb-102">SYNOPSIS</span></span>
<span data-ttu-id="3a6cb-103">Ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a6cb-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="3a6cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a6cb-104">SYNTAX</span></span>

### <span data-ttu-id="3a6cb-105">Byalanalanları Withforwardingparameterset</span><span class="sxs-lookup"><span data-stu-id="3a6cb-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a6cb-106">Byalanalanları Withredirectparameterset</span><span class="sxs-lookup"><span data-stu-id="3a6cb-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <PSRedirectType>] [-RedirectProtocol <PSRedirectProtocol>] [-CustomHost <String>]
 [-CustomPath <String>] [-CustomFragment <String>] [-CustomQueryString <String>]
 [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a6cb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a6cb-107">DESCRIPTION</span></span>
<span data-ttu-id="3a6cb-108">Ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a6cb-108">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="3a6cb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a6cb-109">EXAMPLES</span></span>

### <span data-ttu-id="3a6cb-110">Örnek 1: ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a6cb-110">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="3a6cb-111">Ön kapı oluşturmak için PSRoutingRuleObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a6cb-111">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="3a6cb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a6cb-112">PARAMETERS</span></span>

### <span data-ttu-id="3a6cb-113">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="3a6cb-113">-AcceptedProtocol</span></span>
<span data-ttu-id="3a6cb-114">Bu kuralla eşleşecek iletişim kuralı düzenleri.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-114">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="3a6cb-115">Varsayılan değer: {https, http}</span><span class="sxs-lookup"><span data-stu-id="3a6cb-115">Default value is {Https, Http}</span></span>

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

### <span data-ttu-id="3a6cb-116">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="3a6cb-116">-BackendPoolName</span></span>
<span data-ttu-id="3a6cb-117">Bu kuralın yönlendirme yolu</span><span class="sxs-lookup"><span data-stu-id="3a6cb-117">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="3a6cb-118">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="3a6cb-118">-CustomForwardingPath</span></span>
<span data-ttu-id="3a6cb-119">Bu kuralla eşleşen kaynak yollarını yeniden yazmak için kullanılan özel yol.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-119">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="3a6cb-120">Gelen yolu kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-120">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="3a6cb-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="3a6cb-121">-CustomFragment</span></span>
<span data-ttu-id="3a6cb-122">Redirect URL 'ye eklenecek parça.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-122">Fragment to add to the redirect URL.</span></span> <span data-ttu-id="3a6cb-123">Parça, # ' dan sonra gelen URL 'nin bölümüdür.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-123">Fragment is the part of the URL that comes after #.</span></span> <span data-ttu-id="3a6cb-124">#.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-124">Do not include the #.</span></span>

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

### <span data-ttu-id="3a6cb-125">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="3a6cb-125">-CustomHost</span></span>
<span data-ttu-id="3a6cb-126">Yeniden yönlendirilecek ev.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-126">Host to redirect.</span></span> <span data-ttu-id="3a6cb-127">Hedef ana bilgisayar olarak gelen ana bilgisayarı kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="3a6cb-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="3a6cb-128">-CustomPath</span></span>
<span data-ttu-id="3a6cb-129">Yeniden yönlendirilecek tam yol.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-129">The full path to redirect.</span></span> <span data-ttu-id="3a6cb-130">Yol boş olamaz ve ile başlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-130">Path cannot be empty and must start with /.</span></span> <span data-ttu-id="3a6cb-131">Gelen yolunu hedef yol olarak kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="3a6cb-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="3a6cb-132">-CustomQueryString</span></span>
<span data-ttu-id="3a6cb-133">Yönlendirme URL 'sine yerleştirilecek sorgu dizeleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-133">The set of query strings to be placed in the redirect URL.</span></span> <span data-ttu-id="3a6cb-134">Bu değeri ayarlamak, var olan sorgu dizesinin yerini alır; gelen sorgu dizesini korumak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span> <span data-ttu-id="3a6cb-135">Sorgu dizesi <key>=</span><span class="sxs-lookup"><span data-stu-id="3a6cb-135">Query string must be in <key>=</span></span><value> <span data-ttu-id="3a6cb-136">formatlamak.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-136">format.</span></span> <span data-ttu-id="3a6cb-137">İlk</span><span class="sxs-lookup"><span data-stu-id="3a6cb-137">The first ?</span></span> <span data-ttu-id="3a6cb-138">& otomatik olarak eklenir; böylece bunları öne eklemeyin, ancak birden çok sorgu dizesini & ile ayrı ayrı yapın.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-138">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="3a6cb-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a6cb-139">-DefaultProfile</span></span>
<span data-ttu-id="3a6cb-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a6cb-141">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="3a6cb-141">-DynamicCompression</span></span>
<span data-ttu-id="3a6cb-142">Önbelleğe alma etkinleştirildiğinde önbelleğe alınan içerikte dinamik sıkıştırmanın etkinleştirilip etkinleştirilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-142">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="3a6cb-143">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="3a6cb-143">Default value is Enabled</span></span>

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

### <span data-ttu-id="3a6cb-144">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="3a6cb-144">-EnableCaching</span></span>
<span data-ttu-id="3a6cb-145">Bu yol için önbelleğe almanın etkinleştirilip etkinleştirilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-145">Whether to enable caching for this route.</span></span> <span data-ttu-id="3a6cb-146">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="3a6cb-146">Default value is false</span></span>

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

### <span data-ttu-id="3a6cb-147">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="3a6cb-147">-EnabledState</span></span>
<span data-ttu-id="3a6cb-148">Bu kuralın kullanımını etkinleştirip etkinleştirmeyeceğinizi.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-148">Whether to enable use of this rule.</span></span>
<span data-ttu-id="3a6cb-149">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="3a6cb-149">Default value is Enabled</span></span>

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

### <span data-ttu-id="3a6cb-150">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="3a6cb-150">-ForwardingProtocol</span></span>
<span data-ttu-id="3a6cb-151">Trafiği backends varsayılan değerine iletirken kullanılacak protokol</span><span class="sxs-lookup"><span data-stu-id="3a6cb-151">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6cb-152">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="3a6cb-152">-FrontDoorName</span></span>
<span data-ttu-id="3a6cb-153">Bu yönlendirme kuralının ait olduğu ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-153">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="3a6cb-154">-Frontendenvseçpointname</span><span class="sxs-lookup"><span data-stu-id="3a6cb-154">-FrontendEndpointName</span></span>
<span data-ttu-id="3a6cb-155">Bu kuralla ilişkili ön uç uç noktalarının adları</span><span class="sxs-lookup"><span data-stu-id="3a6cb-155">The names of Frontend endpoints associated with this rule</span></span>

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

### <span data-ttu-id="3a6cb-156">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a6cb-156">-Name</span></span>
<span data-ttu-id="3a6cb-157">Yönlendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-157">RoutingRule name.</span></span>

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

### <span data-ttu-id="3a6cb-158">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="3a6cb-158">-PatternToMatch</span></span>
<span data-ttu-id="3a6cb-159">Kuralın yol desenleri, yolun son/son ucunda olanlar dışında \* içermemelidir.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-159">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="3a6cb-160">Varsayılan değer/\*</span><span class="sxs-lookup"><span data-stu-id="3a6cb-160">Default value is /\*</span></span>

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

### <span data-ttu-id="3a6cb-161">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="3a6cb-161">-QueryParameterStripDirective</span></span>
<span data-ttu-id="3a6cb-162">Önbellek anahtarı oluşturulurken URL sorgu koşullarının kullanımı.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-162">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="3a6cb-163">Varsayılan değer StripAll</span><span class="sxs-lookup"><span data-stu-id="3a6cb-163">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6cb-164">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="3a6cb-164">-RedirectProtocol</span></span>
<span data-ttu-id="3a6cb-165">Trafiğin yönlendirileceği hedefin protokolü.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-165">The protocol of the destination to where the traffic is redirected.</span></span> <span data-ttu-id="3a6cb-166">Varsayılan değer, MatchRequest</span><span class="sxs-lookup"><span data-stu-id="3a6cb-166">Default value is MatchRequest</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectProtocol
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6cb-167">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="3a6cb-167">-RedirectType</span></span>
<span data-ttu-id="3a6cb-168">Kuralı trafiği yeniden yönlendirmede kullanacağı yeniden yönlendirme türü.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-168">The redirect type the rule will use when redirecting traffic.</span></span> <span data-ttu-id="3a6cb-169">Varsayılan değer taşındı</span><span class="sxs-lookup"><span data-stu-id="3a6cb-169">Default Value is Moved</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectType
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:
Accepted values: Moved, Found, TemporaryRedirect, PermanentRedirect

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a6cb-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a6cb-170">-ResourceGroupName</span></span>
<span data-ttu-id="3a6cb-171">RoutingRule 'un içinde oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-171">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="3a6cb-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a6cb-172">CommonParameters</span></span>
<span data-ttu-id="3a6cb-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a6cb-174">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3a6cb-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a6cb-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a6cb-175">INPUTS</span></span>

### <span data-ttu-id="3a6cb-176">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3a6cb-176">None</span></span>

## <span data-ttu-id="3a6cb-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a6cb-177">OUTPUTS</span></span>

### <span data-ttu-id="3a6cb-178">Microsoft. Azure. Commands. Frontkapısı. modeller. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3a6cb-178">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="3a6cb-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a6cb-179">NOTES</span></span>

## <span data-ttu-id="3a6cb-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a6cb-180">RELATED LINKS</span></span>

<span data-ttu-id="3a6cb-181">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Set-Azfrontkapısı](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="3a6cb-181">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
