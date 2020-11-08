---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103862"
---
# <span data-ttu-id="fdea9-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="fdea9-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="fdea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdea9-102">SYNOPSIS</span></span>
<span data-ttu-id="fdea9-103">API yönetim bağlamında ayarlanan bir API sürümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fdea9-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="fdea9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fdea9-104">SYNTAX</span></span>

### <span data-ttu-id="fdea9-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fdea9-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdea9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fdea9-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdea9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fdea9-107">DESCRIPTION</span></span>

<span data-ttu-id="fdea9-108">**Set-Azapsananagementapiversionset** cmdlet 'ı Azure API yönetim API sürümü kümesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fdea9-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="fdea9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fdea9-109">EXAMPLES</span></span>

### <span data-ttu-id="fdea9-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fdea9-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="fdea9-111">Bu komut, sürüm oluşturma düzeni `Header` ve üst bilgi parametresiyle var olan BIR API sürüm kümesini güncelleştirir `api-version` .</span><span class="sxs-lookup"><span data-stu-id="fdea9-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="fdea9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fdea9-112">PARAMETERS</span></span>

### <span data-ttu-id="fdea9-113">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="fdea9-113">-ApiVersionSetId</span></span>
<span data-ttu-id="fdea9-114">Yeni API sürüm kümesi için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="fdea9-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="fdea9-115">-Context</span><span class="sxs-lookup"><span data-stu-id="fdea9-115">-Context</span></span>
<span data-ttu-id="fdea9-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="fdea9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fdea9-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fdea9-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdea9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdea9-118">-DefaultProfile</span></span>
<span data-ttu-id="fdea9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fdea9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdea9-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="fdea9-120">-Description</span></span>
<span data-ttu-id="fdea9-121">API sürüm kümesinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="fdea9-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="fdea9-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="fdea9-122">-HeaderName</span></span>
<span data-ttu-id="fdea9-123">Sürüm bilgilerini içerecek üst bilgi değeri.</span><span class="sxs-lookup"><span data-stu-id="fdea9-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="fdea9-124">Sürüm oluşturma düzeni üst BILGISI seçilirse, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fdea9-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="fdea9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdea9-125">-InputObject</span></span>
<span data-ttu-id="fdea9-126">Psapimanagementapıversionset 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="fdea9-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="fdea9-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fdea9-127">This parameter is required.</span></span>

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

### <span data-ttu-id="fdea9-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="fdea9-128">-Name</span></span>
<span data-ttu-id="fdea9-129">Apıversion kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="fdea9-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="fdea9-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fdea9-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="fdea9-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fdea9-131">-PassThru</span></span>
<span data-ttu-id="fdea9-132">Bu örnekte, değiştirilmiş Apıversionset 'i temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. modellerinin</span><span class="sxs-lookup"><span data-stu-id="fdea9-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="fdea9-133">-SorguAdı</span><span class="sxs-lookup"><span data-stu-id="fdea9-133">-QueryName</span></span>
<span data-ttu-id="fdea9-134">Sürüm bilgilerini içerecek olan sorgu değeri.</span><span class="sxs-lookup"><span data-stu-id="fdea9-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="fdea9-135">Sürüm oluşturma düzeni sorgusu seçilirse, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="fdea9-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="fdea9-136">-Düzen</span><span class="sxs-lookup"><span data-stu-id="fdea9-136">-Scheme</span></span>
<span data-ttu-id="fdea9-137">API sürüm oluşturma kümesini seçmek için sürüm oluşturma düzeni.</span><span class="sxs-lookup"><span data-stu-id="fdea9-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="fdea9-138">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fdea9-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="fdea9-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="fdea9-139">-Confirm</span></span>
<span data-ttu-id="fdea9-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fdea9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdea9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdea9-141">-WhatIf</span></span>
<span data-ttu-id="fdea9-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fdea9-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdea9-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fdea9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdea9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdea9-144">CommonParameters</span></span>
<span data-ttu-id="fdea9-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fdea9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdea9-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fdea9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdea9-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fdea9-147">INPUTS</span></span>

### <span data-ttu-id="fdea9-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="fdea9-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fdea9-149">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="fdea9-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="fdea9-150">System. String</span><span class="sxs-lookup"><span data-stu-id="fdea9-150">System.String</span></span>

### <span data-ttu-id="fdea9-151">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementversioningscheme</span><span class="sxs-lookup"><span data-stu-id="fdea9-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="fdea9-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fdea9-152">OUTPUTS</span></span>

### <span data-ttu-id="fdea9-153">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="fdea9-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="fdea9-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fdea9-154">NOTES</span></span>

## <span data-ttu-id="fdea9-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fdea9-155">RELATED LINKS</span></span>

[<span data-ttu-id="fdea9-156">Get-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="fdea9-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="fdea9-157">New-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="fdea9-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="fdea9-158">Set-Azapsananagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="fdea9-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
