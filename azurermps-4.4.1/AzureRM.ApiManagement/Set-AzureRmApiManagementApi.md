---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 4c9dc60ad1c531a5da9f32abc0090475c32a7ad5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593847"
---
# <span data-ttu-id="2e6c5-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e6c5-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="2e6c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6c5-103">Bir API 'YI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e6c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e6c5-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e6c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e6c5-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6c5-106">**Set-Azurermapımanagementapı** cmdlet 'ı BIR Azure API yönetim API 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="2e6c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e6c5-107">EXAMPLES</span></span>

### <span data-ttu-id="2e6c5-108">Örnek 1 API 'YI değiştirme</span><span class="sxs-lookup"><span data-stu-id="2e6c5-108">Example 1 Modify an API</span></span>
```
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="2e6c5-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e6c5-109">PARAMETERS</span></span>

### <span data-ttu-id="2e6c5-110">-Apııd</span><span class="sxs-lookup"><span data-stu-id="2e6c5-110">-ApiId</span></span>
<span data-ttu-id="2e6c5-111">Değiştirilecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-111">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="2e6c5-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2e6c5-112">-AuthorizationScope</span></span>
<span data-ttu-id="2e6c5-113">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2e6c5-114">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-114">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6c5-115">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="2e6c5-115">-AuthorizationServerId</span></span>
<span data-ttu-id="2e6c5-116">OAuth yetkilendirme sunucusu tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="2e6c5-117">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-117">The default value is $Null.</span></span>
<span data-ttu-id="2e6c5-118">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="2e6c5-119">-Context</span><span class="sxs-lookup"><span data-stu-id="2e6c5-119">-Context</span></span>
<span data-ttu-id="2e6c5-120">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e6c5-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="2e6c5-121">-Description</span></span>
<span data-ttu-id="2e6c5-122">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-122">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="2e6c5-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e6c5-123">-Name</span></span>
<span data-ttu-id="2e6c5-124">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-124">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="2e6c5-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2e6c5-125">-PassThru</span></span>
<span data-ttu-id="2e6c5-126">geçiş</span><span class="sxs-lookup"><span data-stu-id="2e6c5-126">passthru</span></span>

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

### <span data-ttu-id="2e6c5-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="2e6c5-127">-Path</span></span>
<span data-ttu-id="2e6c5-128">API 'nin Genel URL 'sinin son bölümü olan Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-128">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="2e6c5-129">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-129">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2e6c5-130">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-130">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6c5-131">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="2e6c5-131">-Protocols</span></span>
<span data-ttu-id="2e6c5-132">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-132">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2e6c5-133">http ve https psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-133">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="2e6c5-134">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-134">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2e6c5-135">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6c5-136">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2e6c5-136">-ServiceUrl</span></span>
<span data-ttu-id="2e6c5-137">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-137">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2e6c5-138">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-138">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2e6c5-139">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-139">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="2e6c5-140">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="2e6c5-140">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2e6c5-141">Abonelik anahtarı üstbilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-141">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="2e6c5-142">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6c5-143">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2e6c5-143">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2e6c5-144">Abonelik anahtarı sorgu dizesi parametresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-144">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="2e6c5-145">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6c5-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6c5-146">-DefaultProfile</span></span>
<span data-ttu-id="2e6c5-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e6c5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6c5-148">CommonParameters</span></span>
<span data-ttu-id="2e6c5-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6c5-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6c5-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6c5-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e6c5-151">INPUTS</span></span>

## <span data-ttu-id="2e6c5-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e6c5-152">OUTPUTS</span></span>

### <span data-ttu-id="2e6c5-153">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="2e6c5-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2e6c5-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e6c5-154">NOTES</span></span>

## <span data-ttu-id="2e6c5-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e6c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="2e6c5-156">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="2e6c5-156">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="2e6c5-157">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="2e6c5-157">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="2e6c5-158">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="2e6c5-158">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="2e6c5-159">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="2e6c5-159">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="2e6c5-160">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="2e6c5-160">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


