---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 6ab29738f181f6fece9d3b4cd679496a9add9bc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591750"
---
# <span data-ttu-id="e5db7-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e5db7-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="e5db7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5db7-102">SYNOPSIS</span></span>
<span data-ttu-id="e5db7-103">Bir API 'YI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5db7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5db7-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5db7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5db7-105">DESCRIPTION</span></span>
<span data-ttu-id="e5db7-106">**Set-Azurermapımanagementapı** cmdlet 'ı BIR Azure API yönetim API 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="e5db7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5db7-107">EXAMPLES</span></span>

### <span data-ttu-id="e5db7-108">Örnek 1 API 'YI değiştirme</span><span class="sxs-lookup"><span data-stu-id="e5db7-108">Example 1 Modify an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="e5db7-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5db7-109">PARAMETERS</span></span>

### <span data-ttu-id="e5db7-110">-Apııd</span><span class="sxs-lookup"><span data-stu-id="e5db7-110">-ApiId</span></span>
<span data-ttu-id="e5db7-111">Değiştirilecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-111">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="e5db7-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="e5db7-112">-AuthorizationScope</span></span>
<span data-ttu-id="e5db7-113">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="e5db7-114">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="e5db7-114">The default value is $Null.</span></span>

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

### <span data-ttu-id="e5db7-115">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="e5db7-115">-AuthorizationServerId</span></span>
<span data-ttu-id="e5db7-116">OAuth yetkilendirme sunucusu tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="e5db7-117">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="e5db7-117">The default value is $Null.</span></span>
<span data-ttu-id="e5db7-118">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="e5db7-119">-Context</span><span class="sxs-lookup"><span data-stu-id="e5db7-119">-Context</span></span>
<span data-ttu-id="e5db7-120">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e5db7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5db7-121">-DefaultProfile</span></span>
<span data-ttu-id="e5db7-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5db7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e5db7-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e5db7-123">-Description</span></span>
<span data-ttu-id="e5db7-124">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-124">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="e5db7-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5db7-125">-Name</span></span>
<span data-ttu-id="e5db7-126">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-126">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="e5db7-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e5db7-127">-PassThru</span></span>
<span data-ttu-id="e5db7-128">geçiş</span><span class="sxs-lookup"><span data-stu-id="e5db7-128">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5db7-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="e5db7-129">-Path</span></span>
<span data-ttu-id="e5db7-130">API 'nin Genel URL 'sinin son bölümü olan Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-130">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="e5db7-131">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e5db7-131">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="e5db7-132">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="e5db7-132">The default value is $Null.</span></span>

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

### <span data-ttu-id="e5db7-133">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="e5db7-133">-Protocols</span></span>
<span data-ttu-id="e5db7-134">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-134">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="e5db7-135">http ve https psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="e5db7-135">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="e5db7-136">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-136">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="e5db7-137">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="e5db7-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="e5db7-138">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="e5db7-138">-ServiceUrl</span></span>
<span data-ttu-id="e5db7-139">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-139">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="e5db7-140">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="e5db7-140">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="e5db7-141">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e5db7-141">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="e5db7-142">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="e5db7-142">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="e5db7-143">Abonelik anahtarı üstbilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-143">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="e5db7-144">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="e5db7-144">The default value is $Null.</span></span>

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

### <span data-ttu-id="e5db7-145">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="e5db7-145">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="e5db7-146">Abonelik anahtarı sorgu dizesi parametresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5db7-146">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="e5db7-147">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="e5db7-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="e5db7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5db7-148">CommonParameters</span></span>
<span data-ttu-id="e5db7-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5db7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5db7-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5db7-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5db7-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5db7-151">INPUTS</span></span>

### <span data-ttu-id="e5db7-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e5db7-152">None</span></span>
<span data-ttu-id="e5db7-153">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e5db7-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5db7-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5db7-154">OUTPUTS</span></span>

### <span data-ttu-id="e5db7-155">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="e5db7-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e5db7-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5db7-156">NOTES</span></span>

## <span data-ttu-id="e5db7-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5db7-157">RELATED LINKS</span></span>

[<span data-ttu-id="e5db7-158">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="e5db7-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="e5db7-159">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="e5db7-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="e5db7-160">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="e5db7-160">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="e5db7-161">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="e5db7-161">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="e5db7-162">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="e5db7-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


