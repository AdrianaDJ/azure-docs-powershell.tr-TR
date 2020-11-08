---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109237"
---
# <span data-ttu-id="a475b-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a475b-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="a475b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a475b-102">SYNOPSIS</span></span>
<span data-ttu-id="a475b-103">Bir API 'YI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a475b-103">Modifies an API.</span></span>

## <span data-ttu-id="a475b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a475b-104">SYNTAX</span></span>

### <span data-ttu-id="a475b-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a475b-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a475b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a475b-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a475b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a475b-107">DESCRIPTION</span></span>
<span data-ttu-id="a475b-108">**Set-Azapsananagementapı** cmdlet 'ı BIR Azure API yönetim API 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a475b-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="a475b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a475b-109">EXAMPLES</span></span>

### <span data-ttu-id="a475b-110">Örnek 1: API 'YI değiştirme</span><span class="sxs-lookup"><span data-stu-id="a475b-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="a475b-111">Örnek 2: var olan bir Apıversionset 'e API ekleme</span><span class="sxs-lookup"><span data-stu-id="a475b-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="a475b-112">Bu örnek, var olan bir API sürüm kümesine API ekler</span><span class="sxs-lookup"><span data-stu-id="a475b-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="a475b-113">Örnek 3: API 'nin üzerine geldiği arka uç ServiceUrl 'Sini değiştirme</span><span class="sxs-lookup"><span data-stu-id="a475b-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="a475b-114">Bu örnek, işaret eden ServiceUrl 'Sini güncelleştirir `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="a475b-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="a475b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a475b-115">PARAMETERS</span></span>

### <span data-ttu-id="a475b-116">-Apııd</span><span class="sxs-lookup"><span data-stu-id="a475b-116">-ApiId</span></span>
<span data-ttu-id="a475b-117">Değiştirilecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="a475b-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="a475b-118">-AuthorizationScope</span></span>
<span data-ttu-id="a475b-119">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="a475b-120">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="a475b-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="a475b-121">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="a475b-121">-AuthorizationServerId</span></span>
<span data-ttu-id="a475b-122">OAuth yetkilendirme sunucusu tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="a475b-123">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="a475b-123">The default value is $Null.</span></span>
<span data-ttu-id="a475b-124">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a475b-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="a475b-125">-Yataertokensendingmethod</span><span class="sxs-lookup"><span data-stu-id="a475b-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="a475b-126">API 'ya erişim belirtecinin geçirildiği OpenID yetkilendirme sunucusu mekanizması.</span><span class="sxs-lookup"><span data-stu-id="a475b-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="a475b-127">Bölümüne bakın http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="a475b-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="a475b-128">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a475b-128">This parameter is optional.</span></span> <span data-ttu-id="a475b-129">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="a475b-129">Default value is $null.</span></span>

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

### <span data-ttu-id="a475b-130">-Context</span><span class="sxs-lookup"><span data-stu-id="a475b-130">-Context</span></span>
<span data-ttu-id="a475b-131">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a475b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a475b-132">-DefaultProfile</span></span>
<span data-ttu-id="a475b-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a475b-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a475b-134">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a475b-134">-Description</span></span>
<span data-ttu-id="a475b-135">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="a475b-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a475b-136">-InputObject</span></span>
<span data-ttu-id="a475b-137">PsApiManagementApi örneği.</span><span class="sxs-lookup"><span data-stu-id="a475b-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="a475b-138">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a475b-138">This parameter is required.</span></span>

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

### <span data-ttu-id="a475b-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="a475b-139">-Name</span></span>
<span data-ttu-id="a475b-140">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="a475b-141">-Openıdproviderıd</span><span class="sxs-lookup"><span data-stu-id="a475b-141">-OpenIdProviderId</span></span>
<span data-ttu-id="a475b-142">OpenID yetkilendirme sunucusu tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a475b-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="a475b-143">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a475b-143">This parameter is optional.</span></span> <span data-ttu-id="a475b-144">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="a475b-144">Default value is $null.</span></span> <span data-ttu-id="a475b-145">Yataertokensendingmethods belirtilmişse, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a475b-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="a475b-146">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a475b-146">-PassThru</span></span>
<span data-ttu-id="a475b-147">geçiş</span><span class="sxs-lookup"><span data-stu-id="a475b-147">passthru</span></span>

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

### <span data-ttu-id="a475b-148">-Yol</span><span class="sxs-lookup"><span data-stu-id="a475b-148">-Path</span></span>
<span data-ttu-id="a475b-149">API 'nin Genel URL 'sinin son bölümü olan Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="a475b-150">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a475b-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="a475b-151">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="a475b-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="a475b-152">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="a475b-152">-Protocols</span></span>
<span data-ttu-id="a475b-153">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="a475b-154">http ve https psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="a475b-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="a475b-155">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="a475b-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="a475b-156">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="a475b-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="a475b-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="a475b-157">-ServiceUrl</span></span>
<span data-ttu-id="a475b-158">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="a475b-159">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="a475b-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="a475b-160">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a475b-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="a475b-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="a475b-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="a475b-162">Abonelik anahtarı üstbilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="a475b-163">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="a475b-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="a475b-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="a475b-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="a475b-165">Abonelik anahtarı sorgu dizesi parametresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a475b-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="a475b-166">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="a475b-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="a475b-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="a475b-167">-SubscriptionRequired</span></span>
<span data-ttu-id="a475b-168">API için istekler için aboneliğinizi zorunlu kılma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="a475b-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="a475b-169">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a475b-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="a475b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a475b-170">CommonParameters</span></span>
<span data-ttu-id="a475b-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a475b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a475b-172">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a475b-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a475b-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a475b-173">INPUTS</span></span>

### <span data-ttu-id="a475b-174">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a475b-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a475b-175">System. String</span><span class="sxs-lookup"><span data-stu-id="a475b-175">System.String</span></span>

### <span data-ttu-id="a475b-176">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a475b-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="a475b-177">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="a475b-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="a475b-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a475b-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a475b-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a475b-179">OUTPUTS</span></span>

### <span data-ttu-id="a475b-180">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a475b-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="a475b-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a475b-181">NOTES</span></span>

## <span data-ttu-id="a475b-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a475b-182">RELATED LINKS</span></span>

[<span data-ttu-id="a475b-183">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a475b-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="a475b-184">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a475b-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="a475b-185">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a475b-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="a475b-186">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="a475b-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="a475b-187">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a475b-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


