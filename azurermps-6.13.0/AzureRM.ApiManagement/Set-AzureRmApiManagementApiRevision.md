---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592814"
---
# <span data-ttu-id="a8dcd-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="a8dcd-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="a8dcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8dcd-102">SYNOPSIS</span></span>
<span data-ttu-id="a8dcd-103">API düzeltmesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="a8dcd-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8dcd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8dcd-104">SYNTAX</span></span>

### <span data-ttu-id="a8dcd-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a8dcd-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8dcd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a8dcd-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8dcd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8dcd-107">DESCRIPTION</span></span>
<span data-ttu-id="a8dcd-108">**Set-Azurermapımanagementapirevision** cmdlet 'ı BIR Azure API yönetim API düzenlemesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="a8dcd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8dcd-109">EXAMPLES</span></span>

### <span data-ttu-id="a8dcd-110">Örnek 1 API düzeltmesini değiştirme</span><span class="sxs-lookup"><span data-stu-id="a8dcd-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="a8dcd-111">Cmdlet, `2` API 'nin düzeltmesini `echo-api` Yeni bir açıklama, protokol ve yol ile güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="a8dcd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8dcd-112">PARAMETERS</span></span>

### <span data-ttu-id="a8dcd-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="a8dcd-113">-ApiId</span></span>
<span data-ttu-id="a8dcd-114">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-114">Identifier of existing API.</span></span>
<span data-ttu-id="a8dcd-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-115">This parameter is required.</span></span>

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

### <span data-ttu-id="a8dcd-116">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="a8dcd-116">-ApiRevision</span></span>
<span data-ttu-id="a8dcd-117">Var olan API düzeltmesine ait tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="a8dcd-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a8dcd-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="a8dcd-119">-AuthorizationScope</span></span>
<span data-ttu-id="a8dcd-120">OAuth işlemleri kapsamı.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-120">OAuth operations scope.</span></span>
<span data-ttu-id="a8dcd-121">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-121">This parameter is optional.</span></span>
<span data-ttu-id="a8dcd-122">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-122">Default value is $null.</span></span>

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

### <span data-ttu-id="a8dcd-123">-Authorizationserverıd</span><span class="sxs-lookup"><span data-stu-id="a8dcd-123">-AuthorizationServerId</span></span>
<span data-ttu-id="a8dcd-124">OAuth yetkilendirme sunucusu tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="a8dcd-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-125">This parameter is optional.</span></span>
<span data-ttu-id="a8dcd-126">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-126">Default value is $null.</span></span>
<span data-ttu-id="a8dcd-127">, AuthorizationScope belirtilmişse belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="a8dcd-128">-Context</span><span class="sxs-lookup"><span data-stu-id="a8dcd-128">-Context</span></span>
<span data-ttu-id="a8dcd-129">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a8dcd-130">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-130">This parameter is required.</span></span>

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

### <span data-ttu-id="a8dcd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8dcd-131">-DefaultProfile</span></span>
<span data-ttu-id="a8dcd-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8dcd-133">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a8dcd-133">-Description</span></span>
<span data-ttu-id="a8dcd-134">Web API açıklaması.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-134">Web API description.</span></span>
<span data-ttu-id="a8dcd-135">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="a8dcd-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8dcd-136">-InputObject</span></span>
<span data-ttu-id="a8dcd-137">PsApiManagementApi örneği.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="a8dcd-138">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-138">This parameter is required.</span></span>

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

### <span data-ttu-id="a8dcd-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8dcd-139">-Name</span></span>
<span data-ttu-id="a8dcd-140">Web API adı.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-140">Web API name.</span></span>
<span data-ttu-id="a8dcd-141">Geliştirici ve yönetici portalları 'nda görüneceği şekliyle API 'nin genel adı.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="a8dcd-142">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-142">This parameter is required.</span></span>

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

