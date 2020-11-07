---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 95444b74b3d62dd187a701e2305df2e241ff236f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753545"
---
# <span data-ttu-id="703b3-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="703b3-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="703b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="703b3-102">SYNOPSIS</span></span>
<span data-ttu-id="703b3-103">API sürüm kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="703b3-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="703b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="703b3-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="703b3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="703b3-105">DESCRIPTION</span></span>
<span data-ttu-id="703b3-106">**Yeni-Azapsananagementapiversionset** cmdlet 'ı Azure API yönetim BAĞLAMıNDA bir API sürüm kümesi varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="703b3-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="703b3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="703b3-107">EXAMPLES</span></span>

### <span data-ttu-id="703b3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="703b3-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="703b3-109">Bu komut, sürüm oluşturma düzenini ve sorgu parametresini hangi API sürümü kümesi oluşturur `Query` `api-version` .</span><span class="sxs-lookup"><span data-stu-id="703b3-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="703b3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="703b3-110">PARAMETERS</span></span>

### <span data-ttu-id="703b3-111">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="703b3-111">-ApiVersionSetId</span></span>
<span data-ttu-id="703b3-112">Yeni API sürüm kümesi için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="703b3-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="703b3-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="703b3-113">This parameter is optional.</span></span>
<span data-ttu-id="703b3-114">Belirtilmezse, tanımlayıcı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="703b3-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="703b3-115">-Context</span><span class="sxs-lookup"><span data-stu-id="703b3-115">-Context</span></span>
<span data-ttu-id="703b3-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="703b3-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="703b3-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="703b3-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="703b3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="703b3-118">-DefaultProfile</span></span>
<span data-ttu-id="703b3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="703b3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="703b3-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="703b3-120">-Description</span></span>
<span data-ttu-id="703b3-121">API sürüm kümesinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="703b3-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="703b3-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="703b3-122">-HeaderName</span></span>
<span data-ttu-id="703b3-123">Sürüm bilgilerini içerecek üst bilgi değeri.</span><span class="sxs-lookup"><span data-stu-id="703b3-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="703b3-124">Sürüm oluşturma düzeni üst BILGISI seçilirse, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="703b3-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="703b3-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="703b3-125">-Name</span></span>
<span data-ttu-id="703b3-126">Apıversion kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="703b3-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="703b3-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="703b3-127">This parameter is required.</span></span>

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

### <span data-ttu-id="703b3-128">-SorguAdı</span><span class="sxs-lookup"><span data-stu-id="703b3-128">-QueryName</span></span>
<span data-ttu-id="703b3-129">Sürüm bilgilerini içerecek olan sorgu değeri.</span><span class="sxs-lookup"><span data-stu-id="703b3-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="703b3-130">Sürüm oluşturma düzeni sorgusu seçilirse, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="703b3-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="703b3-131">-Düzen</span><span class="sxs-lookup"><span data-stu-id="703b3-131">-Scheme</span></span>
<span data-ttu-id="703b3-132">API sürüm oluşturma kümesini seçmek için sürüm oluşturma düzeni.</span><span class="sxs-lookup"><span data-stu-id="703b3-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="703b3-133">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="703b3-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="703b3-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="703b3-134">-Confirm</span></span>
<span data-ttu-id="703b3-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="703b3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="703b3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="703b3-136">-WhatIf</span></span>
<span data-ttu-id="703b3-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="703b3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="703b3-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="703b3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="703b3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="703b3-139">CommonParameters</span></span>
<span data-ttu-id="703b3-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="703b3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="703b3-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="703b3-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="703b3-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="703b3-142">INPUTS</span></span>

### <span data-ttu-id="703b3-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="703b3-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="703b3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="703b3-144">System.String</span></span>

### <span data-ttu-id="703b3-145">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementversioningscheme</span><span class="sxs-lookup"><span data-stu-id="703b3-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="703b3-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="703b3-146">OUTPUTS</span></span>

### <span data-ttu-id="703b3-147">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="703b3-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="703b3-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="703b3-148">NOTES</span></span>

## <span data-ttu-id="703b3-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="703b3-149">RELATED LINKS</span></span>

[<span data-ttu-id="703b3-150">Get-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="703b3-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="703b3-151">Remove-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="703b3-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="703b3-152">Set-Azapsananagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="703b3-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)