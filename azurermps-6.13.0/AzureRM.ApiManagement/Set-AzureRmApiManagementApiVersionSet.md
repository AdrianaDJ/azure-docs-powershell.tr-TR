---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 5d9bc89eb2d4188b7b2903bee7a8b0a44bec1216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591459"
---
# <span data-ttu-id="10101-101">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="10101-101">Set-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="10101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10101-102">SYNOPSIS</span></span>
<span data-ttu-id="10101-103">API yönetim bağlamında ayarlanan bir API sürümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="10101-103">Updates an API Version Set in the API Management Context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10101-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="10101-104">SYNTAX</span></span>

### <span data-ttu-id="10101-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="10101-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-Name <String>] [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10101-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="10101-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10101-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="10101-107">DESCRIPTION</span></span>

<span data-ttu-id="10101-108">**Set-Azurermapımanagementapiversionset** cmdlet 'ı Azure API yönetimi API sürüm kümesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="10101-108">The **Set-AzureRmApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="10101-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="10101-109">EXAMPLES</span></span>

### <span data-ttu-id="10101-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="10101-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="10101-111">Bu komut, sürüm oluşturma düzeni `Header` ve üst bilgi parametresiyle var olan BIR API sürüm kümesini güncelleştirir `api-version` .</span><span class="sxs-lookup"><span data-stu-id="10101-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="10101-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="10101-112">PARAMETERS</span></span>

### <span data-ttu-id="10101-113">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="10101-113">-ApiVersionSetId</span></span>
<span data-ttu-id="10101-114">Yeni API sürüm kümesi için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="10101-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10101-115">-Context</span><span class="sxs-lookup"><span data-stu-id="10101-115">-Context</span></span>
<span data-ttu-id="10101-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="10101-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="10101-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="10101-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10101-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10101-118">-DefaultProfile</span></span>
<span data-ttu-id="10101-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="10101-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10101-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="10101-120">-Description</span></span>
<span data-ttu-id="10101-121">API sürüm kümesinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="10101-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="10101-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="10101-122">-HeaderName</span></span>
<span data-ttu-id="10101-123">Sürüm bilgilerini içerecek üst bilgi değeri.</span><span class="sxs-lookup"><span data-stu-id="10101-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="10101-124">Sürüm oluşturma düzeni üst bilgisinde, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="10101-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="10101-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10101-125">-InputObject</span></span>
<span data-ttu-id="10101-126">Psapimanagementapıversionset 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="10101-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="10101-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="10101-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10101-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="10101-128">-Name</span></span>
<span data-ttu-id="10101-129">Apıversion kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="10101-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="10101-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="10101-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="10101-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="10101-131">-PassThru</span></span>
<span data-ttu-id="10101-132">Bu örnekte, değiştirilmiş Apıversionset 'i temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. modellerinin</span><span class="sxs-lookup"><span data-stu-id="10101-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10101-133">-SorguAdı</span><span class="sxs-lookup"><span data-stu-id="10101-133">-QueryName</span></span>
<span data-ttu-id="10101-134">Sürüm bilgilerini içerecek olan sorgu değeri.</span><span class="sxs-lookup"><span data-stu-id="10101-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="10101-135">Sürüm oluşturma düzeni sorgusu gerekliyse, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="10101-135">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="10101-136">-Düzen</span><span class="sxs-lookup"><span data-stu-id="10101-136">-Scheme</span></span>
<span data-ttu-id="10101-137">API sürüm oluşturma kümesini seçmek için sürüm oluşturma düzeni.</span><span class="sxs-lookup"><span data-stu-id="10101-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="10101-138">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="10101-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10101-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="10101-139">-Confirm</span></span>
<span data-ttu-id="10101-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="10101-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10101-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10101-141">-WhatIf</span></span>
<span data-ttu-id="10101-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="10101-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10101-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="10101-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10101-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10101-144">CommonParameters</span></span>
<span data-ttu-id="10101-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="10101-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10101-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10101-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10101-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="10101-147">INPUTS</span></span>

### <span data-ttu-id="10101-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="10101-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="10101-149">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="10101-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="10101-150">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="10101-150">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="10101-151">System. String</span><span class="sxs-lookup"><span data-stu-id="10101-151">System.String</span></span>

### <span data-ttu-id="10101-152">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementversioningscheme</span><span class="sxs-lookup"><span data-stu-id="10101-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="10101-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="10101-153">OUTPUTS</span></span>

### <span data-ttu-id="10101-154">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="10101-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="10101-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="10101-155">NOTES</span></span>

## <span data-ttu-id="10101-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="10101-156">RELATED LINKS</span></span>

[<span data-ttu-id="10101-157">Get-Azurermapımanagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="10101-157">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="10101-158">New-Azurermapımanagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="10101-158">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="10101-159">Set-Azurermapımanagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="10101-159">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)