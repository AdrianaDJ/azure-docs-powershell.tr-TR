---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273744"
---
# <span data-ttu-id="05efc-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="05efc-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="05efc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05efc-102">SYNOPSIS</span></span>
<span data-ttu-id="05efc-103">API düzeltmesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="05efc-103">Modifies an API Revision</span></span>

## <span data-ttu-id="05efc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05efc-104">SYNTAX</span></span>

### <span data-ttu-id="05efc-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05efc-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05efc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05efc-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05efc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="05efc-107">DESCRIPTION</span></span>
<span data-ttu-id="05efc-108">**Set-Azapsananagementapirevision** cmdlet 'ı BIR Azure API yönetim API düzenlemesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="05efc-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="05efc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05efc-109">EXAMPLES</span></span>

### <span data-ttu-id="05efc-110">Örnek 1: API düzeltmesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="05efc-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="05efc-111">Cmdlet, `2` API 'nin düzeltmesini `echo-api` Yeni bir açıklama, protokol ve yol ile güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="05efc-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="05efc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05efc-112">PARAMETERS</span></span>

### <span data-ttu-id="05efc-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="05efc-113">-ApiId</span></span>
<span data-ttu-id="05efc-114">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="05efc-114">Identifier of existing API.</span></span>
<span data-ttu-id="05efc-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="05efc-115">This parameter is required.</span></span>

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

### <span data-ttu-id="05efc-116">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="05efc-116">-ApiRevision</span></span>
<span data-ttu-id="05efc-117">Var olan API düzeltmesine ait tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="05efc-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="05efc-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="05efc-118">This parameter is required.</span></span>

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

### <span data-ttu-id="05efc-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="05efc-119">-AuthorizationScope</span></span>
<span data-ttu-id="05efc-120">OAuth işlemleri kapsamı.</span><span class="sxs-lookup"><span data-stu-id="05efc-120">OAuth operations scope.</span></span>
<span data-ttu-id="05efc-121">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-121">This parameter is optional.</span></span>
<span data-ttu-id="05efc-122">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="05efc-122">Default value is $null.</span></span>

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

### <span data-ttu-id="05efc-123">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="05efc-123">-AuthorizationServerId</span></span>
<span data-ttu-id="05efc-124">OAuth yetkilendirme sunucusu tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="05efc-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="05efc-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-125">This parameter is optional.</span></span>
<span data-ttu-id="05efc-126">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="05efc-126">Default value is $null.</span></span>
<span data-ttu-id="05efc-127">, AuthorizationScope belirtilmişse belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="05efc-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="05efc-128">-Yataertokensendingmethod</span><span class="sxs-lookup"><span data-stu-id="05efc-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="05efc-129">API 'ya erişim belirtecinin geçirildiği OpenID yetkilendirme sunucusu mekanizması.</span><span class="sxs-lookup"><span data-stu-id="05efc-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="05efc-130">Bölümüne bakın http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="05efc-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="05efc-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-131">This parameter is optional.</span></span> <span data-ttu-id="05efc-132">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="05efc-132">Default value is $null.</span></span>

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

### <span data-ttu-id="05efc-133">-Context</span><span class="sxs-lookup"><span data-stu-id="05efc-133">-Context</span></span>
<span data-ttu-id="05efc-134">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="05efc-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="05efc-135">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="05efc-135">This parameter is required.</span></span>

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

### <span data-ttu-id="05efc-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05efc-136">-DefaultProfile</span></span>
<span data-ttu-id="05efc-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05efc-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05efc-138">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="05efc-138">-Description</span></span>
<span data-ttu-id="05efc-139">Web API açıklaması.</span><span class="sxs-lookup"><span data-stu-id="05efc-139">Web API description.</span></span>
<span data-ttu-id="05efc-140">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="05efc-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05efc-141">-InputObject</span></span>
<span data-ttu-id="05efc-142">PsApiManagementApi örneği.</span><span class="sxs-lookup"><span data-stu-id="05efc-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="05efc-143">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="05efc-143">This parameter is required.</span></span>

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

### <span data-ttu-id="05efc-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="05efc-144">-Name</span></span>
<span data-ttu-id="05efc-145">Web API adı.</span><span class="sxs-lookup"><span data-stu-id="05efc-145">Web API name.</span></span>
<span data-ttu-id="05efc-146">Geliştirici ve yönetici portalları 'nda görüneceği şekliyle API 'nin genel adı.</span><span class="sxs-lookup"><span data-stu-id="05efc-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="05efc-147">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="05efc-147">This parameter is required.</span></span>

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

