---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: b332ccc8dc9188259c897c53256f1a14fd96280e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753555"
---
# <span data-ttu-id="be4d0-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="be4d0-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="be4d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="be4d0-103">Bir API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be4d0-103">Creates an API.</span></span>

## <span data-ttu-id="be4d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be4d0-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be4d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be4d0-105">DESCRIPTION</span></span>
<span data-ttu-id="be4d0-106">**Yeni-Azapsananagementapı** cmdlet 'ı BIR Azure API yönetim API 'si oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be4d0-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="be4d0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be4d0-107">EXAMPLES</span></span>

### <span data-ttu-id="be4d0-108">Örnek 1: API oluşturma</span><span class="sxs-lookup"><span data-stu-id="be4d0-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="be4d0-109">Bu komut, belirtilen URL ile yankı adlı bir API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be4d0-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="be4d0-110">Örnek 1: tüm işlemleri, etiketleri, ürünleri ve Ilkeleri Echo-API ' t a bir Apıversionset 'e kopyalayarak bir API oluşturma</span><span class="sxs-lookup"><span data-stu-id="be4d0-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="be4d0-111">Bu komut `echoapiv3` Apıversionset içinde BIR API oluşturur `xmsVersionSet` ve tüm Işlem, etiket ve Ilkeleri kaynak API 'den kopyalar `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="be4d0-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="be4d0-112">Bu, aboneliği gerekli, ServiceUrl, yol, protokolleri geçersiz kılar</span><span class="sxs-lookup"><span data-stu-id="be4d0-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="be4d0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be4d0-113">PARAMETERS</span></span>

