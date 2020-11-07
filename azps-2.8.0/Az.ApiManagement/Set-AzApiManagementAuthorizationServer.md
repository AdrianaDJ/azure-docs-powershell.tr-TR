---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 696db55822242e124f006be233a9c8a8605a360d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753424"
---
# <span data-ttu-id="36f48-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="36f48-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="36f48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f48-102">SYNOPSIS</span></span>
<span data-ttu-id="36f48-103">Yetkilendirme sunucusunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="36f48-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="36f48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36f48-104">SYNTAX</span></span>

```
Set-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36f48-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="36f48-105">DESCRIPTION</span></span>
<span data-ttu-id="36f48-106">**Set-Azapsananagementauthorizationserver** cmdlet 'ı Azure API yönetim yetkilendirme sunucusu ayrıntılarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="36f48-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="36f48-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36f48-107">EXAMPLES</span></span>

### <span data-ttu-id="36f48-108">Örnek 1: yetkilendirme sunucusunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="36f48-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="36f48-109">Bu komut belirtilen API yönetim yetkilendirme sunucusunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="36f48-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="36f48-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36f48-110">PARAMETERS</span></span>

### <span data-ttu-id="36f48-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="36f48-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="36f48-112">Erişim belirteci göndermek için bir yöntem dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="36f48-113">AuthorizationHeader ve Query psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="36f48-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="36f48-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="36f48-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="36f48-115">Kaynak sahiplerinin kimliğini doğrulamak ve yetkilendirme onayları edinmek için yetkilendirme uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="36f48-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="36f48-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="36f48-117">Yetkilendirme isteği yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="36f48-118">Al ve postala psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="36f48-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="36f48-119">Varsayılan değer GET değeridir.</span><span class="sxs-lookup"><span data-stu-id="36f48-119">The default value is GET.</span></span>

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

### <span data-ttu-id="36f48-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="36f48-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="36f48-121">İstemci kimlik doğrulama yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="36f48-122">Temel ve gövde psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="36f48-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="36f48-123">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="36f48-123">-ClientId</span></span>
<span data-ttu-id="36f48-124">Uygulama geliştiricisi konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="36f48-125">-ClientRegistrationPageUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="36f48-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="36f48-126">İstemcileri yetkilendirme sunucusuyla kaydettirmek ve istemci kimlik bilgilerini almak için istemci kaydı uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="36f48-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="36f48-127">-ClientSecret</span></span>
<span data-ttu-id="36f48-128">İstemci uygulaması olan geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="36f48-129">-Context</span><span class="sxs-lookup"><span data-stu-id="36f48-129">-Context</span></span>
<span data-ttu-id="36f48-130">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="36f48-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f48-131">-DefaultProfile</span></span>
<span data-ttu-id="36f48-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36f48-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36f48-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="36f48-133">-DefaultScope</span></span>
<span data-ttu-id="36f48-134">Yetkilendirme sunucusunun varsayılan kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="36f48-135">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="36f48-135">-Description</span></span>
<span data-ttu-id="36f48-136">Yetkilendirme sunucusu için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="36f48-137">-Granttürler</span><span class="sxs-lookup"><span data-stu-id="36f48-137">-GrantTypes</span></span>
<span data-ttu-id="36f48-138">Bir atama türleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="36f48-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="36f48-139">psdx_paramvalues</span></span>
- <span data-ttu-id="36f48-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="36f48-140">AuthorizationCode</span></span>
- <span data-ttu-id="36f48-141">Öğelerini</span><span class="sxs-lookup"><span data-stu-id="36f48-141">ClientCredentials</span></span> 
- <span data-ttu-id="36f48-142">İmlecin</span><span class="sxs-lookup"><span data-stu-id="36f48-142">Implicit</span></span> 
- <span data-ttu-id="36f48-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="36f48-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="36f48-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="36f48-144">-Name</span></span>
<span data-ttu-id="36f48-145">Değiştirilecek yetkilendirme sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="36f48-146">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="36f48-146">-PassThru</span></span>
<span data-ttu-id="36f48-147">geçiş</span><span class="sxs-lookup"><span data-stu-id="36f48-147">passthru</span></span>

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

### <span data-ttu-id="36f48-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="36f48-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="36f48-149">Kaynak sahibi parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="36f48-150">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36f48-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="36f48-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="36f48-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="36f48-152">Kaynak sahibi Kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="36f48-153">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="36f48-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="36f48-154">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="36f48-154">-ServerId</span></span>
<span data-ttu-id="36f48-155">Değiştirilecek yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="36f48-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="36f48-156">-SupportState</span></span>
<span data-ttu-id="36f48-157">*Durum* parametresini destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="36f48-157">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="36f48-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="36f48-158">-TokenBodyParameters</span></span>
<span data-ttu-id="36f48-159">Application/x-www-form-urlencoded format kullanarak ek gövde parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="36f48-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="36f48-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="36f48-161">İstemcilerin yetkilendirmeyi sunmak için Exchange 'de erişim belirteçlerini edinmeleri için belirteç uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f48-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="36f48-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f48-162">CommonParameters</span></span>
<span data-ttu-id="36f48-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36f48-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f48-164">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="36f48-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f48-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36f48-165">INPUTS</span></span>

### <span data-ttu-id="36f48-166">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="36f48-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36f48-167">System. String</span><span class="sxs-lookup"><span data-stu-id="36f48-167">System.String</span></span>

### <span data-ttu-id="36f48-168">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementauthorizationrequestmethod []</span><span class="sxs-lookup"><span data-stu-id="36f48-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="36f48-169">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgranttype []</span><span class="sxs-lookup"><span data-stu-id="36f48-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="36f48-170">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementclientauthenticationmethod []</span><span class="sxs-lookup"><span data-stu-id="36f48-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="36f48-171">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="36f48-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="36f48-172">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="36f48-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="36f48-173">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccesstokensendingmethod []</span><span class="sxs-lookup"><span data-stu-id="36f48-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="36f48-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36f48-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36f48-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36f48-175">OUTPUTS</span></span>

### <span data-ttu-id="36f48-176">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="36f48-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="36f48-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36f48-177">NOTES</span></span>

## <span data-ttu-id="36f48-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36f48-178">RELATED LINKS</span></span>

[<span data-ttu-id="36f48-179">Get-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="36f48-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="36f48-180">Yeni-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="36f48-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="36f48-181">Remove-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="36f48-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

