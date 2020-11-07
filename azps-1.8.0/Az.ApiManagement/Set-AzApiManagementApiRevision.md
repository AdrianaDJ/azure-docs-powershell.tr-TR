---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: 8b2e29da3c3f6140cbab422e74d09656c921c16c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917715"
---
# <span data-ttu-id="fb934-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="fb934-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="fb934-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb934-102">SYNOPSIS</span></span>
<span data-ttu-id="fb934-103">API düzeltmesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="fb934-103">Modifies an API Revision</span></span>

## <span data-ttu-id="fb934-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb934-104">SYNTAX</span></span>

### <span data-ttu-id="fb934-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb934-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb934-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb934-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb934-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb934-107">DESCRIPTION</span></span>
<span data-ttu-id="fb934-108">**Set-Azapsananagementapirevision** cmdlet 'ı BIR Azure API yönetim API düzenlemesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fb934-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="fb934-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb934-109">EXAMPLES</span></span>

### <span data-ttu-id="fb934-110">Örnek 1 API düzeltmesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="fb934-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="fb934-111">Cmdlet, `2` API 'nin düzeltmesini `echo-api` Yeni bir açıklama, protokol ve yol ile güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fb934-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="fb934-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb934-112">PARAMETERS</span></span>

### <span data-ttu-id="fb934-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="fb934-113">-ApiId</span></span>
<span data-ttu-id="fb934-114">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="fb934-114">Identifier of existing API.</span></span>
<span data-ttu-id="fb934-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb934-115">This parameter is required.</span></span>

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

### <span data-ttu-id="fb934-116">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="fb934-116">-ApiRevision</span></span>
<span data-ttu-id="fb934-117">Var olan API düzeltmesine ait tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="fb934-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="fb934-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb934-118">This parameter is required.</span></span>

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

### <span data-ttu-id="fb934-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="fb934-119">-AuthorizationScope</span></span>
<span data-ttu-id="fb934-120">OAuth işlemleri kapsamı.</span><span class="sxs-lookup"><span data-stu-id="fb934-120">OAuth operations scope.</span></span>
<span data-ttu-id="fb934-121">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fb934-121">This parameter is optional.</span></span>
<span data-ttu-id="fb934-122">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="fb934-122">Default value is $null.</span></span>

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

### <span data-ttu-id="fb934-123">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="fb934-123">-AuthorizationServerId</span></span>
<span data-ttu-id="fb934-124">OAuth yetkilendirme sunucusu tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="fb934-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="fb934-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fb934-125">This parameter is optional.</span></span>
<span data-ttu-id="fb934-126">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="fb934-126">Default value is $null.</span></span>
<span data-ttu-id="fb934-127">, AuthorizationScope belirtilmişse belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fb934-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="fb934-128">-Context</span><span class="sxs-lookup"><span data-stu-id="fb934-128">-Context</span></span>
<span data-ttu-id="fb934-129">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="fb934-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fb934-130">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb934-130">This parameter is required.</span></span>

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

### <span data-ttu-id="fb934-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb934-131">-DefaultProfile</span></span>
<span data-ttu-id="fb934-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb934-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb934-133">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="fb934-133">-Description</span></span>
<span data-ttu-id="fb934-134">Web API açıklaması.</span><span class="sxs-lookup"><span data-stu-id="fb934-134">Web API description.</span></span>
<span data-ttu-id="fb934-135">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fb934-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb934-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb934-136">-InputObject</span></span>
<span data-ttu-id="fb934-137">PsApiManagementApi örneği.</span><span class="sxs-lookup"><span data-stu-id="fb934-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="fb934-138">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb934-138">This parameter is required.</span></span>

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

### <span data-ttu-id="fb934-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb934-139">-Name</span></span>
<span data-ttu-id="fb934-140">Web API adı.</span><span class="sxs-lookup"><span data-stu-id="fb934-140">Web API name.</span></span>
<span data-ttu-id="fb934-141">Geliştirici ve yönetici portalları 'nda görüneceği şekliyle API 'nin genel adı.</span><span class="sxs-lookup"><span data-stu-id="fb934-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="fb934-142">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb934-142">This parameter is required.</span></span>

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

