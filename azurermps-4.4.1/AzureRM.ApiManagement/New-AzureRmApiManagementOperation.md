---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 545c1f57d269b8cdb36e006a07c754811e0f2b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591219"
---
# <span data-ttu-id="72f51-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="72f51-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="72f51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72f51-102">SYNOPSIS</span></span>
<span data-ttu-id="72f51-103">Bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72f51-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72f51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72f51-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72f51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72f51-105">DESCRIPTION</span></span>
<span data-ttu-id="72f51-106">**Yeni-Azurermapımanagementoperation** cmdlet 'ı bir API işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72f51-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="72f51-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72f51-107">EXAMPLES</span></span>

### <span data-ttu-id="72f51-108">Örnek 1: bir API yönetim işlemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="72f51-108">Example 1: Create an API management operation</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="72f51-109">Bu komut bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72f51-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="72f51-110">Örnek 2: istek ve yanıt ayrıntılarını içeren bir API yönetim işlemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="72f51-110">Example 2: Create an API management operation with request and response details</span></span>
```
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
New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="72f51-111">Bu örnek, istek ve yanıt ayrıntılarını içeren bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72f51-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="72f51-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72f51-112">PARAMETERS</span></span>

### <span data-ttu-id="72f51-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="72f51-113">-ApiId</span></span>
<span data-ttu-id="72f51-114">API yönetim işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="72f51-115">-Context</span><span class="sxs-lookup"><span data-stu-id="72f51-115">-Context</span></span>
<span data-ttu-id="72f51-116">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="72f51-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="72f51-117">-Description</span></span>
<span data-ttu-id="72f51-118">Yeni API işleminin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-118">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="72f51-119">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="72f51-119">-Method</span></span>
<span data-ttu-id="72f51-120">Yeni API yönetim işleminin HTTP yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-120">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="72f51-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="72f51-121">-Name</span></span>
<span data-ttu-id="72f51-122">Yeni API yönetim işleminin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-122">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="72f51-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="72f51-123">-OperationId</span></span>
<span data-ttu-id="72f51-124">API yönetim işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-124">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="72f51-125">-İstek</span><span class="sxs-lookup"><span data-stu-id="72f51-125">-Request</span></span>
<span data-ttu-id="72f51-126">API yönetim işleminin ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-126">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="72f51-127">-Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="72f51-127">-Responses</span></span>
<span data-ttu-id="72f51-128">Olası bir API yönetim işlemi yanıtları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-128">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="72f51-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="72f51-129">-TemplateParameters</span></span>
<span data-ttu-id="72f51-130">*URL şablonunda* tanımlanan bir parametre dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-130">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="72f51-131">Bu parametreyi belirtmezseniz, *URLTEMPLATE* temel alınarak varsayılan bir değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="72f51-131">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="72f51-132">-Urlşablonu</span><span class="sxs-lookup"><span data-stu-id="72f51-132">-UrlTemplate</span></span>
<span data-ttu-id="72f51-133">URL şablonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="72f51-133">Specifies the URL template.</span></span>

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

### <span data-ttu-id="72f51-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72f51-134">-DefaultProfile</span></span>
<span data-ttu-id="72f51-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72f51-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72f51-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72f51-136">CommonParameters</span></span>
<span data-ttu-id="72f51-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72f51-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72f51-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72f51-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72f51-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72f51-139">INPUTS</span></span>

## <span data-ttu-id="72f51-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72f51-140">OUTPUTS</span></span>

### <span data-ttu-id="72f51-141">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="72f51-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="72f51-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72f51-142">NOTES</span></span>

## <span data-ttu-id="72f51-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72f51-143">RELATED LINKS</span></span>

[<span data-ttu-id="72f51-144">Get-Azurermapsananama</span><span class="sxs-lookup"><span data-stu-id="72f51-144">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="72f51-145">Remove-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="72f51-145">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="72f51-146">Set-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="72f51-146">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


