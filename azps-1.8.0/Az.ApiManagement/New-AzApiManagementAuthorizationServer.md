---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: b09ea243dac2952cc4ec630755537a0e3cc5a745
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751123"
---
# <span data-ttu-id="05592-101">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="05592-101">New-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="05592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05592-102">SYNOPSIS</span></span>
<span data-ttu-id="05592-103">Yetkilendirme sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05592-103">Creates an authorization server.</span></span>

## <span data-ttu-id="05592-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05592-104">SYNTAX</span></span>

```
New-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>] -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05592-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05592-105">DESCRIPTION</span></span>
<span data-ttu-id="05592-106">**Yeni-Azapsananagementauthorizationserver** cmdlet 'ı BIR Azure API yönetim yetkilendirme sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05592-106">The **New-AzApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="05592-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05592-107">EXAMPLES</span></span>

### <span data-ttu-id="05592-108">Örnek 1: yetkilendirme sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="05592-108">Example 1: Create an authorization server</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="05592-109">Bu komut, yetkilendirme sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05592-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="05592-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05592-110">PARAMETERS</span></span>

### <span data-ttu-id="05592-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="05592-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="05592-112">Erişim belirteci göndermek için bir yöntem dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="05592-113">AuthorizationHeader ve Query psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="05592-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05592-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="05592-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="05592-115">Kaynak sahiplerinin kimliğini doğrulamak ve yetkilendirme onayları edinmek için yetkilendirme uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="05592-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="05592-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="05592-117">Yetkilendirme isteği yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="05592-118">Geçerli değerler: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="05592-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="05592-119">Varsayılan değer GET değeridir.</span><span class="sxs-lookup"><span data-stu-id="05592-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Get, Post, Head, Options, Trace, Put, Patch, Delete

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05592-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="05592-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="05592-121">İstemci kimlik doğrulama yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="05592-122">Temel ve gövde psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="05592-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05592-123">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="05592-123">-ClientId</span></span>
<span data-ttu-id="05592-124">Uygulama geliştiricisi konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="05592-125">-ClientRegistrationPageUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="05592-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="05592-126">İstemcileri yetkilendirme sunucusuyla kaydettirmek ve istemci kimlik bilgilerini almak için istemci kaydı uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="05592-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="05592-127">-ClientSecret</span></span>
<span data-ttu-id="05592-128">Geliştirici konsolunun istemci uygulaması olan istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-128">Specifies the client secret of developer console that is the client application.</span></span>

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

### <span data-ttu-id="05592-129">-Context</span><span class="sxs-lookup"><span data-stu-id="05592-129">-Context</span></span>
<span data-ttu-id="05592-130">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05592-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05592-131">-DefaultProfile</span></span>
<span data-ttu-id="05592-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05592-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05592-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="05592-133">-DefaultScope</span></span>
<span data-ttu-id="05592-134">Yetkilendirme sunucusunun varsayılan kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="05592-135">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="05592-135">-Description</span></span>
<span data-ttu-id="05592-136">Yetkilendirme sunucusu için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="05592-137">-Granttürler</span><span class="sxs-lookup"><span data-stu-id="05592-137">-GrantTypes</span></span>
<span data-ttu-id="05592-138">Bir atama türleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="05592-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="05592-139">psdx_paramvalues</span></span>
- <span data-ttu-id="05592-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="05592-140">AuthorizationCode</span></span>
- <span data-ttu-id="05592-141">Öğelerini</span><span class="sxs-lookup"><span data-stu-id="05592-141">ClientCredentials</span></span> 
- <span data-ttu-id="05592-142">İmlecin</span><span class="sxs-lookup"><span data-stu-id="05592-142">Implicit</span></span> 
- <span data-ttu-id="05592-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="05592-143">ResourceOwnerPassword</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases:
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05592-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="05592-144">-Name</span></span>
<span data-ttu-id="05592-145">Oluşturulacak yetkilendirme sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-145">Specifies the name of the authorization server to create.</span></span>

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

### <span data-ttu-id="05592-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="05592-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="05592-147">Kaynak sahibi parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="05592-148">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="05592-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="05592-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="05592-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="05592-150">Kaynak sahibi Kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="05592-151">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="05592-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="05592-152">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="05592-152">-ServerId</span></span>
<span data-ttu-id="05592-153">Oluşturulacak yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-153">Specifies the ID of the authorization server to create.</span></span>

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

### <span data-ttu-id="05592-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="05592-154">-SupportState</span></span>
<span data-ttu-id="05592-155">*Durum* parametresini destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="05592-155">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05592-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="05592-156">-TokenBodyParameters</span></span>
<span data-ttu-id="05592-157">**Application/x-www-form-urlencoded** format kullanarak ek gövde parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05592-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="05592-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="05592-159">Kimlik doğrulama veya yenileme belirteçleri için Exchange 'de erişim belirteçlerini edinmek amacıyla istemciler tarafından kullanılan belirteç uç noktası URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05592-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="05592-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05592-160">CommonParameters</span></span>
<span data-ttu-id="05592-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05592-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05592-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05592-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05592-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05592-163">INPUTS</span></span>

### <span data-ttu-id="05592-164">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="05592-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05592-165">System. String</span><span class="sxs-lookup"><span data-stu-id="05592-165">System.String</span></span>

### <span data-ttu-id="05592-166">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementauthorizationrequestmethod []</span><span class="sxs-lookup"><span data-stu-id="05592-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="05592-167">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgranttype []</span><span class="sxs-lookup"><span data-stu-id="05592-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="05592-168">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementclientauthenticationmethod []</span><span class="sxs-lookup"><span data-stu-id="05592-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="05592-169">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="05592-169">System.Collections.Hashtable</span></span>

### <span data-ttu-id="05592-170">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="05592-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="05592-171">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccesstokensendingmethod []</span><span class="sxs-lookup"><span data-stu-id="05592-171">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

## <span data-ttu-id="05592-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05592-172">OUTPUTS</span></span>

### <span data-ttu-id="05592-173">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="05592-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="05592-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05592-174">NOTES</span></span>

## <span data-ttu-id="05592-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05592-175">RELATED LINKS</span></span>