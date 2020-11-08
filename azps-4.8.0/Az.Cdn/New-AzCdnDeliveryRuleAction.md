---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109822"
---
# <span data-ttu-id="f1eab-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="f1eab-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="f1eab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1eab-102">SYNOPSIS</span></span>
<span data-ttu-id="f1eab-103">Teslim eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1eab-103">Creates a delivery action.</span></span>

## <span data-ttu-id="f1eab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1eab-104">SYNTAX</span></span>

### <span data-ttu-id="f1eab-105">CacheExpirationActionParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1eab-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1eab-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1eab-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1eab-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1eab-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1eab-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1eab-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1eab-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1eab-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1eab-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1eab-110">DESCRIPTION</span></span>
<span data-ttu-id="f1eab-111">**New-AzCdnDeliveryRule** CMDLET 'i CDN uç noktası oluşturma için bir teslim kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1eab-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="f1eab-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1eab-112">EXAMPLES</span></span>

### <span data-ttu-id="f1eab-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1eab-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="f1eab-114">Basit bir teslim kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f1eab-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="f1eab-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1eab-115">PARAMETERS</span></span>

### <span data-ttu-id="f1eab-116">-Eylem</span><span class="sxs-lookup"><span data-stu-id="f1eab-116">-Action</span></span>
<span data-ttu-id="f1eab-117">Gerçekleştirilecek eylem.</span><span class="sxs-lookup"><span data-stu-id="f1eab-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="f1eab-118">-CacheBehavior</span></span>
<span data-ttu-id="f1eab-119">Eylem için önbelleğe alma davranışı</span><span class="sxs-lookup"><span data-stu-id="f1eab-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="f1eab-120">-CacheDuration</span></span>
<span data-ttu-id="f1eab-121">İçeriğin önbelleğe alınması gereken süre.</span><span class="sxs-lookup"><span data-stu-id="f1eab-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="f1eab-122">İzin verilen biçim \[ d. \] ss: DD: ss</span><span class="sxs-lookup"><span data-stu-id="f1eab-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="f1eab-123">-CustomFragment</span></span>
<span data-ttu-id="f1eab-124">Redirect URL 'ye eklenecek parça.</span><span class="sxs-lookup"><span data-stu-id="f1eab-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="f1eab-125">Parça, # ' dan sonra gelen URL 'nin bölümüdür.</span><span class="sxs-lookup"><span data-stu-id="f1eab-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="f1eab-126">#.</span><span class="sxs-lookup"><span data-stu-id="f1eab-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-127">-Customanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="f1eab-127">-CustomHostname</span></span>
<span data-ttu-id="f1eab-128">Yeniden yönlendirilecek ev.</span><span class="sxs-lookup"><span data-stu-id="f1eab-128">Host to redirect.</span></span>
<span data-ttu-id="f1eab-129">Hedef ana bilgisayar olarak gelen ana bilgisayarı kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="f1eab-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="f1eab-130">-CustomPath</span></span>
<span data-ttu-id="f1eab-131">Yeniden yönlendirilecek tam yol.</span><span class="sxs-lookup"><span data-stu-id="f1eab-131">The full path to redirect.</span></span>
<span data-ttu-id="f1eab-132">Yol boş olamaz ve ile başlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f1eab-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="f1eab-133">Gelen yolunu hedef yol olarak kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="f1eab-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="f1eab-134">-CustomQueryString</span></span>
<span data-ttu-id="f1eab-135">Yönlendirme URL 'sine yerleştirilecek sorgu dizeleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="f1eab-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="f1eab-136">Bu değeri ayarlamak, var olan sorgu dizesinin yerini alır; gelen sorgu dizesini korumak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="f1eab-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="f1eab-137">Sorgu dizesi \<key\> = \<value\> biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f1eab-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="f1eab-138">?</span><span class="sxs-lookup"><span data-stu-id="f1eab-138">?</span></span> <span data-ttu-id="f1eab-139">ve & otomatik olarak eklenir; böylece bunları eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="f1eab-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1eab-140">-DefaultProfile</span></span>
<span data-ttu-id="f1eab-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1eab-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1eab-142">-Hedef</span><span class="sxs-lookup"><span data-stu-id="f1eab-142">-Destination</span></span>
<span data-ttu-id="f1eab-143">Yukarıdaki isteklerin üzerine yazılması için göreli URL 'YI tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="f1eab-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="f1eab-144">-DestinationProtocol</span></span>
<span data-ttu-id="f1eab-145">Yönlendirme için kullanılacak protokol.</span><span class="sxs-lookup"><span data-stu-id="f1eab-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="f1eab-146">Varsayılan değer MatchRequest değeridir.</span><span class="sxs-lookup"><span data-stu-id="f1eab-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="f1eab-147">-HeaderActionType</span></span>
<span data-ttu-id="f1eab-148">İstek üst bilgisinin veya Yanıt üstbilgisinin değiştirilip güncelleştirilmeyeceğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="f1eab-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="f1eab-149">-HeaderName</span></span>
<span data-ttu-id="f1eab-150">Değiştirilecek üst bilginin adı.</span><span class="sxs-lookup"><span data-stu-id="f1eab-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="f1eab-151">-PreservePath</span></span>
<span data-ttu-id="f1eab-152">Eşleşmeyen yolun korunup korunmayacağı.</span><span class="sxs-lookup"><span data-stu-id="f1eab-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="f1eab-153">-QueryParameter</span></span>
<span data-ttu-id="f1eab-154">İçerilecek veya dışlanacak sorgu parametreleri (virgülle ayrılmış).</span><span class="sxs-lookup"><span data-stu-id="f1eab-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="f1eab-155">-QueryStringBehavior</span></span>
<span data-ttu-id="f1eab-156">İstekler için QueryString davranışı</span><span class="sxs-lookup"><span data-stu-id="f1eab-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="f1eab-157">-RedirectType</span></span>
<span data-ttu-id="f1eab-158">Yeniden yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="f1eab-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="f1eab-159">-SourcePattern</span></span>
<span data-ttu-id="f1eab-160">Yeniden yazılabilir isteklerin türünü tanımlayan bir istek URI deseni tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="f1eab-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="f1eab-161">Değer boşsa, tüm dizeler eşleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f1eab-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-162">-Değer</span><span class="sxs-lookup"><span data-stu-id="f1eab-162">-Value</span></span>
<span data-ttu-id="f1eab-163">Belirtilen eylem değeri.</span><span class="sxs-lookup"><span data-stu-id="f1eab-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1eab-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1eab-164">CommonParameters</span></span>
<span data-ttu-id="f1eab-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1eab-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1eab-166">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f1eab-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1eab-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1eab-167">INPUTS</span></span>

### <span data-ttu-id="f1eab-168">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f1eab-168">None</span></span>

## <span data-ttu-id="f1eab-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1eab-169">OUTPUTS</span></span>

### <span data-ttu-id="f1eab-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="f1eab-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="f1eab-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1eab-171">NOTES</span></span>

## <span data-ttu-id="f1eab-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1eab-172">RELATED LINKS</span></span>
