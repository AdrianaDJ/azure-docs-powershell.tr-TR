---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 973dc9bac629ee9a82b7624053f689bf7884fd8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753431"
---
# <span data-ttu-id="71a42-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="71a42-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="71a42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71a42-102">SYNOPSIS</span></span>
<span data-ttu-id="71a42-103">Bir API 'YI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="71a42-103">Modifies an API.</span></span>

## <span data-ttu-id="71a42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71a42-104">SYNTAX</span></span>

### <span data-ttu-id="71a42-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="71a42-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71a42-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="71a42-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71a42-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="71a42-107">DESCRIPTION</span></span>
<span data-ttu-id="71a42-108">**Set-Azapsananagementapı** cmdlet 'ı BIR Azure API yönetim API 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="71a42-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="71a42-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71a42-109">EXAMPLES</span></span>

### <span data-ttu-id="71a42-110">Örnek 1 API 'YI değiştirme</span><span class="sxs-lookup"><span data-stu-id="71a42-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="71a42-111">Örnek 2 var olan Apıversionset 'e API ekleme</span><span class="sxs-lookup"><span data-stu-id="71a42-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```
<span data-ttu-id="71a42-112">Bu örnek, var olan bir API sürüm kümesine API ekler</span><span class="sxs-lookup"><span data-stu-id="71a42-112">This example adds an API to an existing API Version Set</span></span>

## <span data-ttu-id="71a42-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71a42-113">PARAMETERS</span></span>

### <span data-ttu-id="71a42-114">-Apııd</span><span class="sxs-lookup"><span data-stu-id="71a42-114">-ApiId</span></span>
<span data-ttu-id="71a42-115">Değiştirilecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-115">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="71a42-116">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="71a42-116">-AuthorizationScope</span></span>
<span data-ttu-id="71a42-117">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-117">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="71a42-118">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="71a42-118">The default value is $Null.</span></span>

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

### <span data-ttu-id="71a42-119">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="71a42-119">-AuthorizationServerId</span></span>
<span data-ttu-id="71a42-120">OAuth yetkilendirme sunucusu tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-120">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="71a42-121">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="71a42-121">The default value is $Null.</span></span>
<span data-ttu-id="71a42-122">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="71a42-122">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="71a42-123">-Yataertokensendingmethod</span><span class="sxs-lookup"><span data-stu-id="71a42-123">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="71a42-124">API 'ya erişim belirtecinin geçirildiği OpenID yetkilendirme sunucusu mekanizması.</span><span class="sxs-lookup"><span data-stu-id="71a42-124">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="71a42-125">Bölümüne bakın http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="71a42-125">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="71a42-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="71a42-126">This parameter is optional.</span></span> <span data-ttu-id="71a42-127">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="71a42-127">Default value is $null.</span></span>

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

### <span data-ttu-id="71a42-128">-Context</span><span class="sxs-lookup"><span data-stu-id="71a42-128">-Context</span></span>
<span data-ttu-id="71a42-129">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-129">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="71a42-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a42-130">-DefaultProfile</span></span>
<span data-ttu-id="71a42-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71a42-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71a42-132">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="71a42-132">-Description</span></span>
<span data-ttu-id="71a42-133">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-133">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="71a42-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71a42-134">-InputObject</span></span>
<span data-ttu-id="71a42-135">PsApiManagementApi örneği.</span><span class="sxs-lookup"><span data-stu-id="71a42-135">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="71a42-136">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="71a42-136">This parameter is required.</span></span>

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

### <span data-ttu-id="71a42-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="71a42-137">-Name</span></span>
<span data-ttu-id="71a42-138">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-138">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="71a42-139">-Openıdproviderıd</span><span class="sxs-lookup"><span data-stu-id="71a42-139">-OpenIdProviderId</span></span>
<span data-ttu-id="71a42-140">OpenID yetkilendirme sunucusu tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="71a42-140">OpenId authorization server identifier.</span></span> <span data-ttu-id="71a42-141">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="71a42-141">This parameter is optional.</span></span> <span data-ttu-id="71a42-142">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="71a42-142">Default value is $null.</span></span> <span data-ttu-id="71a42-143">Yataertokensendingmethods belirtilmişse, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="71a42-143">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="71a42-144">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="71a42-144">-PassThru</span></span>
<span data-ttu-id="71a42-145">geçiş</span><span class="sxs-lookup"><span data-stu-id="71a42-145">passthru</span></span>

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

### <span data-ttu-id="71a42-146">-Yol</span><span class="sxs-lookup"><span data-stu-id="71a42-146">-Path</span></span>
<span data-ttu-id="71a42-147">API 'nin Genel URL 'sinin son bölümü olan Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-147">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="71a42-148">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="71a42-148">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="71a42-149">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="71a42-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="71a42-150">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="71a42-150">-Protocols</span></span>
<span data-ttu-id="71a42-151">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-151">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="71a42-152">http ve https psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="71a42-152">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="71a42-153">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="71a42-153">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="71a42-154">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="71a42-154">The default value is $Null.</span></span>

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

### <span data-ttu-id="71a42-155">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="71a42-155">-ServiceUrl</span></span>
<span data-ttu-id="71a42-156">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-156">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="71a42-157">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="71a42-157">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="71a42-158">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="71a42-158">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="71a42-159">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="71a42-159">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="71a42-160">Abonelik anahtarı üstbilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-160">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="71a42-161">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="71a42-161">The default value is $Null.</span></span>

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

### <span data-ttu-id="71a42-162">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="71a42-162">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="71a42-163">Abonelik anahtarı sorgu dizesi parametresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="71a42-163">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="71a42-164">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="71a42-164">The default value is $Null.</span></span>

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

### <span data-ttu-id="71a42-165">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="71a42-165">-SubscriptionRequired</span></span>
<span data-ttu-id="71a42-166">API için istekler için aboneliğinizi zorunlu kılma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="71a42-166">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="71a42-167">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="71a42-167">This parameter is optional.</span></span>

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

### <span data-ttu-id="71a42-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a42-168">CommonParameters</span></span>
<span data-ttu-id="71a42-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71a42-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a42-170">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="71a42-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a42-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71a42-171">INPUTS</span></span>

### <span data-ttu-id="71a42-172">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="71a42-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="71a42-173">System. String</span><span class="sxs-lookup"><span data-stu-id="71a42-173">System.String</span></span>

### <span data-ttu-id="71a42-174">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="71a42-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="71a42-175">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="71a42-175">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="71a42-176">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="71a42-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="71a42-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71a42-177">OUTPUTS</span></span>

### <span data-ttu-id="71a42-178">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="71a42-178">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="71a42-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71a42-179">NOTES</span></span>

## <span data-ttu-id="71a42-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71a42-180">RELATED LINKS</span></span>

[<span data-ttu-id="71a42-181">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="71a42-181">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="71a42-182">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="71a42-182">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="71a42-183">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="71a42-183">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="71a42-184">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="71a42-184">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="71a42-185">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="71a42-185">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


