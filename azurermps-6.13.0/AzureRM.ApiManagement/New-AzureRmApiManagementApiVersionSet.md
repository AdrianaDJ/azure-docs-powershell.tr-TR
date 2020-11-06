---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: e10b91994bdb7351a7154d04cb7de3231ed87a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588648"
---
# <span data-ttu-id="1f7e0-101">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1f7e0-101">New-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1f7e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7e0-103">API sürüm kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-103">Creates an API Version Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f7e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f7e0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>]
 -Name <String> -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f7e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f7e0-105">DESCRIPTION</span></span>
<span data-ttu-id="1f7e0-106">**Yeni-Azurermapımanagementapiversionset** cmdlet 'ı Azure API yönetim BAĞLAMıNDA bir API sürüm kümesi varlığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-106">The **New-AzureRmApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="1f7e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f7e0-107">EXAMPLES</span></span>

### <span data-ttu-id="1f7e0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f7e0-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzureRmApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

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

<span data-ttu-id="1f7e0-109">Bu komut, sürüm oluşturma düzenini ve sorgu parametresini hangi API sürümü kümesi oluşturur `Query` `api-version` .</span><span class="sxs-lookup"><span data-stu-id="1f7e0-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="1f7e0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f7e0-110">PARAMETERS</span></span>

### <span data-ttu-id="1f7e0-111">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="1f7e0-111">-ApiVersionSetId</span></span>
<span data-ttu-id="1f7e0-112">Yeni API sürüm kümesi için tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="1f7e0-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-113">This parameter is optional.</span></span>
<span data-ttu-id="1f7e0-114">Belirtilmezse, tanımlayıcı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="1f7e0-115">-Context</span><span class="sxs-lookup"><span data-stu-id="1f7e0-115">-Context</span></span>
<span data-ttu-id="1f7e0-116">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1f7e0-117">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-117">This parameter is required.</span></span>

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

### <span data-ttu-id="1f7e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7e0-118">-DefaultProfile</span></span>
<span data-ttu-id="1f7e0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f7e0-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="1f7e0-120">-Description</span></span>
<span data-ttu-id="1f7e0-121">API sürüm kümesinin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="1f7e0-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="1f7e0-122">-HeaderName</span></span>
<span data-ttu-id="1f7e0-123">Sürüm bilgilerini içerecek üst bilgi değeri.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="1f7e0-124">Sürüm oluşturma düzeni üst bilgisinde, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-124">If versioning Scheme HEADER is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="1f7e0-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f7e0-125">-Name</span></span>
<span data-ttu-id="1f7e0-126">Apıversion kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="1f7e0-127">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-127">This parameter is required.</span></span>

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

### <span data-ttu-id="1f7e0-128">-SorguAdı</span><span class="sxs-lookup"><span data-stu-id="1f7e0-128">-QueryName</span></span>
<span data-ttu-id="1f7e0-129">Sürüm bilgilerini içerecek olan sorgu değeri.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="1f7e0-130">Sürüm oluşturma düzeni sorgusu gerekliyse, bu değer belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-130">If versioning Scheme Query is choosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="1f7e0-131">-Düzen</span><span class="sxs-lookup"><span data-stu-id="1f7e0-131">-Scheme</span></span>
<span data-ttu-id="1f7e0-132">API sürüm oluşturma kümesini seçmek için sürüm oluşturma düzeni.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="1f7e0-133">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-133">This parameter is required.</span></span>

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

### <span data-ttu-id="1f7e0-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f7e0-134">-Confirm</span></span>
<span data-ttu-id="1f7e0-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f7e0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f7e0-136">-WhatIf</span></span>
<span data-ttu-id="1f7e0-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f7e0-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f7e0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7e0-139">CommonParameters</span></span>
<span data-ttu-id="1f7e0-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f7e0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7e0-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7e0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7e0-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f7e0-142">INPUTS</span></span>

### <span data-ttu-id="1f7e0-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="1f7e0-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="1f7e0-144">Parametreler: bağlam (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1f7e0-144">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="1f7e0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1f7e0-145">System.String</span></span>

### <span data-ttu-id="1f7e0-146">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementversioningscheme</span><span class="sxs-lookup"><span data-stu-id="1f7e0-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="1f7e0-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f7e0-147">OUTPUTS</span></span>

### <span data-ttu-id="1f7e0-148">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="1f7e0-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1f7e0-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f7e0-149">NOTES</span></span>

## <span data-ttu-id="1f7e0-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f7e0-150">RELATED LINKS</span></span>

[<span data-ttu-id="1f7e0-151">Get-Azurermapımanagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="1f7e0-151">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="1f7e0-152">Remove-Azurermapımanagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="1f7e0-152">Remove-AzureRmApiManagementApiVersionSet</span></span>](./Remove-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="1f7e0-153">Set-Azurermapımanagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="1f7e0-153">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
