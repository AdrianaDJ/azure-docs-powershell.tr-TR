---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9d8704abaeb5fd320a871b7b15720af3bbb0c472
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917568"
---
# <span data-ttu-id="797a9-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="797a9-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="797a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="797a9-102">SYNOPSIS</span></span>
<span data-ttu-id="797a9-103">CDN uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="797a9-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="797a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="797a9-104">SYNTAX</span></span>

### <span data-ttu-id="797a9-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="797a9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="797a9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="797a9-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="797a9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="797a9-107">DESCRIPTION</span></span>
<span data-ttu-id="797a9-108">**New-Azcıdnendpoint** cmdlet 'ı bir Azure Content Delivery Network (CDN) uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="797a9-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="797a9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="797a9-109">EXAMPLES</span></span>

## <span data-ttu-id="797a9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="797a9-110">PARAMETERS</span></span>

### <span data-ttu-id="797a9-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="797a9-111">-CdnProfile</span></span>
<span data-ttu-id="797a9-112">Uç noktanın eklendiği CDN profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="797a9-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="797a9-114">Edge düğümünden istemciye Sıkıştırılacak içerik türleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="797a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="797a9-115">-DefaultProfile</span></span>
<span data-ttu-id="797a9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="797a9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="797a9-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="797a9-117">-DeliveryPolicy</span></span>
<span data-ttu-id="797a9-118">Bu uç nokta için teslim ilkesi.</span><span class="sxs-lookup"><span data-stu-id="797a9-118">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="797a9-119">-EndpointName</span></span>
<span data-ttu-id="797a9-120">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="797a9-121">-Geofiller</span><span class="sxs-lookup"><span data-stu-id="797a9-121">-GeoFilters</span></span>
<span data-ttu-id="797a9-122">Bu uç noktaya uygulanan coğrafi filtreler listesi.</span><span class="sxs-lookup"><span data-stu-id="797a9-122">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="797a9-123">-HttpPort</span></span>
<span data-ttu-id="797a9-124">Kaynak sunucudaki HTTP bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-124">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="797a9-125">-HttpsPort</span></span>
<span data-ttu-id="797a9-126">Kaynak sunucudaki HTTPS bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-126">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="797a9-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="797a9-128">Uç nokta için sıkıştırmanın etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="797a9-128">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-129">-Ishttpallowed</span><span class="sxs-lookup"><span data-stu-id="797a9-129">-IsHttpAllowed</span></span>
<span data-ttu-id="797a9-130">Endpoint HTTP trafiğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="797a9-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-131">-Ishttpsallowed</span><span class="sxs-lookup"><span data-stu-id="797a9-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="797a9-132">Endpoint HTTPS trafiğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="797a9-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-133">-Konum</span><span class="sxs-lookup"><span data-stu-id="797a9-133">-Location</span></span>
<span data-ttu-id="797a9-134">Uç noktanın kaynak konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-134">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-135">-En Iyi yazma türü</span><span class="sxs-lookup"><span data-stu-id="797a9-135">-OptimizationType</span></span>
<span data-ttu-id="797a9-136">Bu uç noktanın sahip olduğu en iyi duruma getirmeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="797a9-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="797a9-137">-OriginHostHeader</span></span>
<span data-ttu-id="797a9-138">Uç noktasının kaynak ana bilgisayar kafasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="797a9-139">-Originanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="797a9-139">-OriginHostName</span></span>
<span data-ttu-id="797a9-140">Kaynak sunucunun ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="797a9-141">-AdName</span><span class="sxs-lookup"><span data-stu-id="797a9-141">-OriginName</span></span>
<span data-ttu-id="797a9-142">Kaynak sunucunun kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="797a9-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="797a9-143">-OriginPath</span></span>
<span data-ttu-id="797a9-144">Kaynak sunucunun yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="797a9-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="797a9-145">-ProbePath</span></span>
<span data-ttu-id="797a9-146">Dinamik site Ivmesi için yoklama yolunu belirtir</span><span class="sxs-lookup"><span data-stu-id="797a9-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="797a9-147">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="797a9-147">-ProfileName</span></span>
<span data-ttu-id="797a9-148">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-148">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="797a9-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="797a9-150">Sorgu dizesi istek URL 'sinde olduğunda CDN uç noktasının davranışını belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="797a9-151">-ResourceGroupName</span></span>
<span data-ttu-id="797a9-152">Bu uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="797a9-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-153">Etiketli</span><span class="sxs-lookup"><span data-stu-id="797a9-153">-Tag</span></span>
<span data-ttu-id="797a9-154">Azure CDN uç noktasıyla ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="797a9-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="797a9-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="797a9-155">-Confirm</span></span>
<span data-ttu-id="797a9-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="797a9-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="797a9-157">-WhatIf</span></span>
<span data-ttu-id="797a9-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="797a9-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="797a9-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="797a9-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797a9-160">CommonParameters</span></span>
<span data-ttu-id="797a9-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="797a9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797a9-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="797a9-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797a9-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="797a9-163">INPUTS</span></span>

### <span data-ttu-id="797a9-164">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="797a9-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="797a9-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="797a9-165">OUTPUTS</span></span>

### <span data-ttu-id="797a9-166">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="797a9-166">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="797a9-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="797a9-167">NOTES</span></span>

## <span data-ttu-id="797a9-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="797a9-168">RELATED LINKS</span></span>

[<span data-ttu-id="797a9-169">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="797a9-169">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="797a9-170">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="797a9-170">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="797a9-171">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="797a9-171">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="797a9-172">Başlangıç-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="797a9-172">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="797a9-173">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="797a9-173">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