### <span data-ttu-id="05efc-148">-Openıdproviderıd</span><span class="sxs-lookup"><span data-stu-id="05efc-148">-OpenIdProviderId</span></span>
<span data-ttu-id="05efc-149">OpenID yetkilendirme sunucusu tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="05efc-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="05efc-150">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-150">This parameter is optional.</span></span> <span data-ttu-id="05efc-151">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="05efc-151">Default value is $null.</span></span> <span data-ttu-id="05efc-152">Yataertokensendingmethods belirtilmişse, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="05efc-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="05efc-153">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="05efc-153">-PassThru</span></span>
<span data-ttu-id="05efc-154">Eğer belirtilmişse, ayarlanmış API 'yi temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapimanagementapı türü.</span><span class="sxs-lookup"><span data-stu-id="05efc-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="05efc-155">-Yol</span><span class="sxs-lookup"><span data-stu-id="05efc-155">-Path</span></span>
<span data-ttu-id="05efc-156">Web API yolu.</span><span class="sxs-lookup"><span data-stu-id="05efc-156">Web API Path.</span></span>
<span data-ttu-id="05efc-157">API 'nin Genel URL 'sinin son bölümü.</span><span class="sxs-lookup"><span data-stu-id="05efc-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="05efc-158">Bu URL, Web hizmetine istek göndermek için API tüketicileri tarafından kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="05efc-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="05efc-159">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="05efc-160">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-160">This parameter is optional.</span></span>
<span data-ttu-id="05efc-161">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="05efc-161">Default value is $null.</span></span>

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

### <span data-ttu-id="05efc-162">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="05efc-162">-Protocols</span></span>
<span data-ttu-id="05efc-163">Web API protokolleri (http, https).</span><span class="sxs-lookup"><span data-stu-id="05efc-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="05efc-164">API 'nın kullanılabileceği iletişim kuralları.</span><span class="sxs-lookup"><span data-stu-id="05efc-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="05efc-165">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="05efc-165">This parameter is required.</span></span>
<span data-ttu-id="05efc-166">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="05efc-166">Default value is $null.</span></span>

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

### <span data-ttu-id="05efc-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="05efc-167">-ServiceUrl</span></span>
<span data-ttu-id="05efc-168">API 'yi kullanan Web hizmetinin URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="05efc-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="05efc-169">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="05efc-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="05efc-170">1-2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="05efc-171">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="05efc-171">This parameter is required.</span></span>

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

### <span data-ttu-id="05efc-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="05efc-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="05efc-173">Abonelik anahtarı üstbilgi adı.</span><span class="sxs-lookup"><span data-stu-id="05efc-173">Subscription key header name.</span></span>
<span data-ttu-id="05efc-174">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-174">This parameter is optional.</span></span>
<span data-ttu-id="05efc-175">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="05efc-175">Default value is $null.</span></span>

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

### <span data-ttu-id="05efc-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="05efc-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="05efc-177">Abonelik anahtarı sorgu dizesi parametre adı.</span><span class="sxs-lookup"><span data-stu-id="05efc-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="05efc-178">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-178">This parameter is optional.</span></span>
<span data-ttu-id="05efc-179">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="05efc-179">Default value is $null.</span></span>

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

### <span data-ttu-id="05efc-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="05efc-180">-SubscriptionRequired</span></span>
<span data-ttu-id="05efc-181">API için istekler için aboneliğinizi zorunlu kılma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="05efc-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="05efc-182">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="05efc-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="05efc-183">-Onay</span><span class="sxs-lookup"><span data-stu-id="05efc-183">-Confirm</span></span>
<span data-ttu-id="05efc-184">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05efc-184">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05efc-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05efc-185">-WhatIf</span></span>
<span data-ttu-id="05efc-186">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05efc-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05efc-187">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05efc-187">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05efc-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05efc-188">CommonParameters</span></span>
<span data-ttu-id="05efc-189">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05efc-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05efc-190">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="05efc-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05efc-191">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05efc-191">INPUTS</span></span>

### <span data-ttu-id="05efc-192">System. String</span><span class="sxs-lookup"><span data-stu-id="05efc-192">System.String</span></span>

### <span data-ttu-id="05efc-193">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="05efc-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05efc-194">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="05efc-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="05efc-195">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="05efc-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="05efc-196">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="05efc-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05efc-197">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05efc-197">OUTPUTS</span></span>

### <span data-ttu-id="05efc-198">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="05efc-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="05efc-199">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05efc-199">NOTES</span></span>

## <span data-ttu-id="05efc-200">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05efc-200">RELATED LINKS</span></span>

[<span data-ttu-id="05efc-201">Get-Azapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="05efc-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="05efc-202">Yeni-Azapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="05efc-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="05efc-203">Remove-Azapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="05efc-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)