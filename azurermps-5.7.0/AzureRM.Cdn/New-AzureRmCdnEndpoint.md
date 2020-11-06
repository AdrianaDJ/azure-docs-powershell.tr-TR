---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587650"
---
# <span data-ttu-id="61ba9-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="61ba9-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="61ba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="61ba9-103">CDN uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61ba9-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61ba9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61ba9-104">SYNTAX</span></span>

### <span data-ttu-id="61ba9-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61ba9-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61ba9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61ba9-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ba9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="61ba9-107">DESCRIPTION</span></span>
<span data-ttu-id="61ba9-108">**New-AzureRmCdnEndpoint** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61ba9-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="61ba9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61ba9-109">EXAMPLES</span></span>

## <span data-ttu-id="61ba9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61ba9-110">PARAMETERS</span></span>

### <span data-ttu-id="61ba9-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="61ba9-111">-CdnProfile</span></span>
<span data-ttu-id="61ba9-112">Uç noktanın eklendiği CDN profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="61ba9-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="61ba9-114">Edge düğümünden istemciye Sıkıştırılacak içerik türleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ba9-115">-DefaultProfile</span></span>
<span data-ttu-id="61ba9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="61ba9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="61ba9-117">-EndpointName</span></span>
<span data-ttu-id="61ba9-118">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-119">-Geofiller</span><span class="sxs-lookup"><span data-stu-id="61ba9-119">-GeoFilters</span></span>
<span data-ttu-id="61ba9-120">Bu uç noktaya uygulanan coğrafi filtreler listesi.</span><span class="sxs-lookup"><span data-stu-id="61ba9-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="61ba9-121">-HttpPort</span></span>
<span data-ttu-id="61ba9-122">Kaynak sunucudaki HTTP bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="61ba9-123">-HttpsPort</span></span>
<span data-ttu-id="61ba9-124">Kaynak sunucudaki HTTPS bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="61ba9-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="61ba9-126">Uç nokta için sıkıştırmanın etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-127">-Ishttpallowed</span><span class="sxs-lookup"><span data-stu-id="61ba9-127">-IsHttpAllowed</span></span>
<span data-ttu-id="61ba9-128">Endpoint HTTP trafiğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-129">-Ishttpsallowed</span><span class="sxs-lookup"><span data-stu-id="61ba9-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="61ba9-130">Endpoint HTTPS trafiğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="61ba9-131">-Location</span></span>
<span data-ttu-id="61ba9-132">Uç noktanın kaynak konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-133">-En Iyi yazma türü</span><span class="sxs-lookup"><span data-stu-id="61ba9-133">-OptimizationType</span></span>
<span data-ttu-id="61ba9-134">Bu uç noktanın sahip olduğu en iyi duruma getirmeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-134">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="61ba9-135">-OriginHostHeader</span></span>
<span data-ttu-id="61ba9-136">Uç noktasının kaynak ana bilgisayar kafasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-136">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-137">-Originanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="61ba9-137">-OriginHostName</span></span>
<span data-ttu-id="61ba9-138">Kaynak sunucunun ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-138">Specifies the host name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-139">-AdName</span><span class="sxs-lookup"><span data-stu-id="61ba9-139">-OriginName</span></span>
<span data-ttu-id="61ba9-140">Kaynak sunucunun kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-140">Specifies the resource name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="61ba9-141">-OriginPath</span></span>
<span data-ttu-id="61ba9-142">Kaynak sunucunun yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-142">Specifies the path of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-143">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="61ba9-143">-ProfileName</span></span>
<span data-ttu-id="61ba9-144">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="61ba9-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="61ba9-146">Sorgu dizesi istek URL 'sinde olduğunda CDN uç noktasının davranışını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ba9-147">-ResourceGroupName</span></span>
<span data-ttu-id="61ba9-148">Bu uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-149">Etiketli</span><span class="sxs-lookup"><span data-stu-id="61ba9-149">-Tag</span></span>
<span data-ttu-id="61ba9-150">Azure CDN uç noktasıyla ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="61ba9-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="61ba9-151">-Confirm</span></span>
<span data-ttu-id="61ba9-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61ba9-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ba9-153">-WhatIf</span></span>
<span data-ttu-id="61ba9-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61ba9-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61ba9-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61ba9-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61ba9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ba9-156">CommonParameters</span></span>
<span data-ttu-id="61ba9-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61ba9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ba9-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61ba9-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ba9-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61ba9-159">INPUTS</span></span>

### <span data-ttu-id="61ba9-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="61ba9-160">PSProfile</span></span>
<span data-ttu-id="61ba9-161">' CdnProfile ' parametresi ardışık düzenin ' PSProfile ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="61ba9-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="61ba9-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61ba9-162">OUTPUTS</span></span>

### <span data-ttu-id="61ba9-163">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="61ba9-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="61ba9-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61ba9-164">NOTES</span></span>

## <span data-ttu-id="61ba9-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61ba9-165">RELATED LINKS</span></span>

[<span data-ttu-id="61ba9-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="61ba9-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="61ba9-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="61ba9-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="61ba9-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="61ba9-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="61ba9-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="61ba9-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="61ba9-170">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="61ba9-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


