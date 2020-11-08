---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276462"
---
# <span data-ttu-id="73b9f-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="73b9f-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="73b9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73b9f-102">SYNOPSIS</span></span>
<span data-ttu-id="73b9f-103">Dosyadan veya URL 'den API içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="73b9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73b9f-104">SYNTAX</span></span>

### <span data-ttu-id="73b9f-105">Importfromyereldosya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73b9f-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b9f-106">Importfromurl</span><span class="sxs-lookup"><span data-stu-id="73b9f-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73b9f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="73b9f-107">DESCRIPTION</span></span>
<span data-ttu-id="73b9f-108">**Import-Azapsananagementapı** cmdlet 'i bir dosyadan BIR Azure API yönetim API 'Sini veya Web uygulaması Açıklama Dili (WADL), Web Hizmetleri Açıklama DILI (wsdl) veya Swagger biçimini alır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="73b9f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73b9f-109">EXAMPLES</span></span>

### <span data-ttu-id="73b9f-110">Örnek 1: WADL dosyasından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="73b9f-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="73b9f-111">Bu komut belirtilen WADL dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="73b9f-112">Örnek 2: bir Swagger dosyasından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="73b9f-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="73b9f-113">Bu komut belirtilen Swagger dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="73b9f-114">Örnek 3: WADL bağlantısından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="73b9f-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="73b9f-115">Bu komut belirtilen WADL bağlantısından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="73b9f-116">Örnek 4: açık bir API bağlantısından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="73b9f-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="73b9f-117">Bu komut, belirtilen 3,0 belirtim bağlantısından API 'yi içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="73b9f-118">Örnek 5: açık bir API bağlantısından bir Apıversion kümesine API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="73b9f-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="73b9f-119">Bu komut, belirtilen 3,0 belirtim belgesinden API 'yi içeri aktarır ve yeni bir Apıversion oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73b9f-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="73b9f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73b9f-120">PARAMETERS</span></span>

### <span data-ttu-id="73b9f-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="73b9f-121">-ApiId</span></span>
<span data-ttu-id="73b9f-122">İçeri aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="73b9f-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="73b9f-123">Bu parametreyi belirtmezseniz, sizin için bir KIMLIK oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="73b9f-123">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="73b9f-124">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="73b9f-124">-ApiRevision</span></span>
<span data-ttu-id="73b9f-125">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="73b9f-125">Identifier of API Revision.</span></span> <span data-ttu-id="73b9f-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-126">This parameter is optional.</span></span> <span data-ttu-id="73b9f-127">Belirtilmezse, içeri aktarma işlemi şu anda etkin olan düzeltme veya yeni bir API ile yapılır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="73b9f-128">-Apitürü</span><span class="sxs-lookup"><span data-stu-id="73b9f-128">-ApiType</span></span>
<span data-ttu-id="73b9f-129">Bu parametre, varsayılan http değeriyle isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="73b9f-130">SOAP seçeneği yalnızca WSDL içeri aktarırken geçerlidir ve SOAP PASSTHROUGH API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73b9f-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b9f-131">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="73b9f-131">-ApiVersion</span></span>
<span data-ttu-id="73b9f-132">API 'nın oluşturulacağı API sürümü.</span><span class="sxs-lookup"><span data-stu-id="73b9f-132">Api Version of the Api to create.</span></span> <span data-ttu-id="73b9f-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="73b9f-134">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="73b9f-134">-ApiVersionSetId</span></span>
<span data-ttu-id="73b9f-135">İlgili API sürüm kümesi için bir kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="73b9f-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="73b9f-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="73b9f-137">-Context</span><span class="sxs-lookup"><span data-stu-id="73b9f-137">-Context</span></span>
<span data-ttu-id="73b9f-138">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73b9f-138">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73b9f-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73b9f-139">-DefaultProfile</span></span>
<span data-ttu-id="73b9f-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73b9f-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73b9f-141">-Yol</span><span class="sxs-lookup"><span data-stu-id="73b9f-141">-Path</span></span>
<span data-ttu-id="73b9f-142">API 'nin Genel URL 'sinin son bölümü olarak bir Web API yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="73b9f-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="73b9f-143">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="73b9f-144">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="73b9f-145">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="73b9f-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="73b9f-146">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="73b9f-146">-Protocol</span></span>
<span data-ttu-id="73b9f-147">Web API protokolleri (http, https).</span><span class="sxs-lookup"><span data-stu-id="73b9f-147">Web API protocols (http, https).</span></span> <span data-ttu-id="73b9f-148">API 'nın kullanılabileceği iletişim kuralları.</span><span class="sxs-lookup"><span data-stu-id="73b9f-148">Protocols over which API is made available.</span></span> <span data-ttu-id="73b9f-149">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-149">This parameter is optional.</span></span> <span data-ttu-id="73b9f-150">Sağlanmışsa, Özellikler belgesinde belirtilen protokollerin üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="73b9f-150">If provided it will override the protocols specified in the specifications document.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b9f-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="73b9f-151">-ServiceUrl</span></span>
<span data-ttu-id="73b9f-152">API 'yi kullanan Web hizmetinin URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="73b9f-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="73b9f-153">Bu URL yalnızca Azure API Yönetimi tarafından kullanılır ve genel kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="73b9f-154">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-154">This parameter is optional.</span></span> <span data-ttu-id="73b9f-155">Sağlanmışsa, Özellikler belgesinde belirtilen ServiceUrl 'Yi geçersiz kılacaktır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

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

