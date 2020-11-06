---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: e50e912c55a09ef5d036bee668bc45f58fc42c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587339"
---
# <span data-ttu-id="bd459-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bd459-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="bd459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd459-102">SYNOPSIS</span></span>
<span data-ttu-id="bd459-103">API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bd459-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd459-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd459-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd459-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd459-105">DESCRIPTION</span></span>
<span data-ttu-id="bd459-106">**Set-Azurermapımanagementoperation** CMDLET 'i API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bd459-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="bd459-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd459-107">EXAMPLES</span></span>

### <span data-ttu-id="bd459-108">Örnek 1: işlem ayrıntılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="bd459-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="bd459-109">Bu komut API yönetimi için işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bd459-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="bd459-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd459-110">PARAMETERS</span></span>

### <span data-ttu-id="bd459-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="bd459-111">-ApiId</span></span>
<span data-ttu-id="bd459-112">API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="bd459-113">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="bd459-113">-ApiRevision</span></span>
<span data-ttu-id="bd459-114">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="bd459-114">Identifier of API Revision.</span></span> <span data-ttu-id="bd459-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="bd459-115">This parameter is optional.</span></span> <span data-ttu-id="bd459-116">Belirtilmezse, işlem geçerli API düzeltmesinde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bd459-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="bd459-117">-Context</span><span class="sxs-lookup"><span data-stu-id="bd459-117">-Context</span></span>
<span data-ttu-id="bd459-118">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="bd459-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd459-119">-DefaultProfile</span></span>
<span data-ttu-id="bd459-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd459-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd459-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="bd459-121">-Description</span></span>
<span data-ttu-id="bd459-122">Yeni işlemin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="bd459-123">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="bd459-123">-Method</span></span>
<span data-ttu-id="bd459-124">Yeni işlemin HTTP yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="bd459-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd459-125">-Name</span></span>
<span data-ttu-id="bd459-126">Yeni işlemin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="bd459-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bd459-127">-OperationId</span></span>
<span data-ttu-id="bd459-128">Var olan işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="bd459-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bd459-129">-PassThru</span></span>
<span data-ttu-id="bd459-130">geçiş</span><span class="sxs-lookup"><span data-stu-id="bd459-130">passthru</span></span>

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

### <span data-ttu-id="bd459-131">-İstek</span><span class="sxs-lookup"><span data-stu-id="bd459-131">-Request</span></span>
<span data-ttu-id="bd459-132">İşlem isteği ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="bd459-133">-Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="bd459-133">-Responses</span></span>
<span data-ttu-id="bd459-134">Olası işlem yanıtlarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="bd459-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="bd459-135">-TemplateParameters</span></span>
<span data-ttu-id="bd459-136">Parametre *URL 'Si şablonunda* tanımlanan bir dizi veya parametre belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="bd459-137">Bir değer belirtmezseniz, UrlTemplate temel alınarak varsayılan bir değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bd459-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="bd459-138">Açıklama, tür ve diğer olası değerler gibi parametrelerle ilgili daha fazla ayrıntı vermek için parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="bd459-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="bd459-139">-Urlşablonu</span><span class="sxs-lookup"><span data-stu-id="bd459-139">-UrlTemplate</span></span>
<span data-ttu-id="bd459-140">URL şablonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd459-140">Specifies the URL template.</span></span>
<span data-ttu-id="bd459-141">Örneğin: müşteriler/{CID}/siparişler/{OID}/? tarih = {Date}.</span><span class="sxs-lookup"><span data-stu-id="bd459-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="bd459-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd459-142">CommonParameters</span></span>
<span data-ttu-id="bd459-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd459-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd459-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd459-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd459-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd459-145">INPUTS</span></span>

### <span data-ttu-id="bd459-146">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="bd459-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bd459-147">System. String</span><span class="sxs-lookup"><span data-stu-id="bd459-147">System.String</span></span>

### <span data-ttu-id="bd459-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementparameter []</span><span class="sxs-lookup"><span data-stu-id="bd459-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="bd459-149">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementrequest</span><span class="sxs-lookup"><span data-stu-id="bd459-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="bd459-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementresponse []</span><span class="sxs-lookup"><span data-stu-id="bd459-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="bd459-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bd459-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bd459-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd459-152">OUTPUTS</span></span>

### <span data-ttu-id="bd459-153">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="bd459-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="bd459-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd459-154">NOTES</span></span>

## <span data-ttu-id="bd459-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd459-155">RELATED LINKS</span></span>

[<span data-ttu-id="bd459-156">Get-Azurermapsananama</span><span class="sxs-lookup"><span data-stu-id="bd459-156">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="bd459-157">Yeni-Azurermapsananaks</span><span class="sxs-lookup"><span data-stu-id="bd459-157">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="bd459-158">Remove-Azurermapımanagementoperation</span><span class="sxs-lookup"><span data-stu-id="bd459-158">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


