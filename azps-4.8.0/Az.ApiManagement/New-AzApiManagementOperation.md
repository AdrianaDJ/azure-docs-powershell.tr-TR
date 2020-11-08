---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107993"
---
# <span data-ttu-id="dcb3c-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="dcb3c-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="dcb3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcb3c-102">SYNOPSIS</span></span>
<span data-ttu-id="dcb3c-103">Bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-103">Creates an API management operation.</span></span>

## <span data-ttu-id="dcb3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcb3c-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcb3c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcb3c-105">DESCRIPTION</span></span>
<span data-ttu-id="dcb3c-106">**Yeni-Azapsananagementoperation** cmdlet 'ı bir API işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="dcb3c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcb3c-107">EXAMPLES</span></span>

### <span data-ttu-id="dcb3c-108">Örnek 1: bir API yönetim işlemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dcb3c-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="dcb3c-109">Bu komut bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="dcb3c-110">Örnek 2: istek ve yanıt ayrıntılarını içeren bir API yönetim işlemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dcb3c-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
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
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="dcb3c-111">Bu örnek, istek ve yanıt ayrıntılarını içeren bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="dcb3c-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcb3c-112">PARAMETERS</span></span>

### <span data-ttu-id="dcb3c-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="dcb3c-113">-ApiId</span></span>
<span data-ttu-id="dcb3c-114">API yönetim işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="dcb3c-115">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="dcb3c-115">-ApiRevision</span></span>
<span data-ttu-id="dcb3c-116">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-116">Identifier of API Revision.</span></span> <span data-ttu-id="dcb3c-117">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-117">This parameter is optional.</span></span> <span data-ttu-id="dcb3c-118">Belirtilmemişse, işlem geçerli etkin API düzeltmesine eklenir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="dcb3c-119">-Context</span><span class="sxs-lookup"><span data-stu-id="dcb3c-119">-Context</span></span>
<span data-ttu-id="dcb3c-120">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dcb3c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcb3c-121">-DefaultProfile</span></span>
<span data-ttu-id="dcb3c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcb3c-123">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="dcb3c-123">-Description</span></span>
<span data-ttu-id="dcb3c-124">Yeni API işleminin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="dcb3c-125">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="dcb3c-125">-Method</span></span>
<span data-ttu-id="dcb3c-126">Yeni API yönetim işleminin HTTP yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="dcb3c-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcb3c-127">-Name</span></span>
<span data-ttu-id="dcb3c-128">Yeni API yönetim işleminin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="dcb3c-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="dcb3c-129">-OperationId</span></span>
<span data-ttu-id="dcb3c-130">API yönetim işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="dcb3c-131">-İstek</span><span class="sxs-lookup"><span data-stu-id="dcb3c-131">-Request</span></span>
<span data-ttu-id="dcb3c-132">API yönetim işleminin ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-132">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="dcb3c-133">-Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="dcb3c-133">-Responses</span></span>
<span data-ttu-id="dcb3c-134">Olası bir API yönetim işlemi yanıtları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-134">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="dcb3c-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="dcb3c-135">-TemplateParameters</span></span>
<span data-ttu-id="dcb3c-136">*URL şablonunda* tanımlanan bir parametre dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="dcb3c-137">Bu parametreyi belirtmezseniz, *URLTEMPLATE* temel alınarak varsayılan bir değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="dcb3c-138">-Urlşablonu</span><span class="sxs-lookup"><span data-stu-id="dcb3c-138">-UrlTemplate</span></span>
<span data-ttu-id="dcb3c-139">URL şablonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="dcb3c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcb3c-140">CommonParameters</span></span>
<span data-ttu-id="dcb3c-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcb3c-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dcb3c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcb3c-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcb3c-143">INPUTS</span></span>

### <span data-ttu-id="dcb3c-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="dcb3c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dcb3c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="dcb3c-145">System.String</span></span>

### <span data-ttu-id="dcb3c-146">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementparameter []</span><span class="sxs-lookup"><span data-stu-id="dcb3c-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="dcb3c-147">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementrequest</span><span class="sxs-lookup"><span data-stu-id="dcb3c-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="dcb3c-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementresponse []</span><span class="sxs-lookup"><span data-stu-id="dcb3c-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="dcb3c-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcb3c-149">OUTPUTS</span></span>

### <span data-ttu-id="dcb3c-150">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="dcb3c-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="dcb3c-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcb3c-151">NOTES</span></span>

## <span data-ttu-id="dcb3c-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcb3c-152">RELATED LINKS</span></span>

[<span data-ttu-id="dcb3c-153">Get-Azapsananatomentoperation</span><span class="sxs-lookup"><span data-stu-id="dcb3c-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="dcb3c-154">Remove-Azapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="dcb3c-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="dcb3c-155">Set-Azapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="dcb3c-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


