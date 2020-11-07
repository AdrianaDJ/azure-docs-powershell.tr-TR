---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementApi.md
ms.openlocfilehash: 5e00f3718b093f3112839ebb331fc96984a03038
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764497"
---
# <span data-ttu-id="da72a-101">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da72a-101">Import-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="da72a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da72a-102">SYNOPSIS</span></span>
<span data-ttu-id="da72a-103">Dosyadan veya URL 'den API içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="da72a-103">Imports an API from a file or a URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da72a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da72a-104">SYNTAX</span></span>

### <span data-ttu-id="da72a-105">Importfromyereldosya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="da72a-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da72a-106">Importfromurl</span><span class="sxs-lookup"><span data-stu-id="da72a-106">ImportFromUrl</span></span>
```
Import-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da72a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="da72a-107">DESCRIPTION</span></span>
<span data-ttu-id="da72a-108">**Import-Azurermapımanagementapı** cmdlet 'i bir dosyadan BIR Azure API yönetim API 'Sini veya Web uygulaması Açıklama Dili (WADL), Web Hizmetleri Açıklama DILI (wsdl) veya Swagger biçimini alır.</span><span class="sxs-lookup"><span data-stu-id="da72a-108">The **Import-AzureRmApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="da72a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da72a-109">EXAMPLES</span></span>

### <span data-ttu-id="da72a-110">Örnek 1 bir WADL dosyasından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="da72a-110">Example 1 Import an API from a WADL file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="da72a-111">Bu komut belirtilen WADL dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="da72a-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="da72a-112">Örnek 2 Swagger dosyasından API alma</span><span class="sxs-lookup"><span data-stu-id="da72a-112">Example 2 Import an API from a Swagger file</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="da72a-113">Bu komut belirtilen Swagger dosyasından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="da72a-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="da72a-114">Örnek 3: WADL bağlantısından API Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="da72a-114">Example 3: Import an API from a WADL link</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzureRmApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="da72a-115">Bu komut belirtilen WADL bağlantısından bir API alır.</span><span class="sxs-lookup"><span data-stu-id="da72a-115">This command imports an API from the specified WADL link.</span></span>

## <span data-ttu-id="da72a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da72a-116">PARAMETERS</span></span>

### <span data-ttu-id="da72a-117">-Apııd</span><span class="sxs-lookup"><span data-stu-id="da72a-117">-ApiId</span></span>
<span data-ttu-id="da72a-118">İçeri aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="da72a-118">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="da72a-119">Bu parametreyi belirtmezseniz, sizin için bir KIMLIK oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="da72a-119">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="da72a-120">-Apitürü</span><span class="sxs-lookup"><span data-stu-id="da72a-120">-ApiType</span></span>
<span data-ttu-id="da72a-121">Bu parametre, varsayılan http değeriyle isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="da72a-121">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="da72a-122">SOAP seçeneği yalnızca WSDL içeri aktarırken geçerlidir ve SOAP PASSTHROUGH API oluşturur.</span><span class="sxs-lookup"><span data-stu-id="da72a-122">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: PsApiManagementApiType
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da72a-123">-Context</span><span class="sxs-lookup"><span data-stu-id="da72a-123">-Context</span></span>
<span data-ttu-id="da72a-124">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da72a-124">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="da72a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da72a-125">-DefaultProfile</span></span>
<span data-ttu-id="da72a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da72a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="da72a-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="da72a-127">-Path</span></span>
<span data-ttu-id="da72a-128">API 'nin Genel URL 'sinin son bölümü olarak bir Web API yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="da72a-128">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="da72a-129">Bu URL, API tüketicileri tarafından Web hizmetine istek göndermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="da72a-129">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="da72a-130">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="da72a-130">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="da72a-131">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="da72a-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="da72a-132">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="da72a-132">-SpecificationFormat</span></span>
<span data-ttu-id="da72a-133">Belirtim biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da72a-133">Specifies the specification format.</span></span>
<span data-ttu-id="da72a-134">Wadl, WSDL ve Swagger psdx_paramvalues.</span><span class="sxs-lookup"><span data-stu-id="da72a-134">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da72a-135">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="da72a-135">-SpecificationPath</span></span>
<span data-ttu-id="da72a-136">Belirtim dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="da72a-136">Specifies the specification file path.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromLocalFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da72a-137">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="da72a-137">-SpecificationUrl</span></span>
<span data-ttu-id="da72a-138">Belirtim URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da72a-138">Specifies the specification URL.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromUrl
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da72a-139">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="da72a-139">-WsdlEndpointName</span></span>
<span data-ttu-id="da72a-140">İçeri aktarılacak WSDL uç noktasının (bağlantı noktası) yerel adı.</span><span class="sxs-lookup"><span data-stu-id="da72a-140">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="da72a-141">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="da72a-141">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="da72a-142">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="da72a-142">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="da72a-143">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="da72a-143">Default value is $null.</span></span>

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

### <span data-ttu-id="da72a-144">-Wsdlhizmetadı</span><span class="sxs-lookup"><span data-stu-id="da72a-144">-WsdlServiceName</span></span>
<span data-ttu-id="da72a-145">İçeri aktarılacak WSDL hizmetinin yerel adı.</span><span class="sxs-lookup"><span data-stu-id="da72a-145">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="da72a-146">1-400 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="da72a-146">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="da72a-147">Bu parametre isteğe bağlıdır ve yalnızca WSDL içeri aktarmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="da72a-147">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="da72a-148">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="da72a-148">Default value is $null.</span></span>

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

### <span data-ttu-id="da72a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da72a-149">CommonParameters</span></span>
<span data-ttu-id="da72a-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da72a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da72a-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da72a-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da72a-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da72a-152">INPUTS</span></span>

### <span data-ttu-id="da72a-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="da72a-153">None</span></span>
<span data-ttu-id="da72a-154">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="da72a-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da72a-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da72a-155">OUTPUTS</span></span>

### <span data-ttu-id="da72a-156">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="da72a-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="da72a-157">Bu cmdlet, alınan API 'YI **Psapimanagementapı** nesnesi olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="da72a-157">This cmdlet returns the imported API as a **PsApiManagementApi** object.</span></span>

## <span data-ttu-id="da72a-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da72a-158">NOTES</span></span>

## <span data-ttu-id="da72a-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da72a-159">RELATED LINKS</span></span>

[<span data-ttu-id="da72a-160">Dışarı aktarma-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="da72a-160">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="da72a-161">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="da72a-161">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="da72a-162">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="da72a-162">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="da72a-163">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="da72a-163">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="da72a-164">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="da72a-164">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


