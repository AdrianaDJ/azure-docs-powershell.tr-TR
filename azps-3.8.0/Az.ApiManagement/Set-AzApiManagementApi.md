---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 482a558e469e3f8094e4b619ef61ec37f076f739
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103865"
---
# <span data-ttu-id="d0e49-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d0e49-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="d0e49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0e49-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e49-103">Bir API 'YI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-103">Modifies an API.</span></span>

## <span data-ttu-id="d0e49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0e49-104">SYNTAX</span></span>

### <span data-ttu-id="d0e49-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d0e49-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0e49-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d0e49-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0e49-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0e49-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e49-108">**Set-Azapsananagementapı** cmdlet 'ı BIR Azure API yönetim API 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="d0e49-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0e49-109">EXAMPLES</span></span>

### <span data-ttu-id="d0e49-110">Örnek 1 API 'YI değiştirme</span><span class="sxs-lookup"><span data-stu-id="d0e49-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="d0e49-111">Örnek 2 var olan Apıversionset 'e API ekleme</span><span class="sxs-lookup"><span data-stu-id="d0e49-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="d0e49-112">Bu örnek, var olan bir API sürüm kümesine API ekler</span><span class="sxs-lookup"><span data-stu-id="d0e49-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="d0e49-113">Örnek 3 API 'nin üzerine geldiği arka uç ServiceUrl 'Sini değiştirme</span><span class="sxs-lookup"><span data-stu-id="d0e49-113">Example 3 Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="d0e49-114">Bu örnek, işaret eden ServiceUrl 'Sini güncelleştirir `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="d0e49-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="d0e49-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0e49-115">PARAMETERS</span></span>

### <span data-ttu-id="d0e49-116">-Apııd</span><span class="sxs-lookup"><span data-stu-id="d0e49-116">-ApiId</span></span>
<span data-ttu-id="d0e49-117">Değiştirilecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-117">Specifies the ID of the API to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e49-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="d0e49-118">-AuthorizationScope</span></span>
<span data-ttu-id="d0e49-119">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="d0e49-120">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="d0e49-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="d0e49-121">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="d0e49-121">-AuthorizationServerId</span></span>
<span data-ttu-id="d0e49-122">OAuth yetkilendirme sunucusu tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="d0e49-123">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="d0e49-123">The default value is $Null.</span></span>
<span data-ttu-id="d0e49-124">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="d0e49-125">-Yataertokensendingmethod</span><span class="sxs-lookup"><span data-stu-id="d0e49-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="d0e49-126">API 'ya erişim belirtecinin geçirildiği OpenID yetkilendirme sunucusu mekanizması.</span><span class="sxs-lookup"><span data-stu-id="d0e49-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="d0e49-127">Bölümüne bakın http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="d0e49-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="d0e49-128">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d0e49-128">This parameter is optional.</span></span> <span data-ttu-id="d0e49-129">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="d0e49-129">Default value is $null.</span></span>

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

### <span data-ttu-id="d0e49-130">-Context</span><span class="sxs-lookup"><span data-stu-id="d0e49-130">-Context</span></span>
<span data-ttu-id="d0e49-131">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-131">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e49-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e49-132">-DefaultProfile</span></span>
<span data-ttu-id="d0e49-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0e49-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0e49-134">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d0e49-134">-Description</span></span>
<span data-ttu-id="d0e49-135">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="d0e49-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0e49-136">-InputObject</span></span>
<span data-ttu-id="d0e49-137">PsApiManagementApi örneği.</span><span class="sxs-lookup"><span data-stu-id="d0e49-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="d0e49-138">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-138">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e49-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="d0e49-139">-Name</span></span>
<span data-ttu-id="d0e49-140">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="d0e49-141">-Openıdproviderıd</span><span class="sxs-lookup"><span data-stu-id="d0e49-141">-OpenIdProviderId</span></span>
<span data-ttu-id="d0e49-142">OpenID yetkilendirme sunucusu tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d0e49-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="d0e49-143">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d0e49-143">This parameter is optional.</span></span> <span data-ttu-id="d0e49-144">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="d0e49-144">Default value is $null.</span></span> <span data-ttu-id="d0e49-145">Yataertokensendingmethods belirtilmişse, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="d0e49-146">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d0e49-146">-PassThru</span></span>
<span data-ttu-id="d0e49-147">geçiş</span><span class="sxs-lookup"><span data-stu-id="d0e49-147">passthru</span></span>

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

### <span data-ttu-id="d0e49-148">-Yol</span><span class="sxs-lookup"><span data-stu-id="d0e49-148">-Path</span></span>
<span data-ttu-id="d0e49-149">API 'nin Genel URL 'sinin son bölümü olan Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="d0e49-150">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d0e49-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="d0e49-151">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="d0e49-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="d0e49-152">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="d0e49-152">-Protocols</span></span>
<span data-ttu-id="d0e49-153">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="d0e49-154">http ve https psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="d0e49-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="d0e49-155">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="d0e49-156">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="d0e49-156">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0e49-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="d0e49-157">-ServiceUrl</span></span>
<span data-ttu-id="d0e49-158">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="d0e49-159">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="d0e49-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="d0e49-160">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d0e49-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="d0e49-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="d0e49-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="d0e49-162">Abonelik anahtarı üstbilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="d0e49-163">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="d0e49-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="d0e49-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="d0e49-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="d0e49-165">Abonelik anahtarı sorgu dizesi parametresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0e49-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="d0e49-166">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="d0e49-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="d0e49-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="d0e49-167">-SubscriptionRequired</span></span>
<span data-ttu-id="d0e49-168">API için istekler için aboneliğinizi zorunlu kılma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="d0e49-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="d0e49-169">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d0e49-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="d0e49-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e49-170">CommonParameters</span></span>
<span data-ttu-id="d0e49-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0e49-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e49-172">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d0e49-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e49-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0e49-173">INPUTS</span></span>

### <span data-ttu-id="d0e49-174">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="d0e49-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d0e49-175">System. String</span><span class="sxs-lookup"><span data-stu-id="d0e49-175">System.String</span></span>

### <span data-ttu-id="d0e49-176">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="d0e49-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="d0e49-177">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="d0e49-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="d0e49-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d0e49-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d0e49-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0e49-179">OUTPUTS</span></span>

### <span data-ttu-id="d0e49-180">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="d0e49-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d0e49-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0e49-181">NOTES</span></span>

## <span data-ttu-id="d0e49-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0e49-182">RELATED LINKS</span></span>

[<span data-ttu-id="d0e49-183">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="d0e49-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="d0e49-184">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="d0e49-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="d0e49-185">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="d0e49-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="d0e49-186">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="d0e49-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="d0e49-187">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="d0e49-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


