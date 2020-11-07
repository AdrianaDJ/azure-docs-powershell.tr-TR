---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58f9fda87bc24b22a68e98d60092b80002e74e4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751122"
---
# <span data-ttu-id="60265-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="60265-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="60265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60265-102">SYNOPSIS</span></span>
<span data-ttu-id="60265-103">API sürüm kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60265-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="60265-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60265-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60265-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="60265-105">DESCRIPTION</span></span>
<span data-ttu-id="60265-106">**Yeni-Azapsananagementapiversionset** cmdlet 'ı Azure API yönetim BAĞLAMıNDA bir API sürüm kümesi varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="60265-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="60265-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60265-107">EXAMPLES</span></span>

### <span data-ttu-id="60265-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="60265-108">Example 1</span></span>
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

<span data-ttu-id="60265-109">Bu komut, sürüm oluşturma düzenini ve sorgu parametresini hangi API sürümü kümesi oluşturur `Query` `api-version` .</span><span class="sxs-lookup"><span data-stu-id="60265-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="60265-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60265-110">PARAMETERS</span></span>

### <span data-ttu-id="60265-111">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="60265-111">-ApiVersionSetId</span></span>
<span data-ttu-id="60265-112">Yeni API sürüm kümesi için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="60265-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="60265-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="60265-113">This parameter is optional.</span></span>
<span data-ttu-id="60265-114">Belirtilmezse, tanımlayıcı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="60265-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="60265-115">-Context</span><span class="sxs-lookup"><span data-stu-id="60265-115">-Context</span></span>
<span data-ttu-id="60265-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="60265-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="60265-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="60265-117">This parameter is required.</span></span>

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

### <span data-ttu-id="60265-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60265-118">-DefaultProfile</span></span>
<span data-ttu-id="60265-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60265-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60265-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="60265-120">-Description</span></span>
<span data-ttu-id="60265-121">API sürüm kümesinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="60265-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="60265-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="60265-122">-HeaderName</span></span>
<span data-ttu-id="60265-123">Sürüm bilgilerini içerecek üst bilgi değeri.</span><span class="sxs-lookup"><span data-stu-id="60265-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="60265-124">Sürüm oluşturma düzeni üst bilgisinde, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="60265-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="60265-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="60265-125">-Name</span></span>
<span data-ttu-id="60265-126">Apıversion kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="60265-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="60265-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="60265-127">This parameter is required.</span></span>

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

### <span data-ttu-id="60265-128">-SorguAdı</span><span class="sxs-lookup"><span data-stu-id="60265-128">-QueryName</span></span>
<span data-ttu-id="60265-129">Sürüm bilgilerini içerecek olan sorgu değeri.</span><span class="sxs-lookup"><span data-stu-id="60265-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="60265-130">Sürüm oluşturma düzeni sorgusu gerekliyse, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="60265-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="60265-131">-Düzen</span><span class="sxs-lookup"><span data-stu-id="60265-131">-Scheme</span></span>
<span data-ttu-id="60265-132">API sürüm oluşturma kümesini seçmek için sürüm oluşturma düzeni.</span><span class="sxs-lookup"><span data-stu-id="60265-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="60265-133">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="60265-133">This parameter is required.</span></span>

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

### <span data-ttu-id="60265-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="60265-134">-Confirm</span></span>
<span data-ttu-id="60265-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="60265-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60265-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60265-136">-WhatIf</span></span>
<span data-ttu-id="60265-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="60265-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60265-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="60265-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60265-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60265-139">CommonParameters</span></span>
<span data-ttu-id="60265-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60265-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60265-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60265-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60265-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60265-142">INPUTS</span></span>

### <span data-ttu-id="60265-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="60265-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="60265-144">System. String</span><span class="sxs-lookup"><span data-stu-id="60265-144">System.String</span></span>

### <span data-ttu-id="60265-145">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementversioningscheme</span><span class="sxs-lookup"><span data-stu-id="60265-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="60265-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60265-146">OUTPUTS</span></span>

### <span data-ttu-id="60265-147">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="60265-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="60265-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60265-148">NOTES</span></span>

## <span data-ttu-id="60265-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60265-149">RELATED LINKS</span></span>

[<span data-ttu-id="60265-150">Get-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="60265-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="60265-151">Remove-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="60265-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="60265-152">Set-Azapsananagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="60265-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)