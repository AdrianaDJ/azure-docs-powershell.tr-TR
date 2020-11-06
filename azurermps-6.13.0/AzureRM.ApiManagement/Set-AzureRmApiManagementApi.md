---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 10df1034b414260cb618c7de0b31b8ad93d30d0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592815"
---
# <span data-ttu-id="7a509-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7a509-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="7a509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a509-102">SYNOPSIS</span></span>
<span data-ttu-id="7a509-103">Bir API 'YI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7a509-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a509-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a509-104">SYNTAX</span></span>

### <span data-ttu-id="7a509-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7a509-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a509-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a509-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a509-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a509-107">DESCRIPTION</span></span>
<span data-ttu-id="7a509-108">**Set-Azurermapımanagementapı** cmdlet 'ı BIR Azure API yönetim API 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7a509-108">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="7a509-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a509-109">EXAMPLES</span></span>

### <span data-ttu-id="7a509-110">Örnek 1 API 'YI değiştirme</span><span class="sxs-lookup"><span data-stu-id="7a509-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="7a509-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a509-111">PARAMETERS</span></span>

### <span data-ttu-id="7a509-112">-Apııd</span><span class="sxs-lookup"><span data-stu-id="7a509-112">-ApiId</span></span>
<span data-ttu-id="7a509-113">Değiştirilecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="7a509-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="7a509-114">-AuthorizationScope</span></span>
<span data-ttu-id="7a509-115">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="7a509-116">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="7a509-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="7a509-117">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="7a509-117">-AuthorizationServerId</span></span>
<span data-ttu-id="7a509-118">OAuth yetkilendirme sunucusu tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="7a509-119">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="7a509-119">The default value is $Null.</span></span>
<span data-ttu-id="7a509-120">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a509-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="7a509-121">-Context</span><span class="sxs-lookup"><span data-stu-id="7a509-121">-Context</span></span>
<span data-ttu-id="7a509-122">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a509-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a509-123">-DefaultProfile</span></span>
<span data-ttu-id="7a509-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a509-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a509-125">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7a509-125">-Description</span></span>
<span data-ttu-id="7a509-126">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="7a509-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a509-127">-InputObject</span></span>
<span data-ttu-id="7a509-128">PsApiManagementApi örneği.</span><span class="sxs-lookup"><span data-stu-id="7a509-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="7a509-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7a509-129">This parameter is required.</span></span>

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

### <span data-ttu-id="7a509-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="7a509-130">-Name</span></span>
<span data-ttu-id="7a509-131">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="7a509-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7a509-132">-PassThru</span></span>
<span data-ttu-id="7a509-133">geçiş</span><span class="sxs-lookup"><span data-stu-id="7a509-133">passthru</span></span>

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

### <span data-ttu-id="7a509-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="7a509-134">-Path</span></span>
<span data-ttu-id="7a509-135">API 'nin Genel URL 'sinin son bölümü olan Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="7a509-136">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a509-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="7a509-137">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="7a509-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="7a509-138">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="7a509-138">-Protocols</span></span>
<span data-ttu-id="7a509-139">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="7a509-140">http ve https psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="7a509-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="7a509-141">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="7a509-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="7a509-142">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="7a509-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="7a509-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="7a509-143">-ServiceUrl</span></span>
<span data-ttu-id="7a509-144">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="7a509-145">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="7a509-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="7a509-146">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a509-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="7a509-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="7a509-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="7a509-148">Abonelik anahtarı üstbilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="7a509-149">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="7a509-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="7a509-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="7a509-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="7a509-151">Abonelik anahtarı sorgu dizesi parametresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a509-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="7a509-152">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="7a509-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="7a509-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a509-153">CommonParameters</span></span>
<span data-ttu-id="7a509-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a509-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a509-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a509-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a509-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a509-156">INPUTS</span></span>

### <span data-ttu-id="7a509-157">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="7a509-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7a509-158">System. String</span><span class="sxs-lookup"><span data-stu-id="7a509-158">System.String</span></span>

### <span data-ttu-id="7a509-159">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="7a509-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="7a509-160">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a509-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7a509-161">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="7a509-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="7a509-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a509-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a509-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a509-163">OUTPUTS</span></span>

### <span data-ttu-id="7a509-164">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="7a509-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7a509-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a509-165">NOTES</span></span>

## <span data-ttu-id="7a509-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a509-166">RELATED LINKS</span></span>

[<span data-ttu-id="7a509-167">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="7a509-167">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="7a509-168">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="7a509-168">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="7a509-169">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="7a509-169">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="7a509-170">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="7a509-170">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="7a509-171">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="7a509-171">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


