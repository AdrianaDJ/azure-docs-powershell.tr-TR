---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321909"
---
# <span data-ttu-id="2ea4f-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2ea4f-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="2ea4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ea4f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea4f-103">Bir API 'YI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-103">Modifies an API.</span></span>

## <span data-ttu-id="2ea4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ea4f-104">SYNTAX</span></span>

### <span data-ttu-id="2ea4f-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ea4f-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ea4f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2ea4f-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ea4f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ea4f-107">DESCRIPTION</span></span>
<span data-ttu-id="2ea4f-108">**Set-Azapsananagementapı** cmdlet 'ı BIR Azure API yönetim API 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="2ea4f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ea4f-109">EXAMPLES</span></span>

### <span data-ttu-id="2ea4f-110">Örnek 1: API 'YI değiştirme</span><span class="sxs-lookup"><span data-stu-id="2ea4f-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="2ea4f-111">Örnek 2: var olan bir Apıversionset 'e API ekleme</span><span class="sxs-lookup"><span data-stu-id="2ea4f-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="2ea4f-112">Bu örnek, var olan bir API sürüm kümesine API ekler</span><span class="sxs-lookup"><span data-stu-id="2ea4f-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="2ea4f-113">Örnek 3: API 'nin üzerine geldiği arka uç ServiceUrl 'Sini değiştirme</span><span class="sxs-lookup"><span data-stu-id="2ea4f-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="2ea4f-114">Bu örnek, işaret eden ServiceUrl 'Sini güncelleştirir `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="2ea4f-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="2ea4f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ea4f-115">PARAMETERS</span></span>

### <span data-ttu-id="2ea4f-116">-Apııd</span><span class="sxs-lookup"><span data-stu-id="2ea4f-116">-ApiId</span></span>
<span data-ttu-id="2ea4f-117">Değiştirilecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="2ea4f-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2ea4f-118">-AuthorizationScope</span></span>
<span data-ttu-id="2ea4f-119">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2ea4f-120">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="2ea4f-121">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="2ea4f-121">-AuthorizationServerId</span></span>
<span data-ttu-id="2ea4f-122">OAuth yetkilendirme sunucusu tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="2ea4f-123">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-123">The default value is $Null.</span></span>
<span data-ttu-id="2ea4f-124">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="2ea4f-125">-Yataertokensendingmethod</span><span class="sxs-lookup"><span data-stu-id="2ea4f-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="2ea4f-126">API 'ya erişim belirtecinin geçirildiği OpenID yetkilendirme sunucusu mekanizması.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="2ea4f-127">Bölümüne bakın http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="2ea4f-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="2ea4f-128">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-128">This parameter is optional.</span></span> <span data-ttu-id="2ea4f-129">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-129">Default value is $null.</span></span>

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

### <span data-ttu-id="2ea4f-130">-Context</span><span class="sxs-lookup"><span data-stu-id="2ea4f-130">-Context</span></span>
<span data-ttu-id="2ea4f-131">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2ea4f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea4f-132">-DefaultProfile</span></span>
<span data-ttu-id="2ea4f-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ea4f-134">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="2ea4f-134">-Description</span></span>
<span data-ttu-id="2ea4f-135">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="2ea4f-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ea4f-136">-InputObject</span></span>
<span data-ttu-id="2ea4f-137">PsApiManagementApi örneği.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="2ea4f-138">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-138">This parameter is required.</span></span>

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

### <span data-ttu-id="2ea4f-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ea4f-139">-Name</span></span>
<span data-ttu-id="2ea4f-140">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="2ea4f-141">-Openıdproviderıd</span><span class="sxs-lookup"><span data-stu-id="2ea4f-141">-OpenIdProviderId</span></span>
<span data-ttu-id="2ea4f-142">OpenID yetkilendirme sunucusu tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="2ea4f-143">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-143">This parameter is optional.</span></span> <span data-ttu-id="2ea4f-144">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-144">Default value is $null.</span></span> <span data-ttu-id="2ea4f-145">Yataertokensendingmethods belirtilmişse, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="2ea4f-146">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2ea4f-146">-PassThru</span></span>
<span data-ttu-id="2ea4f-147">geçiş</span><span class="sxs-lookup"><span data-stu-id="2ea4f-147">passthru</span></span>

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

### <span data-ttu-id="2ea4f-148">-Yol</span><span class="sxs-lookup"><span data-stu-id="2ea4f-148">-Path</span></span>
<span data-ttu-id="2ea4f-149">API 'nin Genel URL 'sinin son bölümü olan Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="2ea4f-150">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2ea4f-151">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="2ea4f-152">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="2ea4f-152">-Protocols</span></span>
<span data-ttu-id="2ea4f-153">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2ea4f-154">http ve https psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="2ea4f-155">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2ea4f-156">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="2ea4f-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2ea4f-157">-ServiceUrl</span></span>
<span data-ttu-id="2ea4f-158">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2ea4f-159">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2ea4f-160">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="2ea4f-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="2ea4f-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2ea4f-162">Abonelik anahtarı üstbilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="2ea4f-163">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="2ea4f-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2ea4f-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2ea4f-165">Abonelik anahtarı sorgu dizesi parametresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="2ea4f-166">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="2ea4f-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="2ea4f-167">-SubscriptionRequired</span></span>
<span data-ttu-id="2ea4f-168">API için istekler için aboneliğinizi zorunlu kılma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="2ea4f-169">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="2ea4f-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea4f-170">CommonParameters</span></span>
<span data-ttu-id="2ea4f-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea4f-172">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2ea4f-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea4f-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ea4f-173">INPUTS</span></span>

### <span data-ttu-id="2ea4f-174">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="2ea4f-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2ea4f-175">System. String</span><span class="sxs-lookup"><span data-stu-id="2ea4f-175">System.String</span></span>

### <span data-ttu-id="2ea4f-176">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="2ea4f-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="2ea4f-177">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="2ea4f-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="2ea4f-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2ea4f-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2ea4f-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ea4f-179">OUTPUTS</span></span>

### <span data-ttu-id="2ea4f-180">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="2ea4f-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2ea4f-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ea4f-181">NOTES</span></span>

## <span data-ttu-id="2ea4f-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ea4f-182">RELATED LINKS</span></span>

[<span data-ttu-id="2ea4f-183">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="2ea4f-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="2ea4f-184">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="2ea4f-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="2ea4f-185">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="2ea4f-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="2ea4f-186">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="2ea4f-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="2ea4f-187">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="2ea4f-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


