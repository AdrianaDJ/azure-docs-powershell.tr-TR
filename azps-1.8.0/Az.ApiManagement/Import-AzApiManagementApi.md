---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 690ebbfb1bb3cca6de8feb1f199068510e41f1d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751136"
---
# <span data-ttu-id="f7f20-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f7f20-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="f7f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f20-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f20-103">Dosyadan veya URL 'den API içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="f7f20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7f20-104">SYNTAX</span></span>

### <span data-ttu-id="f7f20-105">Importfromyereldosya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7f20-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7f20-106">Importfromurl</span><span class="sxs-lookup"><span data-stu-id="f7f20-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7f20-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7f20-107">DESCRIPTION</span></span>
<span data-ttu-id="f7f20-108">**Import-Azapsananagementapı** cmdlet 'i bir dosyadan BIR Azure API yönetim API 'Sini veya Web uygulaması Açıklama Dili (WADL), Web Hizmetleri Açıklama DILI (wsdl) veya Swagger biçimini alır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="f7f20-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7f20-109">EXAMPLES</span></span>

### <span data-ttu-id="f7f20-110">Örnek 1 bir WADL dosyasından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="f7f20-110">Example 1 Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="f7f20-111">Bu komut belirtilen WADL dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="f7f20-112">Örnek 2 Swagger dosyasından API alma</span><span class="sxs-lookup"><span data-stu-id="f7f20-112">Example 2 Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="f7f20-113">Bu komut belirtilen Swagger dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="f7f20-114">Örnek 3: WADL bağlantısından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="f7f20-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="f7f20-115">Bu komut belirtilen WADL bağlantısından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="f7f20-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7f20-116">PARAMETERS</span></span>

### <span data-ttu-id="f7f20-117">-Apııd</span><span class="sxs-lookup"><span data-stu-id="f7f20-117">-ApiId</span></span>
<span data-ttu-id="f7f20-118">İçeri aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7f20-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="f7f20-119">Bu parametreyi belirtmezseniz, sizin için bir KIMLIK oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f7f20-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="f7f20-120">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="f7f20-120">-ApiRevision</span></span>
<span data-ttu-id="f7f20-121">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="f7f20-121">Identifier of API Revision.</span></span> <span data-ttu-id="f7f20-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-122">This parameter is optional.</span></span> <span data-ttu-id="f7f20-123">Belirtilmezse, içeri aktarma işlemi şu anda etkin olan düzeltme veya yeni bir API ile yapılır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-123">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

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

### <span data-ttu-id="f7f20-124">-Apitürü</span><span class="sxs-lookup"><span data-stu-id="f7f20-124">-ApiType</span></span>
<span data-ttu-id="f7f20-125">Bu parametre, varsayılan http değeriyle isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-125">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="f7f20-126">SOAP seçeneği yalnızca WSDL içeri aktarırken geçerlidir ve SOAP PASSTHROUGH API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f7f20-126">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

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

### <span data-ttu-id="f7f20-127">-Context</span><span class="sxs-lookup"><span data-stu-id="f7f20-127">-Context</span></span>
<span data-ttu-id="f7f20-128">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7f20-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f7f20-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f20-129">-DefaultProfile</span></span>
<span data-ttu-id="f7f20-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7f20-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7f20-131">-Yol</span><span class="sxs-lookup"><span data-stu-id="f7f20-131">-Path</span></span>
<span data-ttu-id="f7f20-132">API 'nin Genel URL 'sinin son bölümü olarak bir Web API yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7f20-132">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="f7f20-133">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-133">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="f7f20-134">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-134">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="f7f20-135">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="f7f20-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="f7f20-136">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="f7f20-136">-SpecificationFormat</span></span>
<span data-ttu-id="f7f20-137">Belirtim biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7f20-137">Specifies the specification format.</span></span>
<span data-ttu-id="f7f20-138">Wadl, WSDL ve Swagger psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="f7f20-138">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

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

### <span data-ttu-id="f7f20-139">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="f7f20-139">-SpecificationPath</span></span>
<span data-ttu-id="f7f20-140">Belirtim dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7f20-140">Specifies the specification file path.</span></span>

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

### <span data-ttu-id="f7f20-141">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="f7f20-141">-SpecificationUrl</span></span>
<span data-ttu-id="f7f20-142">Belirtim URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7f20-142">Specifies the specification URL.</span></span>

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

### <span data-ttu-id="f7f20-143">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="f7f20-143">-WsdlEndpointName</span></span>
<span data-ttu-id="f7f20-144">İçeri aktarılacak WSDL uç noktasının (bağlantı noktası) yerel adı.</span><span class="sxs-lookup"><span data-stu-id="f7f20-144">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="f7f20-145">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-145">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="f7f20-146">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f7f20-146">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="f7f20-147">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="f7f20-147">Default value is $null.</span></span>

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

### <span data-ttu-id="f7f20-148">-Wsdlhizmetadı</span><span class="sxs-lookup"><span data-stu-id="f7f20-148">-WsdlServiceName</span></span>
<span data-ttu-id="f7f20-149">İçeri aktarılacak WSDL hizmetinin yerel adı.</span><span class="sxs-lookup"><span data-stu-id="f7f20-149">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="f7f20-150">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f7f20-150">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="f7f20-151">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f7f20-151">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="f7f20-152">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="f7f20-152">Default value is $null.</span></span>

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

### <span data-ttu-id="f7f20-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f20-153">CommonParameters</span></span>
<span data-ttu-id="f7f20-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7f20-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f20-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f20-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f20-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7f20-156">INPUTS</span></span>

### <span data-ttu-id="f7f20-157">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f7f20-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f7f20-158">System. String</span><span class="sxs-lookup"><span data-stu-id="f7f20-158">System.String</span></span>

### <span data-ttu-id="f7f20-159">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapiformat</span><span class="sxs-lookup"><span data-stu-id="f7f20-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="f7f20-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananayöneti. ServiceManagement. modeller. Psapimanagementapitürü, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="f7f20-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f7f20-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7f20-161">OUTPUTS</span></span>

### <span data-ttu-id="f7f20-162">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="f7f20-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f7f20-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7f20-163">NOTES</span></span>

## <span data-ttu-id="f7f20-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7f20-164">RELATED LINKS</span></span>

[<span data-ttu-id="f7f20-165">Dışarı aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="f7f20-165">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="f7f20-166">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="f7f20-166">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="f7f20-167">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="f7f20-167">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="f7f20-168">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="f7f20-168">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="f7f20-169">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="f7f20-169">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


