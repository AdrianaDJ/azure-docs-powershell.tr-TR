---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110112"
---
# <span data-ttu-id="afc67-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="afc67-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="afc67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afc67-102">SYNOPSIS</span></span>
<span data-ttu-id="afc67-103">API yönetim bağlamında ayarlanan bir API sürümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="afc67-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="afc67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afc67-104">SYNTAX</span></span>

### <span data-ttu-id="afc67-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="afc67-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afc67-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="afc67-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afc67-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="afc67-107">DESCRIPTION</span></span>

<span data-ttu-id="afc67-108">**Set-Azapsananagementapiversionset** cmdlet 'ı Azure API yönetim API sürümü kümesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="afc67-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="afc67-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afc67-109">EXAMPLES</span></span>

### <span data-ttu-id="afc67-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="afc67-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="afc67-111">Bu komut, sürüm oluşturma düzeni `Header` ve üst bilgi parametresiyle var olan BIR API sürüm kümesini güncelleştirir `api-version` .</span><span class="sxs-lookup"><span data-stu-id="afc67-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="afc67-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afc67-112">PARAMETERS</span></span>

### <span data-ttu-id="afc67-113">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="afc67-113">-ApiVersionSetId</span></span>
<span data-ttu-id="afc67-114">Yeni API sürüm kümesi için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="afc67-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="afc67-115">-Context</span><span class="sxs-lookup"><span data-stu-id="afc67-115">-Context</span></span>
<span data-ttu-id="afc67-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="afc67-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="afc67-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="afc67-117">This parameter is required.</span></span>

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

### <span data-ttu-id="afc67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc67-118">-DefaultProfile</span></span>
<span data-ttu-id="afc67-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afc67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afc67-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="afc67-120">-Description</span></span>
<span data-ttu-id="afc67-121">API sürüm kümesinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="afc67-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="afc67-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="afc67-122">-HeaderName</span></span>
<span data-ttu-id="afc67-123">Sürüm bilgilerini içerecek üst bilgi değeri.</span><span class="sxs-lookup"><span data-stu-id="afc67-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="afc67-124">Sürüm oluşturma düzeni üst BILGISI seçilirse, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="afc67-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="afc67-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afc67-125">-InputObject</span></span>
<span data-ttu-id="afc67-126">Psapimanagementapıversionset 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="afc67-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="afc67-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="afc67-127">This parameter is required.</span></span>

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

### <span data-ttu-id="afc67-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="afc67-128">-Name</span></span>
<span data-ttu-id="afc67-129">Apıversion kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="afc67-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="afc67-130">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="afc67-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="afc67-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="afc67-131">-PassThru</span></span>
<span data-ttu-id="afc67-132">Bu örnekte, değiştirilmiş Apıversionset 'i temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. modellerinin</span><span class="sxs-lookup"><span data-stu-id="afc67-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="afc67-133">-SorguAdı</span><span class="sxs-lookup"><span data-stu-id="afc67-133">-QueryName</span></span>
<span data-ttu-id="afc67-134">Sürüm bilgilerini içerecek olan sorgu değeri.</span><span class="sxs-lookup"><span data-stu-id="afc67-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="afc67-135">Sürüm oluşturma düzeni sorgusu seçilirse, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="afc67-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="afc67-136">-Düzen</span><span class="sxs-lookup"><span data-stu-id="afc67-136">-Scheme</span></span>
<span data-ttu-id="afc67-137">API sürüm oluşturma kümesini seçmek için sürüm oluşturma düzeni.</span><span class="sxs-lookup"><span data-stu-id="afc67-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="afc67-138">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="afc67-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="afc67-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="afc67-139">-Confirm</span></span>
<span data-ttu-id="afc67-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="afc67-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc67-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc67-141">-WhatIf</span></span>
<span data-ttu-id="afc67-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="afc67-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afc67-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="afc67-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc67-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc67-144">CommonParameters</span></span>
<span data-ttu-id="afc67-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afc67-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc67-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="afc67-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc67-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afc67-147">INPUTS</span></span>

### <span data-ttu-id="afc67-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="afc67-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="afc67-149">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="afc67-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="afc67-150">System. String</span><span class="sxs-lookup"><span data-stu-id="afc67-150">System.String</span></span>

### <span data-ttu-id="afc67-151">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementversioningscheme</span><span class="sxs-lookup"><span data-stu-id="afc67-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="afc67-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afc67-152">OUTPUTS</span></span>

### <span data-ttu-id="afc67-153">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="afc67-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="afc67-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afc67-154">NOTES</span></span>

## <span data-ttu-id="afc67-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afc67-155">RELATED LINKS</span></span>

[<span data-ttu-id="afc67-156">Get-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="afc67-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="afc67-157">New-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="afc67-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="afc67-158">Set-Azapsananagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="afc67-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
