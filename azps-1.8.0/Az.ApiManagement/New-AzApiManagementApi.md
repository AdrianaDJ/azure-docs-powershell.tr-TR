---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 43793ef7d1d3f9a4e5e63687e1eaf785d237e86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751128"
---
# <span data-ttu-id="dd111-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="dd111-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="dd111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd111-102">SYNOPSIS</span></span>
<span data-ttu-id="dd111-103">Bir API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd111-103">Creates an API.</span></span>

## <span data-ttu-id="dd111-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd111-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd111-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd111-105">DESCRIPTION</span></span>
<span data-ttu-id="dd111-106">**Yeni-Azapsananagementapı** cmdlet 'ı BIR Azure API yönetim API 'si oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd111-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="dd111-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd111-107">EXAMPLES</span></span>

### <span data-ttu-id="dd111-108">Örnek 1: API oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd111-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="dd111-109">Bu komut, belirtilen URL ile yankı adlı bir API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd111-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="dd111-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd111-110">PARAMETERS</span></span>

### <span data-ttu-id="dd111-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="dd111-111">-ApiId</span></span>
<span data-ttu-id="dd111-112">Oluşturulacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="dd111-113">Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir KIMLIK oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd111-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="dd111-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="dd111-114">-AuthorizationScope</span></span>
<span data-ttu-id="dd111-115">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="dd111-116">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="dd111-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="dd111-117">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="dd111-117">-AuthorizationServerId</span></span>
<span data-ttu-id="dd111-118">OAuth yetkilendirme sunucusu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="dd111-119">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="dd111-119">The default value is $Null.</span></span>
<span data-ttu-id="dd111-120">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd111-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="dd111-121">-Context</span><span class="sxs-lookup"><span data-stu-id="dd111-121">-Context</span></span>
<span data-ttu-id="dd111-122">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dd111-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd111-123">-DefaultProfile</span></span>
<span data-ttu-id="dd111-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd111-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd111-125">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="dd111-125">-Description</span></span>
<span data-ttu-id="dd111-126">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="dd111-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd111-127">-Name</span></span>
<span data-ttu-id="dd111-128">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="dd111-129">Bu, API 'nin geliştirici ve yönetici portalında göründüğü şekliyle genel adıdır.</span><span class="sxs-lookup"><span data-stu-id="dd111-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="dd111-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="dd111-130">-Path</span></span>
<span data-ttu-id="dd111-131">API 'nin Genel URL 'sinin son bölümü olan ve yönetici portalında Web API URL soneki alanına karşılık gelen Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="dd111-132">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dd111-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="dd111-133">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="dd111-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="dd111-134">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="dd111-134">-ProductIds</span></span>
<span data-ttu-id="dd111-135">Yeni API 'yi ekleyeceğiniz ürün kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-135">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="dd111-136">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="dd111-136">-Protocols</span></span>
<span data-ttu-id="dd111-137">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="dd111-138">Geçerli değerler http, https 'dir.</span><span class="sxs-lookup"><span data-stu-id="dd111-138">Valid values are http, https.</span></span>
<span data-ttu-id="dd111-139">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="dd111-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="dd111-140">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="dd111-140">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd111-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="dd111-141">-ServiceUrl</span></span>
<span data-ttu-id="dd111-142">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="dd111-143">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="dd111-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="dd111-144">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dd111-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="dd111-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="dd111-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="dd111-146">Abonelik anahtarı üst bilgi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="dd111-147">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="dd111-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="dd111-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="dd111-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="dd111-149">Abonelik anahtarı sorgu dizesi parametre adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd111-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="dd111-150">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="dd111-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="dd111-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd111-151">CommonParameters</span></span>
<span data-ttu-id="dd111-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd111-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd111-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd111-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd111-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd111-154">INPUTS</span></span>

### <span data-ttu-id="dd111-155">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="dd111-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd111-156">System. String</span><span class="sxs-lookup"><span data-stu-id="dd111-156">System.String</span></span>

### <span data-ttu-id="dd111-157">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="dd111-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="dd111-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="dd111-158">System.String[]</span></span>

## <span data-ttu-id="dd111-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd111-159">OUTPUTS</span></span>

### <span data-ttu-id="dd111-160">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="dd111-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="dd111-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd111-161">NOTES</span></span>

## <span data-ttu-id="dd111-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd111-162">RELATED LINKS</span></span>

[<span data-ttu-id="dd111-163">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="dd111-163">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="dd111-164">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="dd111-164">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="dd111-165">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="dd111-165">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="dd111-166">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="dd111-166">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="dd111-167">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="dd111-167">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


