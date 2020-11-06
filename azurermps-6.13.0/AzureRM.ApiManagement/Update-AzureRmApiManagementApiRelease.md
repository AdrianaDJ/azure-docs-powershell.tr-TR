---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 5b863c0d0c808c8cb993e4f78f9767d13fb634d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587323"
---
# <span data-ttu-id="a27a0-101">Update-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a27a0-101">Update-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="a27a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a27a0-102">SYNOPSIS</span></span>
<span data-ttu-id="a27a0-103">Belirli bir API sürümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a27a0-103">Updates a particular Api Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a27a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a27a0-104">SYNTAX</span></span>

### <span data-ttu-id="a27a0-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a27a0-105">ExpandedParameter (Default)</span></span>
```
Update-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a27a0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a27a0-106">ByInputObject</span></span>
```
Update-AzureRmApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a27a0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a27a0-107">DESCRIPTION</span></span>
<span data-ttu-id="a27a0-108">**Update-Azurermapımanagementapirelease** cmdlet 'ı BIR Azure API yönetimi API sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a27a0-108">The **Update-AzureRmApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="a27a0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a27a0-109">EXAMPLES</span></span>

### <span data-ttu-id="a27a0-110">Örnek 1: bir API düzeltmesi için API sürümünü güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a27a0-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="a27a0-111">Bu komut, `echo-api-release` API 'nin API sürümünü `echo-api` Yeni notla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a27a0-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="a27a0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a27a0-112">PARAMETERS</span></span>

### <span data-ttu-id="a27a0-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="a27a0-113">-ApiId</span></span>
<span data-ttu-id="a27a0-114">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a27a0-114">Identifier of existing API.</span></span>
<span data-ttu-id="a27a0-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a27a0-115">This parameter is required.</span></span>

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

### <span data-ttu-id="a27a0-116">-Context</span><span class="sxs-lookup"><span data-stu-id="a27a0-116">-Context</span></span>
<span data-ttu-id="a27a0-117">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="a27a0-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a27a0-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a27a0-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a27a0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27a0-119">-DefaultProfile</span></span>
<span data-ttu-id="a27a0-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a27a0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a27a0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a27a0-121">-InputObject</span></span>
<span data-ttu-id="a27a0-122">Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapimanagementapırelease türünün örneği.</span><span class="sxs-lookup"><span data-stu-id="a27a0-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a27a0-123">Not</span><span class="sxs-lookup"><span data-stu-id="a27a0-123">-Note</span></span>
<span data-ttu-id="a27a0-124">API sürüm notları.</span><span class="sxs-lookup"><span data-stu-id="a27a0-124">Api Release Notes.</span></span>
<span data-ttu-id="a27a0-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="a27a0-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="a27a0-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a27a0-126">-PassThru</span></span>
<span data-ttu-id="a27a0-127">Belirtildiyse, set API yayımını temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapimanagementapırelease türü.</span><span class="sxs-lookup"><span data-stu-id="a27a0-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="a27a0-128">-ReleaseID</span><span class="sxs-lookup"><span data-stu-id="a27a0-128">-ReleaseId</span></span>
<span data-ttu-id="a27a0-129">API düzeltmesi ReleaseID tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a27a0-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="a27a0-130">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a27a0-130">This parameter is required.</span></span>

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

### <span data-ttu-id="a27a0-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a27a0-131">-Confirm</span></span>
<span data-ttu-id="a27a0-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a27a0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a27a0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a27a0-133">-WhatIf</span></span>
<span data-ttu-id="a27a0-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a27a0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a27a0-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a27a0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a27a0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27a0-136">CommonParameters</span></span>
<span data-ttu-id="a27a0-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a27a0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27a0-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a27a0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27a0-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a27a0-139">INPUTS</span></span>

### <span data-ttu-id="a27a0-140">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="a27a0-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="a27a0-141">Parametreler: bağlam (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a27a0-141">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="a27a0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a27a0-142">System.String</span></span>

### <span data-ttu-id="a27a0-143">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="a27a0-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a27a0-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a27a0-144">OUTPUTS</span></span>

### <span data-ttu-id="a27a0-145">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="a27a0-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a27a0-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a27a0-146">NOTES</span></span>

## <span data-ttu-id="a27a0-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a27a0-147">RELATED LINKS</span></span>

[<span data-ttu-id="a27a0-148">Get-Azurermapımanagementapirelease</span><span class="sxs-lookup"><span data-stu-id="a27a0-148">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="a27a0-149">Yeni-Azurermapımanagementapirelease</span><span class="sxs-lookup"><span data-stu-id="a27a0-149">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)