### <span data-ttu-id="a8dcd-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a8dcd-143">-PassThru</span></span>
<span data-ttu-id="a8dcd-144">Eğer belirtilmişse, ayarlanmış API 'yi temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapimanagementapı türü.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="a8dcd-145">-Yol</span><span class="sxs-lookup"><span data-stu-id="a8dcd-145">-Path</span></span>
<span data-ttu-id="a8dcd-146">Web API yolu.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-146">Web API Path.</span></span>
<span data-ttu-id="a8dcd-147">API 'nin Genel URL 'sinin son bölümü.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="a8dcd-148">Bu URL, Web hizmetine istek göndermek için API tüketicileri tarafından kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="a8dcd-149">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="a8dcd-150">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-150">This parameter is optional.</span></span>
<span data-ttu-id="a8dcd-151">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-151">Default value is $null.</span></span>

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

### <span data-ttu-id="a8dcd-152">-Protokoller</span><span class="sxs-lookup"><span data-stu-id="a8dcd-152">-Protocols</span></span>
<span data-ttu-id="a8dcd-153">Web API protokolleri (http, https).</span><span class="sxs-lookup"><span data-stu-id="a8dcd-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="a8dcd-154">API 'nın kullanılabileceği iletişim kuralları.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="a8dcd-155">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-155">This parameter is required.</span></span>
<span data-ttu-id="a8dcd-156">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-156">Default value is $null.</span></span>

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

### <span data-ttu-id="a8dcd-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="a8dcd-157">-ServiceUrl</span></span>
<span data-ttu-id="a8dcd-158">API 'yi kullanan Web hizmetinin URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="a8dcd-159">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="a8dcd-160">1-2000 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="a8dcd-161">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-161">This parameter is required.</span></span>

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

### <span data-ttu-id="a8dcd-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="a8dcd-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="a8dcd-163">Abonelik anahtarı üstbilgi adı.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-163">Subscription key header name.</span></span>
<span data-ttu-id="a8dcd-164">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-164">This parameter is optional.</span></span>
<span data-ttu-id="a8dcd-165">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-165">Default value is $null.</span></span>

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

### <span data-ttu-id="a8dcd-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="a8dcd-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="a8dcd-167">Abonelik anahtarı sorgu dizesi parametre adı.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="a8dcd-168">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-168">This parameter is optional.</span></span>
<span data-ttu-id="a8dcd-169">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-169">Default value is $null.</span></span>

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

### <span data-ttu-id="a8dcd-170">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8dcd-170">-Confirm</span></span>
<span data-ttu-id="a8dcd-171">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8dcd-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8dcd-172">-WhatIf</span></span>
<span data-ttu-id="a8dcd-173">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8dcd-174">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8dcd-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8dcd-175">CommonParameters</span></span>
<span data-ttu-id="a8dcd-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8dcd-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8dcd-177">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8dcd-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8dcd-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8dcd-178">INPUTS</span></span>

### <span data-ttu-id="a8dcd-179">System. String</span><span class="sxs-lookup"><span data-stu-id="a8dcd-179">System.String</span></span>

### <span data-ttu-id="a8dcd-180">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a8dcd-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a8dcd-181">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a8dcd-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="a8dcd-182">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a8dcd-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a8dcd-183">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementschema []</span><span class="sxs-lookup"><span data-stu-id="a8dcd-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="a8dcd-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a8dcd-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a8dcd-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8dcd-185">OUTPUTS</span></span>

### <span data-ttu-id="a8dcd-186">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="a8dcd-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="a8dcd-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8dcd-187">NOTES</span></span>

## <span data-ttu-id="a8dcd-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8dcd-188">RELATED LINKS</span></span>

[<span data-ttu-id="a8dcd-189">Get-Azurermapımanagementapirevision</span><span class="sxs-lookup"><span data-stu-id="a8dcd-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="a8dcd-190">New-Azurermapımanagementapirevision</span><span class="sxs-lookup"><span data-stu-id="a8dcd-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="a8dcd-191">Remove-Azurermapımanagementapirevision</span><span class="sxs-lookup"><span data-stu-id="a8dcd-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
