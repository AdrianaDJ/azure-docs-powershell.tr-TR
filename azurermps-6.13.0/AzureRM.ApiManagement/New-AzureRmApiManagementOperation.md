---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: d7411b99847b76db5f6e01215b49056842d4e444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587342"
---
# <span data-ttu-id="6b5e3-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6b5e3-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="6b5e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b5e3-103">Bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b5e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b5e3-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b5e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b5e3-105">DESCRIPTION</span></span>
<span data-ttu-id="6b5e3-106">**Yeni-Azurermapımanagementoperation** cmdlet 'ı bir API işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="6b5e3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b5e3-107">EXAMPLES</span></span>

### <span data-ttu-id="6b5e3-108">Örnek 1: bir API yönetim işlemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b5e3-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="6b5e3-109">Bu komut bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="6b5e3-110">Örnek 2: istek ve yanıt ayrıntılarını içeren bir API yönetim işlemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b5e3-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="6b5e3-111">Bu örnek, istek ve yanıt ayrıntılarını içeren bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="6b5e3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b5e3-112">PARAMETERS</span></span>

### <span data-ttu-id="6b5e3-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="6b5e3-113">-ApiId</span></span>
<span data-ttu-id="6b5e3-114">API yönetim işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="6b5e3-115">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="6b5e3-115">-ApiRevision</span></span>
<span data-ttu-id="6b5e3-116">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-116">Identifier of API Revision.</span></span> <span data-ttu-id="6b5e3-117">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-117">This parameter is optional.</span></span> <span data-ttu-id="6b5e3-118">Belirtilmemişse, işlem geçerli etkin API düzeltmesine eklenir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="6b5e3-119">-Context</span><span class="sxs-lookup"><span data-stu-id="6b5e3-119">-Context</span></span>
<span data-ttu-id="6b5e3-120">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6b5e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b5e3-121">-DefaultProfile</span></span>
<span data-ttu-id="6b5e3-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b5e3-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="6b5e3-123">-Description</span></span>
<span data-ttu-id="6b5e3-124">Yeni API işleminin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="6b5e3-125">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="6b5e3-125">-Method</span></span>
<span data-ttu-id="6b5e3-126">Yeni API yönetim işleminin HTTP yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="6b5e3-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b5e3-127">-Name</span></span>
<span data-ttu-id="6b5e3-128">Yeni API yönetim işleminin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="6b5e3-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6b5e3-129">-OperationId</span></span>
<span data-ttu-id="6b5e3-130">API yönetim işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="6b5e3-131">-İstek</span><span class="sxs-lookup"><span data-stu-id="6b5e3-131">-Request</span></span>
<span data-ttu-id="6b5e3-132">API yönetim işleminin ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-132">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b5e3-133">-Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="6b5e3-133">-Responses</span></span>
<span data-ttu-id="6b5e3-134">Olası bir API yönetim işlemi yanıtları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-134">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b5e3-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="6b5e3-135">-TemplateParameters</span></span>
<span data-ttu-id="6b5e3-136">*URL şablonunda* tanımlanan bir parametre dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="6b5e3-137">Bu parametreyi belirtmezseniz, *URLTEMPLATE* temel alınarak varsayılan bir değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b5e3-138">-Urlşablonu</span><span class="sxs-lookup"><span data-stu-id="6b5e3-138">-UrlTemplate</span></span>
<span data-ttu-id="6b5e3-139">URL şablonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="6b5e3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b5e3-140">CommonParameters</span></span>
<span data-ttu-id="6b5e3-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b5e3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b5e3-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b5e3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b5e3-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b5e3-143">INPUTS</span></span>

### <span data-ttu-id="6b5e3-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6b5e3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6b5e3-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6b5e3-145">System.String</span></span>

### <span data-ttu-id="6b5e3-146">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementparameter []</span><span class="sxs-lookup"><span data-stu-id="6b5e3-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="6b5e3-147">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementrequest</span><span class="sxs-lookup"><span data-stu-id="6b5e3-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="6b5e3-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementresponse []</span><span class="sxs-lookup"><span data-stu-id="6b5e3-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="6b5e3-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b5e3-149">OUTPUTS</span></span>

### <span data-ttu-id="6b5e3-150">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="6b5e3-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="6b5e3-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b5e3-151">NOTES</span></span>

## <span data-ttu-id="6b5e3-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b5e3-152">RELATED LINKS</span></span>

[<span data-ttu-id="6b5e3-153">Get-Azurermapsananama</span><span class="sxs-lookup"><span data-stu-id="6b5e3-153">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="6b5e3-154">Remove-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="6b5e3-154">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="6b5e3-155">Set-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="6b5e3-155">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


