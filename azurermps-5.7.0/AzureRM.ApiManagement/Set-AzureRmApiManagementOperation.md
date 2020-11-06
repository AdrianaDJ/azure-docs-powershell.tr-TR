---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 4800d7d56d03071b57d25cdacfcf271defa9276f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590540"
---
# <span data-ttu-id="74a49-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="74a49-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="74a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74a49-102">SYNOPSIS</span></span>
<span data-ttu-id="74a49-103">API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="74a49-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74a49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74a49-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74a49-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74a49-105">DESCRIPTION</span></span>
<span data-ttu-id="74a49-106">**Set-Azurermapımanagementoperation** CMDLET 'i API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="74a49-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="74a49-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74a49-107">EXAMPLES</span></span>

### <span data-ttu-id="74a49-108">Örnek 1: işlem ayrıntılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="74a49-108">Example 1: Set the operation details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="74a49-109">Bu komut API yönetimi için işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="74a49-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="74a49-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74a49-110">PARAMETERS</span></span>

### <span data-ttu-id="74a49-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="74a49-111">-ApiId</span></span>
<span data-ttu-id="74a49-112">API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="74a49-113">-Context</span><span class="sxs-lookup"><span data-stu-id="74a49-113">-Context</span></span>
<span data-ttu-id="74a49-114">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="74a49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a49-115">-DefaultProfile</span></span>
<span data-ttu-id="74a49-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74a49-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="74a49-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="74a49-117">-Description</span></span>
<span data-ttu-id="74a49-118">Yeni işlemin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-118">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="74a49-119">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="74a49-119">-Method</span></span>
<span data-ttu-id="74a49-120">Yeni işlemin HTTP yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-120">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="74a49-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="74a49-121">-Name</span></span>
<span data-ttu-id="74a49-122">Yeni işlemin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-122">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="74a49-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="74a49-123">-OperationId</span></span>
<span data-ttu-id="74a49-124">Var olan işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-124">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="74a49-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="74a49-125">-PassThru</span></span>
<span data-ttu-id="74a49-126">geçiş</span><span class="sxs-lookup"><span data-stu-id="74a49-126">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a49-127">-İstek</span><span class="sxs-lookup"><span data-stu-id="74a49-127">-Request</span></span>
<span data-ttu-id="74a49-128">İşlem isteği ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-128">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="74a49-129">-Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="74a49-129">-Responses</span></span>
<span data-ttu-id="74a49-130">Olası işlem yanıtlarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-130">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="74a49-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="74a49-131">-TemplateParameters</span></span>
<span data-ttu-id="74a49-132">Parametre *URL 'Si şablonunda* tanımlanan bir dizi veya parametre belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-132">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="74a49-133">Bir değer belirtmezseniz, UrlTemplate temel alınarak varsayılan bir değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="74a49-133">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="74a49-134">Açıklama, tür ve diğer olası değerler gibi parametrelerle ilgili daha fazla ayrıntı vermek için parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="74a49-134">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="74a49-135">-Urlşablonu</span><span class="sxs-lookup"><span data-stu-id="74a49-135">-UrlTemplate</span></span>
<span data-ttu-id="74a49-136">URL şablonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="74a49-136">Specifies the URL template.</span></span>
<span data-ttu-id="74a49-137">Örneğin: müşteriler/{CID}/siparişler/{OID}/? tarih = {Date}.</span><span class="sxs-lookup"><span data-stu-id="74a49-137">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="74a49-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a49-138">CommonParameters</span></span>
<span data-ttu-id="74a49-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74a49-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a49-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a49-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a49-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74a49-141">INPUTS</span></span>

### <span data-ttu-id="74a49-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="74a49-142">None</span></span>
<span data-ttu-id="74a49-143">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="74a49-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74a49-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74a49-144">OUTPUTS</span></span>

### <span data-ttu-id="74a49-145">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="74a49-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="74a49-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74a49-146">NOTES</span></span>

## <span data-ttu-id="74a49-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74a49-147">RELATED LINKS</span></span>

[<span data-ttu-id="74a49-148">Get-Azurermapsananama</span><span class="sxs-lookup"><span data-stu-id="74a49-148">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="74a49-149">Yeni-Azurermapsananaks</span><span class="sxs-lookup"><span data-stu-id="74a49-149">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="74a49-150">Remove-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="74a49-150">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