### <span data-ttu-id="73b9f-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="73b9f-156">-SpecificationFormat</span></span>
<span data-ttu-id="73b9f-157">Belirtim biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73b9f-157">Specifies the specification format.</span></span>
<span data-ttu-id="73b9f-158">Wadl, WSDL ve Swagger psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="73b9f-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b9f-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="73b9f-159">-SpecificationPath</span></span>
<span data-ttu-id="73b9f-160">Belirtim dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="73b9f-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b9f-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="73b9f-161">-SpecificationUrl</span></span>
<span data-ttu-id="73b9f-162">Belirtim URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73b9f-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73b9f-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="73b9f-163">-WsdlEndpointName</span></span>
<span data-ttu-id="73b9f-164">İçeri aktarılacak WSDL uç noktasının (bağlantı noktası) yerel adı.</span><span class="sxs-lookup"><span data-stu-id="73b9f-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="73b9f-165">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="73b9f-166">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="73b9f-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="73b9f-167">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="73b9f-167">Default value is $null.</span></span>

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

### <span data-ttu-id="73b9f-168">-Wsdlhizmetadı</span><span class="sxs-lookup"><span data-stu-id="73b9f-168">-WsdlServiceName</span></span>
<span data-ttu-id="73b9f-169">İçeri aktarılacak WSDL hizmetinin yerel adı.</span><span class="sxs-lookup"><span data-stu-id="73b9f-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="73b9f-170">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="73b9f-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="73b9f-171">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="73b9f-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="73b9f-172">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="73b9f-172">Default value is $null.</span></span>

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

### <span data-ttu-id="73b9f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73b9f-173">CommonParameters</span></span>
<span data-ttu-id="73b9f-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73b9f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73b9f-175">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="73b9f-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73b9f-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73b9f-176">INPUTS</span></span>

### <span data-ttu-id="73b9f-177">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="73b9f-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="73b9f-178">System. String</span><span class="sxs-lookup"><span data-stu-id="73b9f-178">System.String</span></span>

### <span data-ttu-id="73b9f-179">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapiformat</span><span class="sxs-lookup"><span data-stu-id="73b9f-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="73b9f-180">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananayöneti. ServiceManagement. modeller. Psapimanagementapitürü, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="73b9f-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="73b9f-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73b9f-181">OUTPUTS</span></span>

### <span data-ttu-id="73b9f-182">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="73b9f-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="73b9f-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73b9f-183">NOTES</span></span>

## <span data-ttu-id="73b9f-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73b9f-184">RELATED LINKS</span></span>

[<span data-ttu-id="73b9f-185">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="73b9f-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="73b9f-186">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="73b9f-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="73b9f-187">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="73b9f-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="73b9f-188">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="73b9f-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="73b9f-189">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="73b9f-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


