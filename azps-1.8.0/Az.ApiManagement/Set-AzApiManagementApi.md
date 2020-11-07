---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917724"
---
# <span data-ttu-id="32699-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="32699-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="32699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32699-102">SYNOPSIS</span></span>
<span data-ttu-id="32699-103">Bir API 'YI değiştirir.</span><span class="sxs-lookup"><span data-stu-id="32699-103">Modifies an API.</span></span>

## <span data-ttu-id="32699-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32699-104">SYNTAX</span></span>

### <span data-ttu-id="32699-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32699-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32699-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="32699-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32699-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="32699-107">DESCRIPTION</span></span>
<span data-ttu-id="32699-108">**Set-Azapsananagementapı** cmdlet 'ı BIR Azure API yönetim API 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="32699-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="32699-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32699-109">EXAMPLES</span></span>

### <span data-ttu-id="32699-110">Örnek 1 API 'YI değiştirme</span><span class="sxs-lookup"><span data-stu-id="32699-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="32699-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32699-111">PARAMETERS</span></span>

### <span data-ttu-id="32699-112">-Apııd</span><span class="sxs-lookup"><span data-stu-id="32699-112">-ApiId</span></span>
<span data-ttu-id="32699-113">Değiştirilecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="32699-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="32699-114">-AuthorizationScope</span></span>
<span data-ttu-id="32699-115">OAuth işlemleri kapsamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="32699-116">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="32699-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="32699-117">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="32699-117">-AuthorizationServerId</span></span>
<span data-ttu-id="32699-118">OAuth yetkilendirme sunucusu tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="32699-119">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="32699-119">The default value is $Null.</span></span>
<span data-ttu-id="32699-120">*Authorizationscope* belirtilmişse bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="32699-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="32699-121">-Context</span><span class="sxs-lookup"><span data-stu-id="32699-121">-Context</span></span>
<span data-ttu-id="32699-122">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="32699-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32699-123">-DefaultProfile</span></span>
<span data-ttu-id="32699-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32699-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32699-125">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="32699-125">-Description</span></span>
<span data-ttu-id="32699-126">Web API 'sinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="32699-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32699-127">-InputObject</span></span>
<span data-ttu-id="32699-128">PsApiManagementApi örneği.</span><span class="sxs-lookup"><span data-stu-id="32699-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="32699-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="32699-129">This parameter is required.</span></span>

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

### <span data-ttu-id="32699-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="32699-130">-Name</span></span>
<span data-ttu-id="32699-131">Web API 'sinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="32699-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="32699-132">-PassThru</span></span>
<span data-ttu-id="32699-133">geçiş</span><span class="sxs-lookup"><span data-stu-id="32699-133">passthru</span></span>

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

### <span data-ttu-id="32699-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="32699-134">-Path</span></span>
<span data-ttu-id="32699-135">API 'nin Genel URL 'sinin son bölümü olan Web API yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="32699-136">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır ve 400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="32699-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="32699-137">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="32699-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="32699-138">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="32699-138">-Protocols</span></span>
<span data-ttu-id="32699-139">Web API protokolleri dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="32699-140">http ve https psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="32699-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="32699-141">Bu, API 'nin kullanılabileceği Web protokollerdir.</span><span class="sxs-lookup"><span data-stu-id="32699-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="32699-142">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="32699-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="32699-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="32699-143">-ServiceUrl</span></span>
<span data-ttu-id="32699-144">API 'yi sunan Web hizmetinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="32699-145">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel olarak yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="32699-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="32699-146">URL, 2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="32699-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="32699-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="32699-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="32699-148">Abonelik anahtarı üstbilgisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="32699-149">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="32699-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="32699-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="32699-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="32699-151">Abonelik anahtarı sorgu dizesi parametresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32699-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="32699-152">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="32699-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="32699-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32699-153">CommonParameters</span></span>
<span data-ttu-id="32699-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32699-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32699-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32699-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32699-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32699-156">INPUTS</span></span>

### <span data-ttu-id="32699-157">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="32699-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="32699-158">System. String</span><span class="sxs-lookup"><span data-stu-id="32699-158">System.String</span></span>

### <span data-ttu-id="32699-159">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="32699-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="32699-160">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="32699-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="32699-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="32699-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="32699-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32699-162">OUTPUTS</span></span>

### <span data-ttu-id="32699-163">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="32699-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="32699-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32699-164">NOTES</span></span>

## <span data-ttu-id="32699-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32699-165">RELATED LINKS</span></span>

[<span data-ttu-id="32699-166">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="32699-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="32699-167">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="32699-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="32699-168">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="32699-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="32699-169">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="32699-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="32699-170">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="32699-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


