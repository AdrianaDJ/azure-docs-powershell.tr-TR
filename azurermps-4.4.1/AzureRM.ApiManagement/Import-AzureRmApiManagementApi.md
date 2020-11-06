---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: a95aa5cf5d78d2540fe2816cfa4b044502c69b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591245"
---
# <span data-ttu-id="ee474-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="ee474-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="ee474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee474-102">SYNOPSIS</span></span>
<span data-ttu-id="ee474-103">Dosyadan veya URL 'den API içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="ee474-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee474-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee474-104">SYNTAX</span></span>

### <span data-ttu-id="ee474-105">Yerel dosyadan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee474-105">From Local File (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee474-106">URL 'den</span><span class="sxs-lookup"><span data-stu-id="ee474-106">From URL</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee474-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee474-107">DESCRIPTION</span></span>
<span data-ttu-id="ee474-108">**Import-Azurermapımanagementapı** cmdlet 'i bir dosyadan BIR Azure API yönetim API 'Sini veya Web uygulaması Açıklama Dili (WADL), Web Hizmetleri Açıklama DILI (wsdl) veya Swagger biçimini alır.</span><span class="sxs-lookup"><span data-stu-id="ee474-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="ee474-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee474-109">EXAMPLES</span></span>

### <span data-ttu-id="ee474-110">Örnek 1 bir WADL dosyasından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="ee474-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="ee474-111">Bu komut belirtilen WADL dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="ee474-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="ee474-112">Örnek 2 Swagger dosyasından API alma</span><span class="sxs-lookup"><span data-stu-id="ee474-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="ee474-113">Bu komut belirtilen Swagger dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="ee474-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="ee474-114">Örnek 3: WADL bağlantısından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="ee474-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="ee474-115">Bu komut belirtilen WADL bağlantısından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="ee474-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="ee474-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee474-116">PARAMETERS</span></span>

### <span data-ttu-id="ee474-117">-Apııd</span><span class="sxs-lookup"><span data-stu-id="ee474-117">-ApiId</span></span>
<span data-ttu-id="ee474-118">İçeri aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee474-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="ee474-119">Bu parametreyi belirtmezseniz, sizin için bir KIMLIK oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ee474-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="ee474-120">-Apitürü</span><span class="sxs-lookup"><span data-stu-id="ee474-120">-ApiType</span></span>
<span data-ttu-id="ee474-121">Bu parametre, varsayılan http değeriyle isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ee474-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="ee474-122">SOAP seçeneği yalnızca WSDL içeri aktarırken geçerlidir ve SOAP PASSTHROUGH API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee474-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="ee474-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ee474-123">-Context</span></span>
<span data-ttu-id="ee474-124">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee474-124">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ee474-125">-Yol</span><span class="sxs-lookup"><span data-stu-id="ee474-125">-Path</span></span>
<span data-ttu-id="ee474-126">API 'nin Genel URL 'sinin son bölümü olarak bir Web API yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee474-126">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="ee474-127">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ee474-127">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="ee474-128">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ee474-128">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="ee474-129">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="ee474-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="ee474-130">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="ee474-130">-SpecificationFormat</span></span>
<span data-ttu-id="ee474-131">Belirtim biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee474-131">Specifies the specification format.</span></span>
<span data-ttu-id="ee474-132">Wadl, WSDL ve Swagger psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="ee474-132">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee474-133">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="ee474-133">-SpecificationPath</span></span>
<span data-ttu-id="ee474-134">Belirtim dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee474-134">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: From Local File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee474-135">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="ee474-135">-SpecificationUrl</span></span>
<span data-ttu-id="ee474-136">Belirtim URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee474-136">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: From URL
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee474-137">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="ee474-137">-WsdlEndpointName</span></span>
<span data-ttu-id="ee474-138">İçeri aktarılacak WSDL uç noktasının (bağlantı noktası) yerel adı.</span><span class="sxs-lookup"><span data-stu-id="ee474-138">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="ee474-139">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ee474-139">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="ee474-140">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ee474-140">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="ee474-141">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="ee474-141">Default value is $null.</span></span>

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

### <span data-ttu-id="ee474-142">-Wsdlhizmetadı</span><span class="sxs-lookup"><span data-stu-id="ee474-142">-WsdlServiceName</span></span>
<span data-ttu-id="ee474-143">İçeri aktarılacak WSDL hizmetinin yerel adı.</span><span class="sxs-lookup"><span data-stu-id="ee474-143">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="ee474-144">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ee474-144">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="ee474-145">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ee474-145">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="ee474-146">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="ee474-146">Default value is $null.</span></span>

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

### <span data-ttu-id="ee474-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee474-147">-DefaultProfile</span></span>
<span data-ttu-id="ee474-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee474-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee474-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee474-149">CommonParameters</span></span>
<span data-ttu-id="ee474-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee474-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee474-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee474-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee474-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee474-152">INPUTS</span></span>

## <span data-ttu-id="ee474-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee474-153">OUTPUTS</span></span>

### <span data-ttu-id="ee474-154">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="ee474-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="ee474-155">Bu cmdlet, alınan API 'YI **Psapimanagementapı** nesnesi olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="ee474-155">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="ee474-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee474-156">NOTES</span></span>

## <span data-ttu-id="ee474-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee474-157">RELATED LINKS</span></span>

[<span data-ttu-id="ee474-158">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="ee474-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="ee474-159">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="ee474-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="ee474-160">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="ee474-160">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="ee474-161">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="ee474-161">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="ee474-162">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="ee474-162">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


