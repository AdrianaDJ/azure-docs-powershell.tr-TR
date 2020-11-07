---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 28bbc9158639faf066fa9a623f5dfacd6566d236
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764276"
---
# <span data-ttu-id="ddfee-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ddfee-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="ddfee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddfee-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfee-103">API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ddfee-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddfee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddfee-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ddfee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddfee-105">DESCRIPTION</span></span>
<span data-ttu-id="ddfee-106">**Set-Azurermapımanagementoperation** CMDLET 'i API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ddfee-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="ddfee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddfee-107">EXAMPLES</span></span>

### <span data-ttu-id="ddfee-108">Örnek 1: işlem ayrıntılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ddfee-108">Example 1: Set the operation details</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="ddfee-109">Bu komut API yönetimi için işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ddfee-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="ddfee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddfee-110">PARAMETERS</span></span>

### <span data-ttu-id="ddfee-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="ddfee-111">-ApiId</span></span>
<span data-ttu-id="ddfee-112">API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="ddfee-113">-Context</span><span class="sxs-lookup"><span data-stu-id="ddfee-113">-Context</span></span>
<span data-ttu-id="ddfee-114">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ddfee-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ddfee-115">-Description</span></span>
<span data-ttu-id="ddfee-116">Yeni işlemin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-116">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="ddfee-117">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="ddfee-117">-Method</span></span>
<span data-ttu-id="ddfee-118">Yeni işlemin HTTP yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-118">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="ddfee-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="ddfee-119">-Name</span></span>
<span data-ttu-id="ddfee-120">Yeni işlemin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-120">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="ddfee-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ddfee-121">-OperationId</span></span>
<span data-ttu-id="ddfee-122">Var olan işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-122">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="ddfee-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ddfee-123">-PassThru</span></span>
<span data-ttu-id="ddfee-124">geçiş</span><span class="sxs-lookup"><span data-stu-id="ddfee-124">passthru</span></span>

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

### <span data-ttu-id="ddfee-125">-İstek</span><span class="sxs-lookup"><span data-stu-id="ddfee-125">-Request</span></span>
<span data-ttu-id="ddfee-126">İşlem isteği ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-126">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="ddfee-127">-Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="ddfee-127">-Responses</span></span>
<span data-ttu-id="ddfee-128">Olası işlem yanıtlarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-128">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="ddfee-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="ddfee-129">-TemplateParameters</span></span>
<span data-ttu-id="ddfee-130">Parametre *URL 'Si şablonunda* tanımlanan bir dizi veya parametre belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-130">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="ddfee-131">Bir değer belirtmezseniz, UrlTemplate temel alınarak varsayılan bir değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ddfee-131">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="ddfee-132">Açıklama, tür ve diğer olası değerler gibi parametrelerle ilgili daha fazla ayrıntı vermek için parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ddfee-132">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="ddfee-133">-Urlşablonu</span><span class="sxs-lookup"><span data-stu-id="ddfee-133">-UrlTemplate</span></span>
<span data-ttu-id="ddfee-134">URL şablonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddfee-134">Specifies the URL template.</span></span>
<span data-ttu-id="ddfee-135">Örneğin: müşteriler/{CID}/siparişler/{OID}/? tarih = {Date}.</span><span class="sxs-lookup"><span data-stu-id="ddfee-135">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="ddfee-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfee-136">-DefaultProfile</span></span>
<span data-ttu-id="ddfee-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddfee-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddfee-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfee-138">CommonParameters</span></span>
<span data-ttu-id="ddfee-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddfee-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfee-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddfee-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfee-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddfee-141">INPUTS</span></span>

## <span data-ttu-id="ddfee-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddfee-142">OUTPUTS</span></span>

### <span data-ttu-id="ddfee-143">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="ddfee-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="ddfee-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddfee-144">NOTES</span></span>

## <span data-ttu-id="ddfee-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddfee-145">RELATED LINKS</span></span>

[<span data-ttu-id="ddfee-146">Get-Azurermapsananama</span><span class="sxs-lookup"><span data-stu-id="ddfee-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ddfee-147">Yeni-Azurermapsananaks</span><span class="sxs-lookup"><span data-stu-id="ddfee-147">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="ddfee-148">Remove-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="ddfee-148">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

