---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 5d2bfdf2bf5f87ccb0213c006de8612b5eaf0730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592657"
---
# <span data-ttu-id="bd11b-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd11b-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="bd11b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd11b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd11b-103">CDN uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd11b-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd11b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd11b-104">SYNTAX</span></span>

### <span data-ttu-id="bd11b-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd11b-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd11b-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="bd11b-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd11b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd11b-107">DESCRIPTION</span></span>
<span data-ttu-id="bd11b-108">**New-AzureRmCdnEndpoint** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd11b-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="bd11b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd11b-109">EXAMPLES</span></span>

## <span data-ttu-id="bd11b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd11b-110">PARAMETERS</span></span>

### <span data-ttu-id="bd11b-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="bd11b-111">-CdnProfile</span></span>
<span data-ttu-id="bd11b-112">Uç noktanın eklendiği CDN profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd11b-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="bd11b-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="bd11b-114">Edge düğümünden istemciye Sıkıştırılacak içerik türleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="bd11b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bd11b-115">-EndpointName</span></span>
<span data-ttu-id="bd11b-116">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="bd11b-117">-Geofiller</span><span class="sxs-lookup"><span data-stu-id="bd11b-117">-GeoFilters</span></span>
<span data-ttu-id="bd11b-118">Bu uç noktaya uygulanan coğrafi filtreler listesi.</span><span class="sxs-lookup"><span data-stu-id="bd11b-118">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="bd11b-119">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="bd11b-119">-HttpPort</span></span>
<span data-ttu-id="bd11b-120">Kaynak sunucudaki HTTP bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-120">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="bd11b-121">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="bd11b-121">-HttpsPort</span></span>
<span data-ttu-id="bd11b-122">Kaynak sunucudaki HTTPS bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-122">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="bd11b-123">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="bd11b-123">-IsCompressionEnabled</span></span>
<span data-ttu-id="bd11b-124">Uç nokta için sıkıştırmanın etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-124">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="bd11b-125">-Ishttpallowed</span><span class="sxs-lookup"><span data-stu-id="bd11b-125">-IsHttpAllowed</span></span>
<span data-ttu-id="bd11b-126">Endpoint HTTP trafiğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-126">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="bd11b-127">-Ishttpsallowed</span><span class="sxs-lookup"><span data-stu-id="bd11b-127">-IsHttpsAllowed</span></span>
<span data-ttu-id="bd11b-128">Endpoint HTTPS trafiğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-128">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="bd11b-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="bd11b-129">-Location</span></span>
<span data-ttu-id="bd11b-130">Uç noktanın kaynak konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-130">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd11b-131">-En Iyi yazma türü</span><span class="sxs-lookup"><span data-stu-id="bd11b-131">-OptimizationType</span></span>
<span data-ttu-id="bd11b-132">Bu uç noktanın sahip olduğu en iyi duruma getirmeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-132">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="bd11b-133">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="bd11b-133">-OriginHostHeader</span></span>
<span data-ttu-id="bd11b-134">Uç noktasının kaynak ana bilgisayar kafasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-134">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="bd11b-135">-Originanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="bd11b-135">-OriginHostName</span></span>
<span data-ttu-id="bd11b-136">Kaynak sunucunun ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-136">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="bd11b-137">-AdName</span><span class="sxs-lookup"><span data-stu-id="bd11b-137">-OriginName</span></span>
<span data-ttu-id="bd11b-138">Kaynak sunucunun kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-138">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="bd11b-139">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="bd11b-139">-OriginPath</span></span>
<span data-ttu-id="bd11b-140">Kaynak sunucunun yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-140">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="bd11b-141">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bd11b-141">-ProfileName</span></span>
<span data-ttu-id="bd11b-142">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-142">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd11b-143">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="bd11b-143">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="bd11b-144">Sorgu dizesi istek URL 'sinde olduğunda CDN uç noktasının davranışını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-144">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="bd11b-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd11b-145">-ResourceGroupName</span></span>
<span data-ttu-id="bd11b-146">Bu uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-146">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd11b-147">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="bd11b-147">-Tags</span></span>
<span data-ttu-id="bd11b-148">Bu kaynakla ilişkili etiketlerin karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-148">Specifies a hash table of the tags that associated with this resource.</span></span>

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

### <span data-ttu-id="bd11b-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd11b-149">-Confirm</span></span>
<span data-ttu-id="bd11b-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd11b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd11b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd11b-151">-WhatIf</span></span>
<span data-ttu-id="bd11b-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd11b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd11b-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd11b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd11b-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd11b-154">-DefaultProfile</span></span>
<span data-ttu-id="bd11b-155">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd11b-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd11b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd11b-156">CommonParameters</span></span>
<span data-ttu-id="bd11b-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd11b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd11b-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd11b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd11b-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd11b-159">INPUTS</span></span>

### <span data-ttu-id="bd11b-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="bd11b-160">PSProfile</span></span>
<span data-ttu-id="bd11b-161">' CdnProfile ' parametresi ardışık düzenin ' PSProfile ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bd11b-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="bd11b-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd11b-162">OUTPUTS</span></span>

### <span data-ttu-id="bd11b-163">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd11b-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bd11b-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd11b-164">NOTES</span></span>

## <span data-ttu-id="bd11b-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd11b-165">RELATED LINKS</span></span>

[<span data-ttu-id="bd11b-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd11b-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bd11b-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd11b-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bd11b-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd11b-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bd11b-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd11b-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="bd11b-170">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bd11b-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)