### <span data-ttu-id="fb934-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fb934-143">-PassThru</span></span>
<span data-ttu-id="fb934-144">Eğer belirtilmişse, ayarlanmış API 'yi temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapimanagementapı türü.</span><span class="sxs-lookup"><span data-stu-id="fb934-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="fb934-145">-Yol</span><span class="sxs-lookup"><span data-stu-id="fb934-145">-Path</span></span>
<span data-ttu-id="fb934-146">Web API yolu.</span><span class="sxs-lookup"><span data-stu-id="fb934-146">Web API Path.</span></span>
<span data-ttu-id="fb934-147">API 'nin Genel URL 'sinin son bölümü.</span><span class="sxs-lookup"><span data-stu-id="fb934-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="fb934-148">Bu URL, Web hizmetine istek göndermek için API tüketicileri tarafından kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="fb934-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="fb934-149">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fb934-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="fb934-150">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fb934-150">This parameter is optional.</span></span>
<span data-ttu-id="fb934-151">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="fb934-151">Default value is $null.</span></span>

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

### <span data-ttu-id="fb934-152">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="fb934-152">-Protocols</span></span>
<span data-ttu-id="fb934-153">Web API protokolleri (http, https).</span><span class="sxs-lookup"><span data-stu-id="fb934-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="fb934-154">API 'nın kullanılabileceği iletişim kuralları.</span><span class="sxs-lookup"><span data-stu-id="fb934-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="fb934-155">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb934-155">This parameter is required.</span></span>
<span data-ttu-id="fb934-156">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="fb934-156">Default value is $null.</span></span>

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

### <span data-ttu-id="fb934-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="fb934-157">-ServiceUrl</span></span>
<span data-ttu-id="fb934-158">API 'yi kullanan Web hizmetinin URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="fb934-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="fb934-159">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="fb934-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="fb934-160">1-2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fb934-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="fb934-161">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb934-161">This parameter is required.</span></span>

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

### <span data-ttu-id="fb934-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="fb934-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="fb934-163">Abonelik anahtarı üstbilgi adı.</span><span class="sxs-lookup"><span data-stu-id="fb934-163">Subscription key header name.</span></span>
<span data-ttu-id="fb934-164">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fb934-164">This parameter is optional.</span></span>
<span data-ttu-id="fb934-165">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="fb934-165">Default value is $null.</span></span>

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

### <span data-ttu-id="fb934-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="fb934-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="fb934-167">Abonelik anahtarı sorgu dizesi parametre adı.</span><span class="sxs-lookup"><span data-stu-id="fb934-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="fb934-168">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fb934-168">This parameter is optional.</span></span>
<span data-ttu-id="fb934-169">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="fb934-169">Default value is $null.</span></span>

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

### <span data-ttu-id="fb934-170">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb934-170">-Confirm</span></span>
<span data-ttu-id="fb934-171">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb934-171">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb934-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb934-172">-WhatIf</span></span>
<span data-ttu-id="fb934-173">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb934-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb934-174">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb934-174">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb934-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb934-175">CommonParameters</span></span>
<span data-ttu-id="fb934-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb934-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb934-177">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb934-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb934-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb934-178">INPUTS</span></span>

### <span data-ttu-id="fb934-179">System. String</span><span class="sxs-lookup"><span data-stu-id="fb934-179">System.String</span></span>

### <span data-ttu-id="fb934-180">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="fb934-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fb934-181">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="fb934-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="fb934-182">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="fb934-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="fb934-183">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fb934-183">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb934-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb934-184">OUTPUTS</span></span>

### <span data-ttu-id="fb934-185">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="fb934-185">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="fb934-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb934-186">NOTES</span></span>

## <span data-ttu-id="fb934-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb934-187">RELATED LINKS</span></span>

[<span data-ttu-id="fb934-188">Get-Azapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="fb934-188">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="fb934-189">Yeni-Azapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="fb934-189">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="fb934-190">Remove-Azapsananagementapirevision</span><span class="sxs-lookup"><span data-stu-id="fb934-190">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)