---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 36560b23d9108ff1f8cd981abdb44a3c24f25402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586845"
---
# <span data-ttu-id="10eca-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="10eca-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="10eca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10eca-102">SYNOPSIS</span></span>
<span data-ttu-id="10eca-103">Bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10eca-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10eca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10eca-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10eca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="10eca-105">DESCRIPTION</span></span>
<span data-ttu-id="10eca-106">**Yeni-Azurermapımanagementoperation** cmdlet 'ı bir API işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10eca-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="10eca-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10eca-107">EXAMPLES</span></span>

### <span data-ttu-id="10eca-108">Örnek 1: bir API yönetim işlemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="10eca-108">Example 1: Create an API management operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="10eca-109">Bu komut bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10eca-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="10eca-110">Örnek 2: istek ve yanıt ayrıntılarını içeren bir API yönetim işlemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="10eca-110">Example 2: Create an API management operation with request and response details</span></span>
```
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

<span data-ttu-id="10eca-111">Bu örnek, istek ve yanıt ayrıntılarını içeren bir API yönetim işlemi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="10eca-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="10eca-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10eca-112">PARAMETERS</span></span>

### <span data-ttu-id="10eca-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="10eca-113">-ApiId</span></span>
<span data-ttu-id="10eca-114">API yönetim işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-114">Specifies the identifier of the API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eca-115">-Context</span><span class="sxs-lookup"><span data-stu-id="10eca-115">-Context</span></span>
<span data-ttu-id="10eca-116">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="10eca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10eca-117">-DefaultProfile</span></span>
<span data-ttu-id="10eca-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10eca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="10eca-119">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="10eca-119">-Description</span></span>
<span data-ttu-id="10eca-120">Yeni API işleminin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-120">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="10eca-121">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="10eca-121">-Method</span></span>
<span data-ttu-id="10eca-122">Yeni API yönetim işleminin HTTP yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-122">Specifies the HTTP method of the new API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eca-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="10eca-123">-Name</span></span>
<span data-ttu-id="10eca-124">Yeni API yönetim işleminin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-124">Specifies the display name of new API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eca-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="10eca-125">-OperationId</span></span>
<span data-ttu-id="10eca-126">API yönetim işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-126">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="10eca-127">-İstek</span><span class="sxs-lookup"><span data-stu-id="10eca-127">-Request</span></span>
<span data-ttu-id="10eca-128">API yönetim işleminin ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-128">Specifies the details of the API management operation.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eca-129">-Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="10eca-129">-Responses</span></span>
<span data-ttu-id="10eca-130">Olası bir API yönetim işlemi yanıtları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-130">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eca-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="10eca-131">-TemplateParameters</span></span>
<span data-ttu-id="10eca-132">*URL şablonunda* tanımlanan bir parametre dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-132">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="10eca-133">Bu parametreyi belirtmezseniz, *URLTEMPLATE* temel alınarak varsayılan bir değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="10eca-133">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eca-134">-Urlşablonu</span><span class="sxs-lookup"><span data-stu-id="10eca-134">-UrlTemplate</span></span>
<span data-ttu-id="10eca-135">URL şablonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="10eca-135">Specifies the URL template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10eca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10eca-136">CommonParameters</span></span>
<span data-ttu-id="10eca-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10eca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10eca-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10eca-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10eca-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10eca-139">INPUTS</span></span>

### <span data-ttu-id="10eca-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="10eca-140">None</span></span>
<span data-ttu-id="10eca-141">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="10eca-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10eca-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10eca-142">OUTPUTS</span></span>

### <span data-ttu-id="10eca-143">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="10eca-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="10eca-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10eca-144">NOTES</span></span>

## <span data-ttu-id="10eca-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10eca-145">RELATED LINKS</span></span>

[<span data-ttu-id="10eca-146">Get-Azurermapsananama</span><span class="sxs-lookup"><span data-stu-id="10eca-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="10eca-147">Remove-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="10eca-147">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="10eca-148">Set-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="10eca-148">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


