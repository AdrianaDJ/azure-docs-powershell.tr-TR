---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 03092cf9577bb7b8a35fd0ef69f5d3c94e9c92de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753477"
---
# <span data-ttu-id="fb9b0-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="fb9b0-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="fb9b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9b0-103">Belirli bir API sürüm kümesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="fb9b0-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="fb9b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb9b0-104">SYNTAX</span></span>

### <span data-ttu-id="fb9b0-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb9b0-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9b0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb9b0-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb9b0-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="fb9b0-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb9b0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb9b0-108">DESCRIPTION</span></span>

<span data-ttu-id="fb9b0-109">**Remove-AzAzureRmApiManagementApiVersionSet** cmdlet 'i var olan bir API sürüm kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="fb9b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb9b0-110">EXAMPLES</span></span>

### <span data-ttu-id="fb9b0-111">Örnek 1: API sürüm kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="fb9b0-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="fb9b0-112">Bu komut belirtilen Apıversionsetid ile API sürüm kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="fb9b0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb9b0-113">PARAMETERS</span></span>

### <span data-ttu-id="fb9b0-114">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="fb9b0-114">-ApiVersionSetId</span></span>
<span data-ttu-id="fb9b0-115">API sürüm kümesinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="fb9b0-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-116">This parameter is required.</span></span>

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

### <span data-ttu-id="fb9b0-117">-Context</span><span class="sxs-lookup"><span data-stu-id="fb9b0-117">-Context</span></span>
<span data-ttu-id="fb9b0-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fb9b0-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-119">This parameter is required.</span></span>

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

### <span data-ttu-id="fb9b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9b0-120">-DefaultProfile</span></span>
<span data-ttu-id="fb9b0-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb9b0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb9b0-122">-InputObject</span></span>
<span data-ttu-id="fb9b0-123">Psapimanagementapıversionset 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="fb9b0-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-124">This parameter is required.</span></span>

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

### <span data-ttu-id="fb9b0-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fb9b0-125">-PassThru</span></span>
<span data-ttu-id="fb9b0-126">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="fb9b0-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb9b0-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fb9b0-128">-ResourceId</span></span>
<span data-ttu-id="fb9b0-129">Apıversionset 'in Kolonu.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="fb9b0-130">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb9b0-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb9b0-131">-Confirm</span></span>
<span data-ttu-id="fb9b0-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb9b0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb9b0-133">-WhatIf</span></span>
<span data-ttu-id="fb9b0-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb9b0-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb9b0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9b0-136">CommonParameters</span></span>
<span data-ttu-id="fb9b0-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9b0-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fb9b0-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9b0-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb9b0-139">INPUTS</span></span>

### <span data-ttu-id="fb9b0-140">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="fb9b0-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fb9b0-141">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="fb9b0-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="fb9b0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fb9b0-142">System.String</span></span>

## <span data-ttu-id="fb9b0-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb9b0-143">OUTPUTS</span></span>

### <span data-ttu-id="fb9b0-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb9b0-144">System.Boolean</span></span>

## <span data-ttu-id="fb9b0-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb9b0-145">NOTES</span></span>

## <span data-ttu-id="fb9b0-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb9b0-146">RELATED LINKS</span></span>

[<span data-ttu-id="fb9b0-147">Get-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="fb9b0-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="fb9b0-148">New-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="fb9b0-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="fb9b0-149">Set-Azapsananagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="fb9b0-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)