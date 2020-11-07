---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: 0e5764ec40c05c6894715e718926714a4cbc7070
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753406"
---
# <span data-ttu-id="e4906-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="e4906-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="e4906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4906-102">SYNOPSIS</span></span>
<span data-ttu-id="e4906-103">API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e4906-103">Sets API operation details.</span></span>

## <span data-ttu-id="e4906-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4906-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4906-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4906-105">DESCRIPTION</span></span>
<span data-ttu-id="e4906-106">**Set-Azapsananagementoperation** CMDLET 'i API işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e4906-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="e4906-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4906-107">EXAMPLES</span></span>

### <span data-ttu-id="e4906-108">Örnek 1: işlem ayrıntılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4906-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="e4906-109">Bu komut API yönetimi için işlem ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e4906-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="e4906-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4906-110">PARAMETERS</span></span>

### <span data-ttu-id="e4906-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="e4906-111">-ApiId</span></span>
<span data-ttu-id="e4906-112">API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="e4906-113">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="e4906-113">-ApiRevision</span></span>
<span data-ttu-id="e4906-114">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="e4906-114">Identifier of API Revision.</span></span> <span data-ttu-id="e4906-115">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e4906-115">This parameter is optional.</span></span> <span data-ttu-id="e4906-116">Belirtilmezse, işlem geçerli API düzeltmesinde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e4906-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="e4906-117">-Context</span><span class="sxs-lookup"><span data-stu-id="e4906-117">-Context</span></span>
<span data-ttu-id="e4906-118">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="e4906-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4906-119">-DefaultProfile</span></span>
<span data-ttu-id="e4906-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4906-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4906-121">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e4906-121">-Description</span></span>
<span data-ttu-id="e4906-122">Yeni işlemin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="e4906-123">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="e4906-123">-Method</span></span>
<span data-ttu-id="e4906-124">Yeni işlemin HTTP yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="e4906-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4906-125">-Name</span></span>
<span data-ttu-id="e4906-126">Yeni işlemin görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="e4906-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e4906-127">-OperationId</span></span>
<span data-ttu-id="e4906-128">Var olan işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="e4906-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e4906-129">-PassThru</span></span>
<span data-ttu-id="e4906-130">geçiş</span><span class="sxs-lookup"><span data-stu-id="e4906-130">passthru</span></span>

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

### <span data-ttu-id="e4906-131">-İstek</span><span class="sxs-lookup"><span data-stu-id="e4906-131">-Request</span></span>
<span data-ttu-id="e4906-132">İşlem isteği ayrıntılarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="e4906-133">-Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="e4906-133">-Responses</span></span>
<span data-ttu-id="e4906-134">Olası işlem yanıtlarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="e4906-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="e4906-135">-TemplateParameters</span></span>
<span data-ttu-id="e4906-136">Parametre *URL 'Si şablonunda* tanımlanan bir dizi veya parametre belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="e4906-137">Bir değer belirtmezseniz, UrlTemplate temel alınarak varsayılan bir değer oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e4906-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="e4906-138">Açıklama, tür ve diğer olası değerler gibi parametrelerle ilgili daha fazla ayrıntı vermek için parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="e4906-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="e4906-139">-Urlşablonu</span><span class="sxs-lookup"><span data-stu-id="e4906-139">-UrlTemplate</span></span>
<span data-ttu-id="e4906-140">URL şablonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4906-140">Specifies the URL template.</span></span>
<span data-ttu-id="e4906-141">Örneğin: müşteriler/{CID}/siparişler/{OID}/? tarih = {Date}.</span><span class="sxs-lookup"><span data-stu-id="e4906-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="e4906-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4906-142">-Confirm</span></span>
<span data-ttu-id="e4906-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4906-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4906-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4906-144">-WhatIf</span></span>
<span data-ttu-id="e4906-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4906-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4906-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4906-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4906-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4906-147">CommonParameters</span></span>
<span data-ttu-id="e4906-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4906-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4906-149">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e4906-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4906-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4906-150">INPUTS</span></span>

### <span data-ttu-id="e4906-151">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e4906-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e4906-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e4906-152">System.String</span></span>

### <span data-ttu-id="e4906-153">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementparameter []</span><span class="sxs-lookup"><span data-stu-id="e4906-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="e4906-154">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementrequest</span><span class="sxs-lookup"><span data-stu-id="e4906-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="e4906-155">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementresponse []</span><span class="sxs-lookup"><span data-stu-id="e4906-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="e4906-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e4906-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e4906-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4906-157">OUTPUTS</span></span>

### <span data-ttu-id="e4906-158">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="e4906-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="e4906-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4906-159">NOTES</span></span>

## <span data-ttu-id="e4906-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4906-160">RELATED LINKS</span></span>

[<span data-ttu-id="e4906-161">Get-Azapsananatomentoperation</span><span class="sxs-lookup"><span data-stu-id="e4906-161">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="e4906-162">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="e4906-162">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="e4906-163">Remove-Azapsananagementoperation</span><span class="sxs-lookup"><span data-stu-id="e4906-163">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


