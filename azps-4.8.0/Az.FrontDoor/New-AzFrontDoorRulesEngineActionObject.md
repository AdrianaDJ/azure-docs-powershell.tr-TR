---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineActionObject.md
ms.openlocfilehash: 25c8c2e772e4321a9edef5ac08b0c0a3bdc04bfd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268254"
---
# <span data-ttu-id="5b2d6-101">New-AzFrontDoorRulesEngineActionObject</span><span class="sxs-lookup"><span data-stu-id="5b2d6-101">New-AzFrontDoorRulesEngineActionObject</span></span>

## <span data-ttu-id="5b2d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b2d6-103">Kural altyapısı kuralı oluşturmak için PSRulesEngineAction nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-103">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span>

## <span data-ttu-id="5b2d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b2d6-104">SYNTAX</span></span>

### <span data-ttu-id="5b2d6-105">Byalanalanları Withforwardingparameterset</span><span class="sxs-lookup"><span data-stu-id="5b2d6-105">ByFieldsWithForwardingParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-CustomForwardingPath <String>] [-ForwardingProtocol <String>] -ResourceGroupName <String>
 -FrontDoorName <String> -BackendPoolName <String> [-EnableCaching <Boolean>]
 [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b2d6-106">Byalanalanları Withredirectparameterset</span><span class="sxs-lookup"><span data-stu-id="5b2d6-106">ByFieldsWithRedirectParameterSet</span></span>
```
New-AzFrontDoorRulesEngineActionObject
 [-RequestHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-ResponseHeaderAction <System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b2d6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b2d6-107">DESCRIPTION</span></span>
<span data-ttu-id="5b2d6-108">Kural altyapısı kuralı oluşturmak için PSRulesEngineAction nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-108">Create a PSRulesEngineAction object for creating a rules engine rule.</span></span> 

<span data-ttu-id="5b2d6-109">"-RequestHeaderActions" ve "-ResponseHeaderActions" parametrelerini geçirmek üzere PSHeaderObjects 'i oluşturmak için "New-AzFrontDoorHeaderActionObject" cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-109">Use cmdlet "New-AzFrontDoorHeaderActionObject" to create PSHeaderObjects to pass into the parameters "-RequestHeaderActions" and "-ResponseHeaderActions"."</span></span>

## <span data-ttu-id="5b2d6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b2d6-110">EXAMPLES</span></span>

### <span data-ttu-id="5b2d6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5b2d6-111">Example 1</span></span>
```powershell
PS C:\> $rulesEngineAction = New-AzFrontDoorRulesEngineActionObject -RequestHeaderAction $headerActions -ForwardingProtocol HttpsOnly -BackendPoolName mybackendpool -ResourceGroupName Jessicl-Test-RG -FrontDoorName jessicl-test-myappfrontend -QueryParameterStripDirective StripNone -DynamicCompression Disabled -EnableCaching $true
PS C:\> $rulesEngineAction

RequestHeaderAction            ResponseHeaderAction RouteConfigurationOverride
-------------------            -------------------- --------------------------
{headeraction1, headeraction2} {}                   Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineAction.RequestHeaderAction

HeaderName    HeaderActionType Value
----------    ---------------- -----
headeraction1        Overwrite
headeraction2           Append

PS C:\> $rulesEngineAction.ResponseHeaderAction
PS C:\> $rulesEngineAction.RouteConfigurationOverride

CustomForwardingPath         :
ForwardingProtocol           : HttpsOnly
BackendPoolId                : /subscriptions/47f4bc68-6fe4-43a2-be8b-dfd0e290efa2/resourceGroups/myresourcegroup/provi
                               ders/Microsoft.Network/frontDoors/myfrontdoor/BackendPools/mybackendpool
QueryParameterStripDirective : StripNone
DynamicCompression           : Disabled
EnableCaching                : True
```

<span data-ttu-id="5b2d6-112">Kural altyapısı eylemi oluşturun ve oluşturulan kural altyapısı eyleminin özelliklerinin nasıl görüntüleneceğini gösterin.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-112">Create a rules engine action and show how to view the properties of the rules engine action created.</span></span>

## <span data-ttu-id="5b2d6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b2d6-113">PARAMETERS</span></span>

### <span data-ttu-id="5b2d6-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="5b2d6-114">-BackendPoolName</span></span>
<span data-ttu-id="5b2d6-115">Bu kuralın yönlendirdığı BackendPool adı</span><span class="sxs-lookup"><span data-stu-id="5b2d6-115">The name of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="5b2d6-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="5b2d6-116">-CustomForwardingPath</span></span>
<span data-ttu-id="5b2d6-117">Bu kuralla eşleşen kaynak yollarını yeniden yazmak için kullanılan özel yol.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="5b2d6-118">Gelen yolu kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-118">Leave empty to use incoming path.</span></span>

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

### <span data-ttu-id="5b2d6-119">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="5b2d6-119">-CustomFragment</span></span>
<span data-ttu-id="5b2d6-120">Redirect URL 'ye eklenecek parça.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-120">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="5b2d6-121">Parça, # ' dan sonra gelen URL 'nin bölümüdür.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-121">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="5b2d6-122">#.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-122">Do not include the #.</span></span>

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

### <span data-ttu-id="5b2d6-123">-CustomHost</span><span class="sxs-lookup"><span data-stu-id="5b2d6-123">-CustomHost</span></span>
<span data-ttu-id="5b2d6-124">Yeniden yönlendirilecek ev.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-124">Host to redirect.</span></span>
<span data-ttu-id="5b2d6-125">Hedef ana bilgisayar olarak gelen ana bilgisayarı kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-125">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="5b2d6-126">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="5b2d6-126">-CustomPath</span></span>
<span data-ttu-id="5b2d6-127">Yeniden yönlendirilecek tam yol.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-127">The full path to redirect.</span></span>
<span data-ttu-id="5b2d6-128">Yol boş olamaz ve ile başlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-128">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="5b2d6-129">Gelen yolunu hedef yol olarak kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-129">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="5b2d6-130">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="5b2d6-130">-CustomQueryString</span></span>
<span data-ttu-id="5b2d6-131">Yönlendirme URL 'sine yerleştirilecek sorgu dizeleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-131">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="5b2d6-132">Bu değeri ayarlamak, var olan sorgu dizesinin yerini alır; gelen sorgu dizesini korumak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-132">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="5b2d6-133">Sorgu dizesi \<key\> = \<value\> biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-133">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="5b2d6-134">İlk</span><span class="sxs-lookup"><span data-stu-id="5b2d6-134">The first ?</span></span>
<span data-ttu-id="5b2d6-135">& otomatik olarak eklenir; böylece bunları öne eklemeyin, ancak birden çok sorgu dizesini & ile ayrı ayrı yapın.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-135">and & will be added automatically so do not include them in the front, but do separate multiple query strings with &.</span></span>

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

### <span data-ttu-id="5b2d6-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b2d6-136">-DefaultProfile</span></span>
<span data-ttu-id="5b2d6-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b2d6-138">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="5b2d6-138">-DynamicCompression</span></span>
<span data-ttu-id="5b2d6-139">Önbelleğe alınan içerik için dinamik Sıkıştırmayı etkinleştirip etkinleştirmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-139">Whether to enable dynamic compression for cached content.</span></span>
<span data-ttu-id="5b2d6-140">Varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="5b2d6-140">Default value is Enabled</span></span>

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

### <span data-ttu-id="5b2d6-141">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="5b2d6-141">-EnableCaching</span></span>
<span data-ttu-id="5b2d6-142">Bu yol için önbelleğe almanın etkinleştirilip etkinleştirilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-142">Whether to enable caching for this route.</span></span>
<span data-ttu-id="5b2d6-143">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="5b2d6-143">Default value is false</span></span>

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

### <span data-ttu-id="5b2d6-144">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="5b2d6-144">-ForwardingProtocol</span></span>
<span data-ttu-id="5b2d6-145">Bu kuralın, trafiği backends 'ye iletirken kullanacağı protokol.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-145">The protocol this rule will use when forwarding traffic to backends.</span></span>
<span data-ttu-id="5b2d6-146">Varsayılan değer, MatchRequest</span><span class="sxs-lookup"><span data-stu-id="5b2d6-146">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="5b2d6-147">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="5b2d6-147">-FrontDoorName</span></span>
<span data-ttu-id="5b2d6-148">Bu yönlendirme kuralının ait olduğu ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-148">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="5b2d6-149">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="5b2d6-149">-QueryParameterStripDirective</span></span>
<span data-ttu-id="5b2d6-150">Önbellek anahtarı oluşturulurken URL sorgu koşullarının kullanımı.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-150">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="5b2d6-151">Varsayılan değer StripAll</span><span class="sxs-lookup"><span data-stu-id="5b2d6-151">Default value is StripAll</span></span>

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

### <span data-ttu-id="5b2d6-152">-RedirectProtocol</span><span class="sxs-lookup"><span data-stu-id="5b2d6-152">-RedirectProtocol</span></span>
<span data-ttu-id="5b2d6-153">Trafiğin yönlendirileceği hedefin protokolü.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-153">The protocol of the destination to where the traffic is redirected.</span></span>
<span data-ttu-id="5b2d6-154">Varsayılan değer, MatchRequest</span><span class="sxs-lookup"><span data-stu-id="5b2d6-154">Default value is MatchRequest</span></span>

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

### <span data-ttu-id="5b2d6-155">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="5b2d6-155">-RedirectType</span></span>
<span data-ttu-id="5b2d6-156">Kuralı trafiği yeniden yönlendirmede kullanacağı yeniden yönlendirme türü.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-156">The redirect type the rule will use when redirecting traffic.</span></span>
<span data-ttu-id="5b2d6-157">Varsayılan değer taşındı</span><span class="sxs-lookup"><span data-stu-id="5b2d6-157">Default Value is Moved</span></span>

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

### <span data-ttu-id="5b2d6-158">-RequestHeaderAction</span><span class="sxs-lookup"><span data-stu-id="5b2d6-158">-RequestHeaderAction</span></span>
<span data-ttu-id="5b2d6-159">AFD 'dan kaynağa uygulanacak üstbilgi eylemlerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-159">A list of header actions to apply from the request from AFD to the origin.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2d6-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b2d6-160">-ResourceGroupName</span></span>
<span data-ttu-id="5b2d6-161">RoutingRule 'un içinde oluşturulduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-161">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="5b2d6-162">-ResponseHeaderAction</span><span class="sxs-lookup"><span data-stu-id="5b2d6-162">-ResponseHeaderAction</span></span>
<span data-ttu-id="5b2d6-163">AFD 'dan istemciye yapılan yanıttan uygulanacak üstbilgi eylemlerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-163">A list of header actions to apply from the response from AFD to the client.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b2d6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b2d6-164">CommonParameters</span></span>
<span data-ttu-id="5b2d6-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b2d6-166">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5b2d6-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b2d6-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b2d6-167">INPUTS</span></span>

### <span data-ttu-id="5b2d6-168">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5b2d6-168">None</span></span>

## <span data-ttu-id="5b2d6-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b2d6-169">OUTPUTS</span></span>

### <span data-ttu-id="5b2d6-170">Microsoft. Azure. Commands. Frontkapısı. modeller. PSRulesEngineAction</span><span class="sxs-lookup"><span data-stu-id="5b2d6-170">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction</span></span>

## <span data-ttu-id="5b2d6-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b2d6-171">NOTES</span></span>

## <span data-ttu-id="5b2d6-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b2d6-172">RELATED LINKS</span></span>
