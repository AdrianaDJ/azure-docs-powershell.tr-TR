---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 75a6dbf480e8b2f2f3d9f7524db4e57e5ed88f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764494"
---
# <span data-ttu-id="43dde-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="43dde-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="43dde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43dde-102">SYNOPSIS</span></span>
<span data-ttu-id="43dde-103">Bir API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43dde-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43dde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43dde-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43dde-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="43dde-105">DESCRIPTION</span></span>
<span data-ttu-id="43dde-106">**Yeni-Azurermapsananagementapı** cmdlet 'ı BIR Azure API yönetim API 'si oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43dde-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="43dde-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43dde-107">EXAMPLES</span></span>

### <span data-ttu-id="43dde-108">Örnek 1: API oluşturma</span><span class="sxs-lookup"><span data-stu-id="43dde-108">Example 1: Create an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="43dde-109">Bu komut, belirtilen URL ile yankı adlı bir API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43dde-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="43dde-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43dde-110">PARAMETERS</span></span>

### <span data-ttu-id="43dde-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="43dde-111">-ApiId</span></span>
<span data-ttu-id="43dde-112">Oluşturulacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="43dde-113">Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir KIMLIK oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43dde-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="43dde-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="43dde-114">-AuthorizationScope</span></span>
<span data-ttu-id="43dde-115">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="43dde-116">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="43dde-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="43dde-117">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="43dde-117">-AuthorizationServerId</span></span>
<span data-ttu-id="43dde-118">OAuth yetkilendirme sunucusu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="43dde-119">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="43dde-119">The default value is $Null.</span></span>
<span data-ttu-id="43dde-120">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="43dde-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="43dde-121">-Context</span><span class="sxs-lookup"><span data-stu-id="43dde-121">-Context</span></span>
<span data-ttu-id="43dde-122">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="43dde-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43dde-123">-DefaultProfile</span></span>
<span data-ttu-id="43dde-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43dde-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="43dde-125">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="43dde-125">-Description</span></span>
<span data-ttu-id="43dde-126">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="43dde-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="43dde-127">-Name</span></span>
<span data-ttu-id="43dde-128">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="43dde-129">Bu, API 'nin geliştirici ve yönetici portalında göründüğü şekliyle genel adıdır.</span><span class="sxs-lookup"><span data-stu-id="43dde-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="43dde-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="43dde-130">-Path</span></span>
<span data-ttu-id="43dde-131">API 'nin Genel URL 'sinin son bölümü olan ve yönetici portalında Web API URL soneki alanına karşılık gelen Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="43dde-132">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="43dde-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="43dde-133">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="43dde-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="43dde-134">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="43dde-134">-ProductIds</span></span>
<span data-ttu-id="43dde-135">Yeni API 'yi ekleyeceğiniz ürün kimlikleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43dde-136">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="43dde-136">-Protocols</span></span>
<span data-ttu-id="43dde-137">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="43dde-138">Geçerli değerler http, https 'dir.</span><span class="sxs-lookup"><span data-stu-id="43dde-138">Valid values are http, https.</span></span>
<span data-ttu-id="43dde-139">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="43dde-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="43dde-140">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="43dde-140">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43dde-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="43dde-141">-ServiceUrl</span></span>
<span data-ttu-id="43dde-142">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="43dde-143">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="43dde-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="43dde-144">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="43dde-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="43dde-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="43dde-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="43dde-146">Abonelik anahtarı üst bilgi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="43dde-147">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="43dde-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="43dde-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="43dde-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="43dde-149">Abonelik anahtarı sorgu dizesi parametre adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43dde-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="43dde-150">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="43dde-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="43dde-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43dde-151">CommonParameters</span></span>
<span data-ttu-id="43dde-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43dde-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43dde-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43dde-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43dde-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43dde-154">INPUTS</span></span>

### <span data-ttu-id="43dde-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="43dde-155">None</span></span>
<span data-ttu-id="43dde-156">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="43dde-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43dde-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43dde-157">OUTPUTS</span></span>

### <span data-ttu-id="43dde-158">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="43dde-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="43dde-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43dde-159">NOTES</span></span>

## <span data-ttu-id="43dde-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43dde-160">RELATED LINKS</span></span>

[<span data-ttu-id="43dde-161">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="43dde-161">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="43dde-162">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="43dde-162">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="43dde-163">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="43dde-163">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="43dde-164">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="43dde-164">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="43dde-165">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="43dde-165">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


