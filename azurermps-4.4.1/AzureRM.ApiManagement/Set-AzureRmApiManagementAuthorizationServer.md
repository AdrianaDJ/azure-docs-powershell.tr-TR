---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 93005775-3AB9-43C5-B353-45B82124ADB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: ed7043746aa5ce59e733737acf8da61bdb44b0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764281"
---
# <span data-ttu-id="e6b91-101">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="e6b91-101">Set-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="e6b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6b91-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b91-103">Yetkilendirme sunucusunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-103">Modifies an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6b91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6b91-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> -Name <String>
 [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b91-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6b91-105">DESCRIPTION</span></span>
<span data-ttu-id="e6b91-106">**Set-Azurermapımanagementauthorizationserver** cmdlet 'ı Azure API yönetim yetkilendirme sunucusu ayrıntılarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-106">The **Set-AzureRmApiManagementAuthorizationServer** cmdlet modifies Azure API Management authorization server details.</span></span>

## <span data-ttu-id="e6b91-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6b91-107">EXAMPLES</span></span>

### <span data-ttu-id="e6b91-108">Örnek 1: yetkilendirme sunucusunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="e6b91-108">Example 1: Modify an authorization server</span></span>
```
PS C:\>Set-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -ServerId 0123456789 -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signupv2" -AuthorizationEndpointUrl "https://contoso/authv2" -TokenEndpointUrl "https://contoso/tokenv2" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'} -AccessTokenSendingMethods @('AuthorizationHeader')
```

<span data-ttu-id="e6b91-109">Bu komut belirtilen API yönetim yetkilendirme sunucusunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-109">This command modifies the specified API Management authorization server.</span></span>

## <span data-ttu-id="e6b91-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6b91-110">PARAMETERS</span></span>

### <span data-ttu-id="e6b91-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="e6b91-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="e6b91-112">Erişim belirteci göndermek için bir yöntem dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="e6b91-113">AuthorizationHeader ve Query psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="e6b91-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

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

### <span data-ttu-id="e6b91-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="e6b91-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="e6b91-115">Kaynak sahiplerinin kimliğini doğrulamak ve yetkilendirme onayları edinmek için yetkilendirme uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

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

### <span data-ttu-id="e6b91-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="e6b91-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="e6b91-117">Yetkilendirme isteği yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="e6b91-118">Al ve postala psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="e6b91-118">psdx_paramvalues GET and POST.</span></span>
<span data-ttu-id="e6b91-119">Varsayılan değer GET değeridir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-119">The default value is GET.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b91-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="e6b91-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="e6b91-121">İstemci kimlik doğrulama yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="e6b91-122">Temel ve gövde psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="e6b91-122">psdx_paramvalues Basic and Body.</span></span>

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

### <span data-ttu-id="e6b91-123">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="e6b91-123">-ClientId</span></span>
<span data-ttu-id="e6b91-124">Uygulama geliştiricisi konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-124">Specifies the client ID of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="e6b91-125">-ClientRegistrationPageUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="e6b91-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="e6b91-126">İstemcileri yetkilendirme sunucusuyla kaydettirmek ve istemci kimlik bilgilerini almak için istemci kaydı uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

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

### <span data-ttu-id="e6b91-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="e6b91-127">-ClientSecret</span></span>
<span data-ttu-id="e6b91-128">İstemci uygulaması olan geliştirici konsolunun istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-128">Specifies the client secret of the developer console that is the client application.</span></span>

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

### <span data-ttu-id="e6b91-129">-Context</span><span class="sxs-lookup"><span data-stu-id="e6b91-129">-Context</span></span>
<span data-ttu-id="e6b91-130">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e6b91-131">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="e6b91-131">-DefaultScope</span></span>
<span data-ttu-id="e6b91-132">Yetkilendirme sunucusunun varsayılan kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-132">Specifies the default scope for the authorization server.</span></span>

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

### <span data-ttu-id="e6b91-133">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e6b91-133">-Description</span></span>
<span data-ttu-id="e6b91-134">Yetkilendirme sunucusu için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-134">Specifies a description for an authorization server.</span></span>

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

### <span data-ttu-id="e6b91-135">-Granttürler</span><span class="sxs-lookup"><span data-stu-id="e6b91-135">-GrantTypes</span></span>
<span data-ttu-id="e6b91-136">Bir atama türleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-136">Specifies an array of grant types.</span></span>
<span data-ttu-id="e6b91-137">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="e6b91-137">psdx_paramvalues</span></span>

- <span data-ttu-id="e6b91-138">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="e6b91-138">AuthorizationCode</span></span>
- <span data-ttu-id="e6b91-139">Öğelerini</span><span class="sxs-lookup"><span data-stu-id="e6b91-139">ClientCredentials</span></span> 
- <span data-ttu-id="e6b91-140">İmlecin</span><span class="sxs-lookup"><span data-stu-id="e6b91-140">Implicit</span></span> 
- <span data-ttu-id="e6b91-141">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="e6b91-141">ResourceOwnerPassword</span></span>

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

### <span data-ttu-id="e6b91-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6b91-142">-Name</span></span>
<span data-ttu-id="e6b91-143">Değiştirilecek yetkilendirme sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-143">Specifies the name of the authorization server to modify.</span></span>

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

### <span data-ttu-id="e6b91-144">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e6b91-144">-PassThru</span></span>
<span data-ttu-id="e6b91-145">geçiş</span><span class="sxs-lookup"><span data-stu-id="e6b91-145">passthru</span></span>

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

### <span data-ttu-id="e6b91-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="e6b91-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="e6b91-147">Kaynak sahibi parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="e6b91-148">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-148">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="e6b91-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="e6b91-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="e6b91-150">Kaynak sahibi Kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="e6b91-151">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

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

### <span data-ttu-id="e6b91-152">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="e6b91-152">-ServerId</span></span>
<span data-ttu-id="e6b91-153">Değiştirilecek yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-153">Specifies the ID of the authorization server to modify.</span></span>

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

### <span data-ttu-id="e6b91-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="e6b91-154">-SupportState</span></span>
<span data-ttu-id="e6b91-155">*Durum* parametresini destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-155">Indicates whether to support the *State* parameter.</span></span>

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

### <span data-ttu-id="e6b91-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="e6b91-156">-TokenBodyParameters</span></span>
<span data-ttu-id="e6b91-157">Application/x-www-form-urlencoded format kullanarak ek gövde parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-157">Specifies additional body parameters using application/x-www-form-urlencoded format.</span></span>

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

### <span data-ttu-id="e6b91-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="e6b91-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="e6b91-159">İstemcilerin yetkilendirmeyi sunmak için Exchange 'de erişim belirteçlerini edinmeleri için belirteç uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6b91-159">Specifies the token endpoint for clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

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

### <span data-ttu-id="e6b91-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b91-160">-DefaultProfile</span></span>
<span data-ttu-id="e6b91-161">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6b91-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b91-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b91-162">CommonParameters</span></span>
<span data-ttu-id="e6b91-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6b91-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b91-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6b91-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b91-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6b91-165">INPUTS</span></span>

## <span data-ttu-id="e6b91-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6b91-166">OUTPUTS</span></span>

### <span data-ttu-id="e6b91-167">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="e6b91-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="e6b91-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6b91-168">NOTES</span></span>

## <span data-ttu-id="e6b91-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6b91-169">RELATED LINKS</span></span>

[<span data-ttu-id="e6b91-170">Get-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="e6b91-170">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="e6b91-171">Yeni-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="e6b91-171">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="e6b91-172">Remove-Azurermapımanagementauthorizationserver</span><span class="sxs-lookup"><span data-stu-id="e6b91-172">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)


