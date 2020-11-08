---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098325"
---
# <span data-ttu-id="51187-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="51187-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="51187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51187-102">SYNOPSIS</span></span>
<span data-ttu-id="51187-103">Teslim eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51187-103">Creates a delivery action.</span></span>

## <span data-ttu-id="51187-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51187-104">SYNTAX</span></span>

### <span data-ttu-id="51187-105">CacheExpirationActionParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51187-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51187-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51187-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51187-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51187-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51187-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51187-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51187-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="51187-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51187-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="51187-110">DESCRIPTION</span></span>
<span data-ttu-id="51187-111">**New-AzCdnDeliveryRule** CMDLET 'i CDN uç noktası oluşturma için bir teslim kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="51187-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="51187-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51187-112">EXAMPLES</span></span>

### <span data-ttu-id="51187-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="51187-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="51187-114">Basit bir teslim kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="51187-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="51187-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51187-115">PARAMETERS</span></span>

### <span data-ttu-id="51187-116">-Eylem</span><span class="sxs-lookup"><span data-stu-id="51187-116">-Action</span></span>
<span data-ttu-id="51187-117">Gerçekleştirilecek eylem.</span><span class="sxs-lookup"><span data-stu-id="51187-117">Action to perform.</span></span>

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

### <span data-ttu-id="51187-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="51187-118">-CacheBehavior</span></span>
<span data-ttu-id="51187-119">Eylem için önbelleğe alma davranışı</span><span class="sxs-lookup"><span data-stu-id="51187-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="51187-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="51187-120">-CacheDuration</span></span>
<span data-ttu-id="51187-121">İçeriğin önbelleğe alınması gereken süre.</span><span class="sxs-lookup"><span data-stu-id="51187-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="51187-122">İzin verilen biçim \[ d. \] ss: DD: ss</span><span class="sxs-lookup"><span data-stu-id="51187-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="51187-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="51187-123">-CustomFragment</span></span>
<span data-ttu-id="51187-124">Redirect URL 'ye eklenecek parça.</span><span class="sxs-lookup"><span data-stu-id="51187-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="51187-125">Parça, # ' dan sonra gelen URL 'nin bölümüdür.</span><span class="sxs-lookup"><span data-stu-id="51187-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="51187-126">#.</span><span class="sxs-lookup"><span data-stu-id="51187-126">Do not include the #.</span></span>

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

### <span data-ttu-id="51187-127">-Customanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="51187-127">-CustomHostname</span></span>
<span data-ttu-id="51187-128">Yeniden yönlendirilecek ev.</span><span class="sxs-lookup"><span data-stu-id="51187-128">Host to redirect.</span></span>
<span data-ttu-id="51187-129">Hedef ana bilgisayar olarak gelen ana bilgisayarı kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="51187-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="51187-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="51187-130">-CustomPath</span></span>
<span data-ttu-id="51187-131">Yeniden yönlendirilecek tam yol.</span><span class="sxs-lookup"><span data-stu-id="51187-131">The full path to redirect.</span></span>
<span data-ttu-id="51187-132">Yol boş olamaz ve ile başlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="51187-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="51187-133">Gelen yolunu hedef yol olarak kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="51187-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="51187-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="51187-134">-CustomQueryString</span></span>
<span data-ttu-id="51187-135">Yönlendirme URL 'sine yerleştirilecek sorgu dizeleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="51187-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="51187-136">Bu değeri ayarlamak, var olan sorgu dizesinin yerini alır; gelen sorgu dizesini korumak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="51187-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="51187-137">Sorgu dizesi \< anahtar \> = \< değeri \> biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="51187-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="51187-138">?</span><span class="sxs-lookup"><span data-stu-id="51187-138">?</span></span> <span data-ttu-id="51187-139">ve & otomatik olarak eklenir; böylece bunları eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="51187-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="51187-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51187-140">-DefaultProfile</span></span>
<span data-ttu-id="51187-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51187-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51187-142">-Hedef</span><span class="sxs-lookup"><span data-stu-id="51187-142">-Destination</span></span>
<span data-ttu-id="51187-143">Yukarıdaki isteklerin üzerine yazılması için göreli URL 'YI tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="51187-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="51187-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="51187-144">-DestinationProtocol</span></span>
<span data-ttu-id="51187-145">Yönlendirme için kullanılacak protokol.</span><span class="sxs-lookup"><span data-stu-id="51187-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="51187-146">Varsayılan değer MatchRequest değeridir.</span><span class="sxs-lookup"><span data-stu-id="51187-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="51187-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="51187-147">-HeaderActionType</span></span>
<span data-ttu-id="51187-148">İstek üst bilgisinin veya Yanıt üstbilgisinin değiştirilip güncelleştirilmeyeceğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="51187-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="51187-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="51187-149">-HeaderName</span></span>
<span data-ttu-id="51187-150">Değiştirilecek üst bilginin adı.</span><span class="sxs-lookup"><span data-stu-id="51187-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="51187-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="51187-151">-PreservePath</span></span>
<span data-ttu-id="51187-152">Eşleşmeyen yolun korunup korunmayacağı.</span><span class="sxs-lookup"><span data-stu-id="51187-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="51187-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="51187-153">-QueryParameter</span></span>
<span data-ttu-id="51187-154">İçerilecek veya dışlanacak sorgu parametreleri (virgülle ayrılmış).</span><span class="sxs-lookup"><span data-stu-id="51187-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="51187-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="51187-155">-QueryStringBehavior</span></span>
<span data-ttu-id="51187-156">İstekler için QueryString davranışı</span><span class="sxs-lookup"><span data-stu-id="51187-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="51187-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="51187-157">-RedirectType</span></span>
<span data-ttu-id="51187-158">Yeniden yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="51187-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="51187-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="51187-159">-SourcePattern</span></span>
<span data-ttu-id="51187-160">Yeniden yazılabilir isteklerin türünü tanımlayan bir istek URI deseni tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="51187-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="51187-161">Değer boşsa, tüm dizeler eşleştirilir.</span><span class="sxs-lookup"><span data-stu-id="51187-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="51187-162">-Değer</span><span class="sxs-lookup"><span data-stu-id="51187-162">-Value</span></span>
<span data-ttu-id="51187-163">Belirtilen eylem değeri.</span><span class="sxs-lookup"><span data-stu-id="51187-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="51187-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51187-164">CommonParameters</span></span>
<span data-ttu-id="51187-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51187-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51187-166">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="51187-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51187-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51187-167">INPUTS</span></span>

### <span data-ttu-id="51187-168">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="51187-168">None</span></span>

## <span data-ttu-id="51187-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51187-169">OUTPUTS</span></span>

### <span data-ttu-id="51187-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="51187-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="51187-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51187-171">NOTES</span></span>

## <span data-ttu-id="51187-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51187-172">RELATED LINKS</span></span>
