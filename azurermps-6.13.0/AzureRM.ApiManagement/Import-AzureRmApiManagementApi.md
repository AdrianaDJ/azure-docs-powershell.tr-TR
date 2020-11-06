---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 7eb2e25f137abb303e1c9fa5b4ebe8b932346871
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589617"
---
# <span data-ttu-id="8dbbd-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8dbbd-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="8dbbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dbbd-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbbd-103">Dosyadan veya URL 'den API içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8dbbd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8dbbd-104">SYNTAX</span></span>

### <span data-ttu-id="8dbbd-105">Importfromyereldosya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8dbbd-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dbbd-106">Importfromurl</span><span class="sxs-lookup"><span data-stu-id="8dbbd-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dbbd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8dbbd-107">DESCRIPTION</span></span>
<span data-ttu-id="8dbbd-108">**Import-Azurermapımanagementapı** cmdlet 'i bir dosyadan BIR Azure API yönetim API 'Sini veya Web uygulaması Açıklama Dili (WADL), Web Hizmetleri Açıklama DILI (wsdl) veya Swagger biçimini alır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="8dbbd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8dbbd-109">EXAMPLES</span></span>

### <span data-ttu-id="8dbbd-110">Örnek 1 bir WADL dosyasından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="8dbbd-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="8dbbd-111">Bu komut belirtilen WADL dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="8dbbd-112">Örnek 2 Swagger dosyasından API alma</span><span class="sxs-lookup"><span data-stu-id="8dbbd-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="8dbbd-113">Bu komut belirtilen Swagger dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="8dbbd-114">Örnek 3: WADL bağlantısından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="8dbbd-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="8dbbd-115">Bu komut belirtilen WADL bağlantısından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="8dbbd-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8dbbd-116">PARAMETERS</span></span>

### <span data-ttu-id="8dbbd-117">-Apııd</span><span class="sxs-lookup"><span data-stu-id="8dbbd-117">-ApiId</span></span>
<span data-ttu-id="8dbbd-118">İçeri aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="8dbbd-119">Bu parametreyi belirtmezseniz, sizin için bir KIMLIK oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="8dbbd-120">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="8dbbd-120">-ApiRevision</span></span>
<span data-ttu-id="8dbbd-121">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-121">Identifier of API Revision.</span></span> <span data-ttu-id="8dbbd-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-122">This parameter is optional.</span></span> <span data-ttu-id="8dbbd-123">Belirtilmezse, içeri aktarma işlemi şu anda etkin olan düzeltme veya yeni bir API ile yapılır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="8dbbd-124">-Apitürü</span><span class="sxs-lookup"><span data-stu-id="8dbbd-124">-ApiType</span></span>
<span data-ttu-id="8dbbd-125">Bu parametre, varsayılan http değeriyle isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="8dbbd-126">SOAP seçeneği yalnızca WSDL içeri aktarırken geçerlidir ve SOAP PASSTHROUGH API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="8dbbd-127">-Context</span><span class="sxs-lookup"><span data-stu-id="8dbbd-127">-Context</span></span>
<span data-ttu-id="8dbbd-128">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8dbbd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dbbd-129">-DefaultProfile</span></span>
<span data-ttu-id="8dbbd-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dbbd-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="8dbbd-131">-Path</span></span>
<span data-ttu-id="8dbbd-132">API 'nin Genel URL 'sinin son bölümü olarak bir Web API yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="8dbbd-133">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="8dbbd-134">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="8dbbd-135">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="8dbbd-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="8dbbd-136">-SpecificationFormat</span></span>
<span data-ttu-id="8dbbd-137">Belirtim biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-137">Specifies the specification format.</span></span>
<span data-ttu-id="8dbbd-138">Wadl, WSDL ve Swagger psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="8dbbd-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="8dbbd-139">-SpecificationPath</span></span>
<span data-ttu-id="8dbbd-140">Belirtim dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="8dbbd-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="8dbbd-141">-SpecificationUrl</span></span>
<span data-ttu-id="8dbbd-142">Belirtim URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="8dbbd-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="8dbbd-143">-WsdlEndpointName</span></span>
<span data-ttu-id="8dbbd-144">İçeri aktarılacak WSDL uç noktasının (bağlantı noktası) yerel adı.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="8dbbd-145">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="8dbbd-146">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="8dbbd-147">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-147">Default value is $null.</span></span>

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

### <span data-ttu-id="8dbbd-148">-Wsdlhizmetadı</span><span class="sxs-lookup"><span data-stu-id="8dbbd-148">-WsdlServiceName</span></span>
<span data-ttu-id="8dbbd-149">İçeri aktarılacak WSDL hizmetinin yerel adı.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="8dbbd-150">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="8dbbd-151">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="8dbbd-152">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-152">Default value is $null.</span></span>

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

### <span data-ttu-id="8dbbd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbbd-153">CommonParameters</span></span>
<span data-ttu-id="8dbbd-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8dbbd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbbd-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dbbd-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbbd-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8dbbd-156">INPUTS</span></span>

### <span data-ttu-id="8dbbd-157">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="8dbbd-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8dbbd-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8dbbd-158">System.String</span></span>

### <span data-ttu-id="8dbbd-159">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapiformat</span><span class="sxs-lookup"><span data-stu-id="8dbbd-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="8dbbd-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapimanagementapitürü, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="8dbbd-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8dbbd-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8dbbd-161">OUTPUTS</span></span>

### <span data-ttu-id="8dbbd-162">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="8dbbd-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8dbbd-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8dbbd-163">NOTES</span></span>

## <span data-ttu-id="8dbbd-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8dbbd-164">RELATED LINKS</span></span>

[<span data-ttu-id="8dbbd-165">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="8dbbd-165">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="8dbbd-166">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="8dbbd-166">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="8dbbd-167">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="8dbbd-167">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="8dbbd-168">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="8dbbd-168">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="8dbbd-169">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="8dbbd-169">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