### <span data-ttu-id="be4d0-114">-Apııd</span><span class="sxs-lookup"><span data-stu-id="be4d0-114">-ApiId</span></span>
<span data-ttu-id="be4d0-115">Oluşturulacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="be4d0-116">Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir KIMLIK oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be4d0-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="be4d0-117">-ApiVersion</span></span>
<span data-ttu-id="be4d0-118">API 'nın oluşturulacağı API sürümü.</span><span class="sxs-lookup"><span data-stu-id="be4d0-118">Api Version of the Api to create.</span></span> <span data-ttu-id="be4d0-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-120">-Apıversiondescription</span><span class="sxs-lookup"><span data-stu-id="be4d0-120">-ApiVersionDescription</span></span>
<span data-ttu-id="be4d0-121">API sürüm açıklaması.</span><span class="sxs-lookup"><span data-stu-id="be4d0-121">Api Version Description.</span></span> <span data-ttu-id="be4d0-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-123">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="be4d0-123">-ApiVersionSetId</span></span>
<span data-ttu-id="be4d0-124">İlgili API sürüm kümesi için bir kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="be4d0-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="be4d0-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-125">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="be4d0-126">-AuthorizationScope</span></span>
<span data-ttu-id="be4d0-127">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="be4d0-128">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="be4d0-128">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-129">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="be4d0-129">-AuthorizationServerId</span></span>
<span data-ttu-id="be4d0-130">OAuth yetkilendirme sunucusu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="be4d0-131">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="be4d0-131">The default value is $Null.</span></span>
<span data-ttu-id="be4d0-132">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-133">-Yataertokensendingmethod</span><span class="sxs-lookup"><span data-stu-id="be4d0-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="be4d0-134">API 'ya erişim belirtecinin geçirildiği OpenID yetkilendirme sunucusu mekanizması.</span><span class="sxs-lookup"><span data-stu-id="be4d0-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="be4d0-135">Bölümüne bakın http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="be4d0-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="be4d0-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-136">This parameter is optional.</span></span> <span data-ttu-id="be4d0-137">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="be4d0-137">Default value is $null.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-138">-Context</span><span class="sxs-lookup"><span data-stu-id="be4d0-138">-Context</span></span>
<span data-ttu-id="be4d0-139">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-139">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be4d0-140">-DefaultProfile</span></span>
<span data-ttu-id="be4d0-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be4d0-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be4d0-142">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="be4d0-142">-Description</span></span>
<span data-ttu-id="be4d0-143">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-143">Specifies a description for the web API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="be4d0-144">-Name</span></span>
<span data-ttu-id="be4d0-145">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="be4d0-146">Bu, API 'nin geliştirici ve yönetici portalında göründüğü şekliyle genel adıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-147">-Openıdproviderıd</span><span class="sxs-lookup"><span data-stu-id="be4d0-147">-OpenIdProviderId</span></span>
<span data-ttu-id="be4d0-148">OpenID yetkilendirme sunucusu tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="be4d0-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="be4d0-149">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-149">This parameter is optional.</span></span> <span data-ttu-id="be4d0-150">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="be4d0-150">Default value is $null.</span></span> <span data-ttu-id="be4d0-151">Yataertokensendingmethods belirtilmişse, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-152">-Yol</span><span class="sxs-lookup"><span data-stu-id="be4d0-152">-Path</span></span>
<span data-ttu-id="be4d0-153">API 'nin Genel URL 'sinin son bölümü olan ve yönetici portalında Web API URL soneki alanına karşılık gelen Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="be4d0-154">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="be4d0-155">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="be4d0-155">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-156">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="be4d0-156">-ProductIds</span></span>
<span data-ttu-id="be4d0-157">Yeni API 'yi ekleyeceğiniz ürün kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-157">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-158">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="be4d0-158">-Protocols</span></span>
<span data-ttu-id="be4d0-159">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="be4d0-160">Geçerli değerler http, https 'dir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-160">Valid values are http, https.</span></span>
<span data-ttu-id="be4d0-161">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="be4d0-162">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="be4d0-162">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="be4d0-163">-ServiceUrl</span></span>
<span data-ttu-id="be4d0-164">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="be4d0-165">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="be4d0-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="be4d0-166">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-166">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-167">-Sourceapııd</span><span class="sxs-lookup"><span data-stu-id="be4d0-167">-SourceApiId</span></span>
<span data-ttu-id="be4d0-168">Kaynak API 'sının API tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="be4d0-168">Api identifier of the source API.</span></span> <span data-ttu-id="be4d0-169">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-169">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-170">-Sourceapırevision</span><span class="sxs-lookup"><span data-stu-id="be4d0-170">-SourceApiRevision</span></span>
<span data-ttu-id="be4d0-171">Kaynak API 'nın API düzeltmesi.</span><span class="sxs-lookup"><span data-stu-id="be4d0-171">Api Revision of the source API.</span></span> <span data-ttu-id="be4d0-172">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-172">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-173">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="be4d0-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="be4d0-174">Abonelik anahtarı üst bilgi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="be4d0-175">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="be4d0-175">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="be4d0-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="be4d0-177">Abonelik anahtarı sorgu dizesi parametre adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="be4d0-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="be4d0-178">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="be4d0-178">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="be4d0-179">-SubscriptionRequired</span></span>
<span data-ttu-id="be4d0-180">API için istekler için aboneliğinizi zorunlu kılma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="be4d0-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="be4d0-181">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="be4d0-181">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be4d0-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be4d0-182">CommonParameters</span></span>
<span data-ttu-id="be4d0-183">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be4d0-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be4d0-184">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="be4d0-184">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be4d0-185">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be4d0-185">INPUTS</span></span>

### <span data-ttu-id="be4d0-186">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="be4d0-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="be4d0-187">System. String</span><span class="sxs-lookup"><span data-stu-id="be4d0-187">System.String</span></span>

### <span data-ttu-id="be4d0-188">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="be4d0-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="be4d0-189">System. String []</span><span class="sxs-lookup"><span data-stu-id="be4d0-189">System.String[]</span></span>

## <span data-ttu-id="be4d0-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be4d0-190">OUTPUTS</span></span>

### <span data-ttu-id="be4d0-191">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="be4d0-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="be4d0-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be4d0-192">NOTES</span></span>

## <span data-ttu-id="be4d0-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be4d0-193">RELATED LINKS</span></span>

[<span data-ttu-id="be4d0-194">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="be4d0-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="be4d0-195">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="be4d0-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="be4d0-196">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="be4d0-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="be4d0-197">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="be4d0-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="be4d0-198">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="be4d0-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


