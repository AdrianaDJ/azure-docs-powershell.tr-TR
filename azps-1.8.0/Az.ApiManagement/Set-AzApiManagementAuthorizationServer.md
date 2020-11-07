---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 88e7c1304aae987dbf7315d5ed474969af12ba08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917704"
---
# <span data-ttu-id="f23da-101">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="f23da-101">Set-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="f23da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f23da-102">SYNOPSIS</span></span>
<span data-ttu-id="f23da-103">Yetkilendirme sunucusunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f23da-103">Modifies an authorization server.</span></span>

## <span data-ttu-id="f23da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f23da-104">SYNTAX</span></span>

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

## <span data-ttu-id="f23da-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f23da-105">DESCRIPTION</span></span>
<span data-ttu-id="f23da-106">**Set-Azapsananagementauthorizationserver** cmdlet 'ı Azure API yönetim yetkilendirme sunucusu ayrıntılarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f23da-106">The **Set-AzApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="f23da-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f23da-107">EXAMPLES</span></span>

### <span data-ttu-id="f23da-108">Örnek 1: yetkilendirme sunucusunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="f23da-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="f23da-109">Bu komut belirtilen API yönetim yetkilendirme sunucusunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f23da-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="f23da-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f23da-110">PARAMETERS</span></span>

### <span data-ttu-id="f23da-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="f23da-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="f23da-112">Erişim belirteci göndermek için bir yöntem dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="f23da-113">AuthorizationHeader ve Query psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="f23da-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="f23da-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="f23da-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="f23da-115">Kaynak sahiplerinin kimliğini doğrulamak ve yetkilendirme onayları edinmek için yetkilendirme uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="f23da-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="f23da-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="f23da-117">Yetkilendirme isteği yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="f23da-118">Al ve postala psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="f23da-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="f23da-119">Varsayılan değer GET değeridir.</span><span class="sxs-lookup"><span data-stu-id="f23da-119">The default value is GET.</span></span>

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

### <span data-ttu-id="f23da-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="f23da-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="f23da-121">İstemci kimlik doğrulama yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="f23da-122">Temel ve gövde psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="f23da-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="f23da-123">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="f23da-123">-ClientId</span></span>
<span data-ttu-id="f23da-124">Uygulama geliştiricisi konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="f23da-125">-ClientRegistrationPageUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="f23da-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="f23da-126">İstemcileri yetkilendirme sunucusuyla kaydettirmek ve istemci kimlik bilgilerini almak için istemci kaydı uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="f23da-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f23da-127">-ClientSecret</span></span>
<span data-ttu-id="f23da-128">İstemci uygulaması olan geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="f23da-129">-Context</span><span class="sxs-lookup"><span data-stu-id="f23da-129">-Context</span></span>
<span data-ttu-id="f23da-130">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f23da-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23da-131">-DefaultProfile</span></span>
<span data-ttu-id="f23da-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f23da-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f23da-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="f23da-133">-DefaultScope</span></span>
<span data-ttu-id="f23da-134">Yetkilendirme sunucusunun varsayılan kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-134">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="f23da-135">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="f23da-135">-Description</span></span>
<span data-ttu-id="f23da-136">Yetkilendirme sunucusu için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-136">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="f23da-137">-Granttürler</span><span class="sxs-lookup"><span data-stu-id="f23da-137">-GrantTypes</span></span>
<span data-ttu-id="f23da-138">Bir atama türleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="f23da-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="f23da-139">psdx_paramvalues</span></span>
- <span data-ttu-id="f23da-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="f23da-140">AuthorizationCode</span></span>
- <span data-ttu-id="f23da-141">Öğelerini</span><span class="sxs-lookup"><span data-stu-id="f23da-141">ClientCredentials</span></span> 
- <span data-ttu-id="f23da-142">İmlecin</span><span class="sxs-lookup"><span data-stu-id="f23da-142">Implicit</span></span> 
- <span data-ttu-id="f23da-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="f23da-143">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="f23da-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="f23da-144">-Name</span></span>
<span data-ttu-id="f23da-145">Değiştirilecek yetkilendirme sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-145">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="f23da-146">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f23da-146">-PassThru</span></span>
<span data-ttu-id="f23da-147">geçiş</span><span class="sxs-lookup"><span data-stu-id="f23da-147">passthru</span></span>

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

### <span data-ttu-id="f23da-148">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="f23da-148">-ResourceOwnerPassword</span></span>
<span data-ttu-id="f23da-149">Kaynak sahibi parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-149">Specifies the resource owner password.</span></span>
<span data-ttu-id="f23da-150">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f23da-150">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="f23da-151">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="f23da-151">-ResourceOwnerUsername</span></span>
<span data-ttu-id="f23da-152">Kaynak sahibi Kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-152">Specifies the resource owner user name.</span></span>
<span data-ttu-id="f23da-153">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f23da-153">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="f23da-154">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="f23da-154">-ServerId</span></span>
<span data-ttu-id="f23da-155">Değiştirilecek yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-155">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="f23da-156">-SupportState</span><span class="sxs-lookup"><span data-stu-id="f23da-156">-SupportState</span></span>
<span data-ttu-id="f23da-157">*Durum* parametresini destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f23da-157">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="f23da-158">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="f23da-158">-TokenBodyParameters</span></span>
<span data-ttu-id="f23da-159">Application/x-www-form-urlencoded format kullanarak ek gövde parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-159">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="f23da-160">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="f23da-160">-TokenEndpointUrl</span></span>
<span data-ttu-id="f23da-161">İstemcilerin yetkilendirmeyi sunmak için Exchange 'de erişim belirteçlerini edinmeleri için belirteç uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23da-161">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="f23da-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23da-162">CommonParameters</span></span>
<span data-ttu-id="f23da-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f23da-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23da-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23da-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23da-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f23da-165">INPUTS</span></span>

### <span data-ttu-id="f23da-166">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f23da-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f23da-167">System. String</span><span class="sxs-lookup"><span data-stu-id="f23da-167">System.String</span></span>

### <span data-ttu-id="f23da-168">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementauthorizationrequestmethod []</span><span class="sxs-lookup"><span data-stu-id="f23da-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]</span></span>

### <span data-ttu-id="f23da-169">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementgranttype []</span><span class="sxs-lookup"><span data-stu-id="f23da-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGrantType[]</span></span>

### <span data-ttu-id="f23da-170">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementclientauthenticationmethod []</span><span class="sxs-lookup"><span data-stu-id="f23da-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientAuthenticationMethod[]</span></span>

### <span data-ttu-id="f23da-171">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f23da-171">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f23da-172">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="f23da-172">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f23da-173">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementaccesstokensendingmethod []</span><span class="sxs-lookup"><span data-stu-id="f23da-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessTokenSendingMethod[]</span></span>

### <span data-ttu-id="f23da-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f23da-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f23da-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f23da-175">OUTPUTS</span></span>

### <span data-ttu-id="f23da-176">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="f23da-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="f23da-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f23da-177">NOTES</span></span>

## <span data-ttu-id="f23da-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f23da-178">RELATED LINKS</span></span>

[<span data-ttu-id="f23da-179">Get-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="f23da-179">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="f23da-180">Yeni-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="f23da-180">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="f23da-181">Remove-Azapsananagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="f23da-181">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)


