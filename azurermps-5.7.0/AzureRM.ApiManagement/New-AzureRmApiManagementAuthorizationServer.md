---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 45B96AB0-ACE3-4754-B162-88027AC8CA41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: f1853c8f9e1e8449d0b607cadede215ec42b8952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762552"
---
# <span data-ttu-id="3ef1e-101">New-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="3ef1e-101">New-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="3ef1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ef1e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef1e-103">Yetkilendirme sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-103">Creates an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ef1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ef1e-104">SYNTAX</span></span>

```
New-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 -Name <String> [-Description <String>] -ClientRegistrationPageUrl <String> -AuthorizationEndpointUrl <String>
 -TokenEndpointUrl <String> -ClientId <String> [-ClientSecret <String>]
 [-AuthorizationRequestMethods <PsApiManagementAuthorizationRequestMethod[]>]
 -GrantTypes <PsApiManagementGrantType[]>
 -ClientAuthenticationMethods <PsApiManagementClientAuthenticationMethod[]> [-TokenBodyParameters <Hashtable>]
 [-SupportState <Boolean>] [-DefaultScope <String>]
 -AccessTokenSendingMethods <PsApiManagementAccessTokenSendingMethod[]> [-ResourceOwnerUsername <String>]
 [-ResourceOwnerPassword <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ef1e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ef1e-105">DESCRIPTION</span></span>
<span data-ttu-id="3ef1e-106">**Yeni-Azurermapımanagementauthorizationserver** cmdlet 'ı BIR Azure API yönetim yetkilendirme sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-106">The **New-AzureRmApiManagementAuthorizationServer** cmdlet creates an Azure API Management authorization server.</span></span>

## <span data-ttu-id="3ef1e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ef1e-107">EXAMPLES</span></span>

### <span data-ttu-id="3ef1e-108">Örnek 1: yetkilendirme sunucusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="3ef1e-108">Example 1: Create an authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext -Name "Contoso OAuth2 server" -ClientRegistrationPageUrl "https://contoso/signup" -AuthorizationEndpointUrl "https://contoso/auth" -TokenEndpointUrl "https://contoso/token" -ClientId "clientid" -ClientSecret "e041ed1b660b4eadbad5a29d066e6e88" -AuthorizationRequestMethods @('Get', 'Post') -GrantTypes @( 'AuthorizationCode', 'Implicit', 'ResourceOwnerPassword', 'ClientCredentials') -ClientAuthenticationMethods @('Basic') -TokenBodyParameters @{'par1'='val1'; 'par2'='val2'} -AccessTokenSendingMethods @('AuthorizationHeader', 'Query') -ResourceOwnerUsername "ivan" -ResourceOwnerPassword "qwerty"
```

<span data-ttu-id="3ef1e-109">Bu komut, yetkilendirme sunucusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-109">This command creates an authorization server.</span></span>

## <span data-ttu-id="3ef1e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ef1e-110">PARAMETERS</span></span>

### <span data-ttu-id="3ef1e-111">-AccessTokenSendingMethods</span><span class="sxs-lookup"><span data-stu-id="3ef1e-111">-AccessTokenSendingMethods</span></span>
<span data-ttu-id="3ef1e-112">Erişim belirteci göndermek için bir yöntem dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-112">Specifies an array of methods to send an access token.</span></span>
<span data-ttu-id="3ef1e-113">AuthorizationHeader ve Query psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-113">psdx_paramvalues AuthorizationHeader and Query.</span></span>

```yaml
Type: PsApiManagementAccessTokenSendingMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationHeader, Query

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-114">-AuthorizationEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="3ef1e-114">-AuthorizationEndpointUrl</span></span>
<span data-ttu-id="3ef1e-115">Kaynak sahiplerinin kimliğini doğrulamak ve yetkilendirme onayları edinmek için yetkilendirme uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-115">Specifies the authorization endpoint to authenticate resource owners and obtain authorization grants.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-116">-AuthorizationRequestMethods</span><span class="sxs-lookup"><span data-stu-id="3ef1e-116">-AuthorizationRequestMethods</span></span>
<span data-ttu-id="3ef1e-117">Yetkilendirme isteği yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-117">Specifies an array of authorization request methods.</span></span>
<span data-ttu-id="3ef1e-118">Geçerli değerler: GET, POST.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-118">Valid values are: GET, POST.</span></span>
<span data-ttu-id="3ef1e-119">Varsayılan değer GET değeridir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-119">The default value is GET.</span></span>

```yaml
Type: PsApiManagementAuthorizationRequestMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Get, Post

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-120">-ClientAuthenticationMethods</span><span class="sxs-lookup"><span data-stu-id="3ef1e-120">-ClientAuthenticationMethods</span></span>
<span data-ttu-id="3ef1e-121">İstemci kimlik doğrulama yöntemleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-121">Specifies an array of client authentication methods.</span></span>
<span data-ttu-id="3ef1e-122">Temel ve gövde psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-122">psdx_paramvalues Basic and Body.</span></span>

