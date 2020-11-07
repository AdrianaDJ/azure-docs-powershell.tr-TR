---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: d30b48a7e1860610dc772555bc7e7428ec1ee3f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917683"
---
# <span data-ttu-id="6bee6-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6bee6-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="6bee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bee6-102">SYNOPSIS</span></span>
<span data-ttu-id="6bee6-103">API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6bee6-103">Sets API operation details.</span></span>

## <span data-ttu-id="6bee6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bee6-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bee6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bee6-105">DESCRIPTION</span></span>
<span data-ttu-id="6bee6-106">**Set-Azapsananagementoperation** CMDLET 'i API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6bee6-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="6bee6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bee6-107">EXAMPLES</span></span>

### <span data-ttu-id="6bee6-108">Örnek 1: işlem ayrıntılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6bee6-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="6bee6-109">Bu komut API yönetimi için işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6bee6-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="6bee6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bee6-110">PARAMETERS</span></span>

### <span data-ttu-id="6bee6-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="6bee6-111">-ApiId</span></span>
<span data-ttu-id="6bee6-112">API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="6bee6-113">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="6bee6-113">-ApiRevision</span></span>
<span data-ttu-id="6bee6-114">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6bee6-114">Identifier of API Revision.</span></span> <span data-ttu-id="6bee6-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6bee6-115">This parameter is optional.</span></span> <span data-ttu-id="6bee6-116">Belirtilmezse, işlem geçerli API düzeltmesinde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="6bee6-117">-Context</span><span class="sxs-lookup"><span data-stu-id="6bee6-117">-Context</span></span>
<span data-ttu-id="6bee6-118">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="6bee6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bee6-119">-DefaultProfile</span></span>
<span data-ttu-id="6bee6-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bee6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bee6-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="6bee6-121">-Description</span></span>
<span data-ttu-id="6bee6-122">Yeni işlemin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="6bee6-123">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="6bee6-123">-Method</span></span>
<span data-ttu-id="6bee6-124">Yeni işlemin HTTP yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="6bee6-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="6bee6-125">-Name</span></span>
<span data-ttu-id="6bee6-126">Yeni işlemin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="6bee6-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6bee6-127">-OperationId</span></span>
<span data-ttu-id="6bee6-128">Var olan işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="6bee6-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6bee6-129">-PassThru</span></span>
<span data-ttu-id="6bee6-130">geçiş</span><span class="sxs-lookup"><span data-stu-id="6bee6-130">passthru</span></span>

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

### <span data-ttu-id="6bee6-131">-İstek</span><span class="sxs-lookup"><span data-stu-id="6bee6-131">-Request</span></span>
<span data-ttu-id="6bee6-132">İşlem isteği ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="6bee6-133">-Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="6bee6-133">-Responses</span></span>
<span data-ttu-id="6bee6-134">Olası işlem yanıtlarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="6bee6-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="6bee6-135">-TemplateParameters</span></span>
<span data-ttu-id="6bee6-136">Parametre *URL 'Si şablonunda* tanımlanan bir dizi veya parametre belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="6bee6-137">Bir değer belirtmezseniz, UrlTemplate temel alınarak varsayılan bir değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6bee6-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="6bee6-138">Açıklama, tür ve diğer olası değerler gibi parametrelerle ilgili daha fazla ayrıntı vermek için parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="6bee6-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="6bee6-139">-Urlşablonu</span><span class="sxs-lookup"><span data-stu-id="6bee6-139">-UrlTemplate</span></span>
<span data-ttu-id="6bee6-140">URL şablonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bee6-140">Specifies the URL template.</span></span>
<span data-ttu-id="6bee6-141">Örneğin: müşteriler/{CID}/siparişler/{OID}/? tarih = {Date}.</span><span class="sxs-lookup"><span data-stu-id="6bee6-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="6bee6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bee6-142">CommonParameters</span></span>
<span data-ttu-id="6bee6-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bee6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bee6-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bee6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bee6-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bee6-145">INPUTS</span></span>

### <span data-ttu-id="6bee6-146">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6bee6-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6bee6-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6bee6-147">System.String</span></span>

### <span data-ttu-id="6bee6-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementparameter []</span><span class="sxs-lookup"><span data-stu-id="6bee6-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="6bee6-149">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementrequest</span><span class="sxs-lookup"><span data-stu-id="6bee6-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="6bee6-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementresponse []</span><span class="sxs-lookup"><span data-stu-id="6bee6-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="6bee6-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6bee6-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6bee6-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bee6-152">OUTPUTS</span></span>

### <span data-ttu-id="6bee6-153">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="6bee6-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="6bee6-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bee6-154">NOTES</span></span>

## <span data-ttu-id="6bee6-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bee6-155">RELATED LINKS</span></span>

[<span data-ttu-id="6bee6-156">Get-Azapsananatomentoperation</span><span class="sxs-lookup"><span data-stu-id="6bee6-156">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="6bee6-157">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="6bee6-157">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="6bee6-158">Remove-Azapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="6bee6-158">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


