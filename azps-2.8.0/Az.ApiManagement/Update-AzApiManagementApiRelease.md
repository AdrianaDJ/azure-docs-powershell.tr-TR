---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 1141d671db13c3ea44a7ed7bd003574f3c13615c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753396"
---
# <span data-ttu-id="64d1f-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="64d1f-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="64d1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="64d1f-103">Belirli bir API sürümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="64d1f-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="64d1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64d1f-104">SYNTAX</span></span>

### <span data-ttu-id="64d1f-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="64d1f-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64d1f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="64d1f-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64d1f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="64d1f-107">DESCRIPTION</span></span>
<span data-ttu-id="64d1f-108">**Update-Azapsananagementapırelease** cmdlet 'ı BIR Azure API yönetimi API sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="64d1f-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="64d1f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64d1f-109">EXAMPLES</span></span>

### <span data-ttu-id="64d1f-110">Örnek 1: bir API düzeltmesi için API sürümünü güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="64d1f-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="64d1f-111">Bu komut, `echo-api-release` API 'nin API sürümünü `echo-api` Yeni notla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="64d1f-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="64d1f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64d1f-112">PARAMETERS</span></span>

### <span data-ttu-id="64d1f-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="64d1f-113">-ApiId</span></span>
<span data-ttu-id="64d1f-114">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="64d1f-114">Identifier of existing API.</span></span>
<span data-ttu-id="64d1f-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="64d1f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="64d1f-116">-Context</span><span class="sxs-lookup"><span data-stu-id="64d1f-116">-Context</span></span>
<span data-ttu-id="64d1f-117">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="64d1f-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="64d1f-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="64d1f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="64d1f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d1f-119">-DefaultProfile</span></span>
<span data-ttu-id="64d1f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64d1f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64d1f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64d1f-121">-InputObject</span></span>
<span data-ttu-id="64d1f-122">Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapimanagementapırelease türünün örneği.</span><span class="sxs-lookup"><span data-stu-id="64d1f-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="64d1f-123">Not</span><span class="sxs-lookup"><span data-stu-id="64d1f-123">-Note</span></span>
<span data-ttu-id="64d1f-124">API sürüm notları.</span><span class="sxs-lookup"><span data-stu-id="64d1f-124">Api Release Notes.</span></span>
<span data-ttu-id="64d1f-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="64d1f-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="64d1f-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="64d1f-126">-PassThru</span></span>
<span data-ttu-id="64d1f-127">Belirtildiyse, set API yayımını temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapimanagementapırelease türü.</span><span class="sxs-lookup"><span data-stu-id="64d1f-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="64d1f-128">-ReleaseID</span><span class="sxs-lookup"><span data-stu-id="64d1f-128">-ReleaseId</span></span>
<span data-ttu-id="64d1f-129">API düzeltmesi ReleaseID tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="64d1f-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="64d1f-130">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="64d1f-130">This parameter is required.</span></span>

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

### <span data-ttu-id="64d1f-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="64d1f-131">-Confirm</span></span>
<span data-ttu-id="64d1f-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="64d1f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64d1f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d1f-133">-WhatIf</span></span>
<span data-ttu-id="64d1f-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="64d1f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64d1f-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="64d1f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64d1f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d1f-136">CommonParameters</span></span>
<span data-ttu-id="64d1f-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64d1f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d1f-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="64d1f-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d1f-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64d1f-139">INPUTS</span></span>

### <span data-ttu-id="64d1f-140">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="64d1f-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="64d1f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="64d1f-141">System.String</span></span>

### <span data-ttu-id="64d1f-142">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="64d1f-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="64d1f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64d1f-143">OUTPUTS</span></span>

### <span data-ttu-id="64d1f-144">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapirelease</span><span class="sxs-lookup"><span data-stu-id="64d1f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="64d1f-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64d1f-145">NOTES</span></span>

## <span data-ttu-id="64d1f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64d1f-146">RELATED LINKS</span></span>

[<span data-ttu-id="64d1f-147">Get-Azapimpırelease</span><span class="sxs-lookup"><span data-stu-id="64d1f-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="64d1f-148">Yeni-Azapimpırelease</span><span class="sxs-lookup"><span data-stu-id="64d1f-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