```yaml
Type: PsApiManagementClientAuthenticationMethod[]
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Body

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-123">-Clitıd</span><span class="sxs-lookup"><span data-stu-id="3ef1e-123">-ClientId</span></span>
<span data-ttu-id="3ef1e-124">Uygulama geliştiricisi konsolunun istemci KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-124">Specifies the client ID of the developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-125">-ClientRegistrationPageUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="3ef1e-125">-ClientRegistrationPageUrl</span></span>
<span data-ttu-id="3ef1e-126">İstemcileri yetkilendirme sunucusuyla kaydettirmek ve istemci kimlik bilgilerini almak için istemci kaydı uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-126">Specifies the client registration endpoint to register clients with the authorization server and obtain client credentials.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-127">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="3ef1e-127">-ClientSecret</span></span>
<span data-ttu-id="3ef1e-128">Geliştirici konsolunun istemci uygulaması olan istemci gizliliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-128">Specifies the client secret of developer console that is the client application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-129">-Context</span><span class="sxs-lookup"><span data-stu-id="3ef1e-129">-Context</span></span>
<span data-ttu-id="3ef1e-130">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef1e-131">-DefaultProfile</span></span>
<span data-ttu-id="3ef1e-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-133">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="3ef1e-133">-DefaultScope</span></span>
<span data-ttu-id="3ef1e-134">Yetkilendirme sunucusunun varsayılan kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-134">Specifies the default scope for the authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-135">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="3ef1e-135">-Description</span></span>
<span data-ttu-id="3ef1e-136">Yetkilendirme sunucusu için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-136">Specifies a description for an authorization server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-137">-Granttürler</span><span class="sxs-lookup"><span data-stu-id="3ef1e-137">-GrantTypes</span></span>
<span data-ttu-id="3ef1e-138">Bir atama türleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-138">Specifies an array of grant types.</span></span>
<span data-ttu-id="3ef1e-139">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="3ef1e-139">psdx_paramvalues</span></span>

- <span data-ttu-id="3ef1e-140">AuthorizationCode</span><span class="sxs-lookup"><span data-stu-id="3ef1e-140">AuthorizationCode</span></span>
- <span data-ttu-id="3ef1e-141">Öğelerini</span><span class="sxs-lookup"><span data-stu-id="3ef1e-141">ClientCredentials</span></span> 
- <span data-ttu-id="3ef1e-142">İmlecin</span><span class="sxs-lookup"><span data-stu-id="3ef1e-142">Implicit</span></span> 
- <span data-ttu-id="3ef1e-143">ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="3ef1e-143">ResourceOwnerPassword</span></span>

```yaml
Type: PsApiManagementGrantType[]
Parameter Sets: (All)
Aliases: 
Accepted values: AuthorizationCode, Implicit, ResourceOwnerPassword, ClientCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ef1e-144">-Name</span></span>
<span data-ttu-id="3ef1e-145">Oluşturulacak yetkilendirme sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-145">Specifies the name of the authorization server to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-146">-ResourceOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="3ef1e-146">-ResourceOwnerPassword</span></span>
<span data-ttu-id="3ef1e-147">Kaynak sahibi parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-147">Specifies the resource owner password.</span></span>
<span data-ttu-id="3ef1e-148">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse, bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-148">You must specify this parameter is required if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-149">-ResourceOwnerUsername</span><span class="sxs-lookup"><span data-stu-id="3ef1e-149">-ResourceOwnerUsername</span></span>
<span data-ttu-id="3ef1e-150">Kaynak sahibi Kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-150">Specifies the resource owner user name.</span></span>
<span data-ttu-id="3ef1e-151">ResourceOwnerPassword, *GrantTypes* parametresiyle belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-151">You must specify this parameter if ResourceOwnerPassword is specified by the *GrantTypes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-152">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="3ef1e-152">-ServerId</span></span>
<span data-ttu-id="3ef1e-153">Oluşturulacak yetkilendirme sunucusunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-153">Specifies the ID of the authorization server to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-154">-SupportState</span><span class="sxs-lookup"><span data-stu-id="3ef1e-154">-SupportState</span></span>
<span data-ttu-id="3ef1e-155">*Durum* parametresini destekleyip desteklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-155">Indicates whether to support the *State* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-156">-TokenBodyParameters</span><span class="sxs-lookup"><span data-stu-id="3ef1e-156">-TokenBodyParameters</span></span>
<span data-ttu-id="3ef1e-157">**Application/x-www-form-urlencoded** format kullanarak ek gövde parametrelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-157">Specifies additional body parameters using **application/x-www-form-urlencoded** format.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-158">-TokenEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="3ef1e-158">-TokenEndpointUrl</span></span>
<span data-ttu-id="3ef1e-159">Kimlik doğrulama veya yenileme belirteçleri için Exchange 'de erişim belirteçlerini edinmek amacıyla istemciler tarafından kullanılan belirteç uç noktası URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-159">Specifies the token endpoint URL that is used by clients to obtain access tokens in exchange for presenting authorization grants or refresh tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef1e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef1e-160">CommonParameters</span></span>
<span data-ttu-id="3ef1e-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef1e-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ef1e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef1e-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ef1e-163">INPUTS</span></span>

### <span data-ttu-id="3ef1e-164">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3ef1e-164">None</span></span>
<span data-ttu-id="3ef1e-165">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3ef1e-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ef1e-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ef1e-166">OUTPUTS</span></span>

### <span data-ttu-id="3ef1e-167">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="3ef1e-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer</span></span>

## <span data-ttu-id="3ef1e-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ef1e-168">NOTES</span></span>

## <span data-ttu-id="3ef1e-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ef1e-169">RELATED LINKS</span></span>

