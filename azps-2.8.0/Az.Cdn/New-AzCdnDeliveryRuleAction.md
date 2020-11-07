---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753065"
---
# <span data-ttu-id="0c4d4-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="0c4d4-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="0c4d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="0c4d4-103">Teslim eylemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-103">Creates a delivery action.</span></span>

## <span data-ttu-id="0c4d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c4d4-104">SYNTAX</span></span>

### <span data-ttu-id="0c4d4-105">CacheExpirationActionParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c4d4-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c4d4-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4d4-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c4d4-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c4d4-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c4d4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c4d4-108">DESCRIPTION</span></span>
<span data-ttu-id="0c4d4-109">**New-AzCdnDeliveryRule** CMDLET 'i CDN uç noktası oluşturma için bir teslim kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="0c4d4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c4d4-110">EXAMPLES</span></span>

### <span data-ttu-id="0c4d4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c4d4-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="0c4d4-112">Basit bir teslim kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="0c4d4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c4d4-113">PARAMETERS</span></span>

### <span data-ttu-id="0c4d4-114">-Eylem</span><span class="sxs-lookup"><span data-stu-id="0c4d4-114">-Action</span></span>
<span data-ttu-id="0c4d4-115">Gerçekleştirilecek eylem.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-115">Action to perform.</span></span>

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

### <span data-ttu-id="0c4d4-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="0c4d4-116">-CacheBehavior</span></span>
<span data-ttu-id="0c4d4-117">Eylem için önbelleğe alma davranışı</span><span class="sxs-lookup"><span data-stu-id="0c4d4-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="0c4d4-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="0c4d4-118">-CacheDuration</span></span>
<span data-ttu-id="0c4d4-119">İçeriğin önbelleğe alınması gereken süre.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="0c4d4-120">İzin verilen biçim \[ d. \] ss: DD: ss</span><span class="sxs-lookup"><span data-stu-id="0c4d4-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="0c4d4-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="0c4d4-121">-CustomFragment</span></span>
<span data-ttu-id="0c4d4-122">Redirect URL 'ye eklenecek parça.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="0c4d4-123">Parça, # ' dan sonra gelen URL 'nin bölümüdür.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="0c4d4-124">#.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-124">Do not include the #.</span></span>

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

### <span data-ttu-id="0c4d4-125">-Customanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="0c4d4-125">-CustomHostname</span></span>
<span data-ttu-id="0c4d4-126">Yeniden yönlendirilecek ev.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-126">Host to redirect.</span></span>
<span data-ttu-id="0c4d4-127">Hedef ana bilgisayar olarak gelen ana bilgisayarı kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="0c4d4-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="0c4d4-128">-CustomPath</span></span>
<span data-ttu-id="0c4d4-129">Yeniden yönlendirilecek tam yol.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-129">The full path to redirect.</span></span>
<span data-ttu-id="0c4d4-130">Yol boş olamaz ve ile başlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="0c4d4-131">Gelen yolunu hedef yol olarak kullanmak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="0c4d4-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="0c4d4-132">-CustomQueryString</span></span>
<span data-ttu-id="0c4d4-133">Yönlendirme URL 'sine yerleştirilecek sorgu dizeleri kümesi.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="0c4d4-134">Bu değeri ayarlamak, var olan sorgu dizesinin yerini alır; gelen sorgu dizesini korumak için boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="0c4d4-135">Sorgu dizesi \< anahtar \> = \< değeri \> biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="0c4d4-136">?</span><span class="sxs-lookup"><span data-stu-id="0c4d4-136">?</span></span> <span data-ttu-id="0c4d4-137">ve & otomatik olarak eklenir; böylece bunları eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="0c4d4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c4d4-138">-DefaultProfile</span></span>
<span data-ttu-id="0c4d4-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c4d4-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="0c4d4-140">-DestinationProtocol</span></span>
<span data-ttu-id="0c4d4-141">Yönlendirme için kullanılacak protokol.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="0c4d4-142">Varsayılan değer MatchRequest değeridir.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="0c4d4-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="0c4d4-143">-HeaderActionType</span></span>
<span data-ttu-id="0c4d4-144">İstek üst bilgisinin veya Yanıt üstbilgisinin değiştirilip güncelleştirilmeyeceğini değiştirme</span><span class="sxs-lookup"><span data-stu-id="0c4d4-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="0c4d4-145">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="0c4d4-145">-HeaderName</span></span>
<span data-ttu-id="0c4d4-146">Değiştirilecek üst bilginin adı.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="0c4d4-147">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="0c4d4-147">-RedirectType</span></span>
<span data-ttu-id="0c4d4-148">Yeniden yönlendirme türü</span><span class="sxs-lookup"><span data-stu-id="0c4d4-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="0c4d4-149">-Değer</span><span class="sxs-lookup"><span data-stu-id="0c4d4-149">-Value</span></span>
<span data-ttu-id="0c4d4-150">Belirtilen eylem değeri.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="0c4d4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c4d4-151">CommonParameters</span></span>
<span data-ttu-id="0c4d4-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c4d4-153">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0c4d4-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c4d4-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c4d4-154">INPUTS</span></span>

### <span data-ttu-id="0c4d4-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0c4d4-155">None</span></span>

## <span data-ttu-id="0c4d4-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c4d4-156">OUTPUTS</span></span>

### <span data-ttu-id="0c4d4-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="0c4d4-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="0c4d4-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c4d4-158">NOTES</span></span>

## <span data-ttu-id="0c4d4-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c4d4-159">RELATED LINKS</span></span>
