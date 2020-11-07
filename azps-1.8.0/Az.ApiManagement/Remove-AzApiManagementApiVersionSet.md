---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 681ce525d1d00802cc226539fd9c3014c1786098
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917803"
---
# <span data-ttu-id="6d2d9-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="6d2d9-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="6d2d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d2d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d2d9-103">Belirli bir API sürüm kümesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6d2d9-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="6d2d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d2d9-104">SYNTAX</span></span>

### <span data-ttu-id="6d2d9-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6d2d9-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d2d9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6d2d9-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d2d9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d2d9-107">DESCRIPTION</span></span>

<span data-ttu-id="6d2d9-108">**Remove-AzAzureRmApiManagementApiVersionSet** cmdlet 'i var olan bir API sürüm kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-108">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="6d2d9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d2d9-109">EXAMPLES</span></span>

### <span data-ttu-id="6d2d9-110">Örnek 1: API sürüm kümesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6d2d9-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="6d2d9-111">Bu komut belirtilen Apıversionsetid ile API sürüm kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="6d2d9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d2d9-112">PARAMETERS</span></span>

### <span data-ttu-id="6d2d9-113">-Apıversionsetid</span><span class="sxs-lookup"><span data-stu-id="6d2d9-113">-ApiVersionSetId</span></span>
<span data-ttu-id="6d2d9-114">API sürüm kümesinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="6d2d9-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-115">This parameter is required.</span></span>

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

### <span data-ttu-id="6d2d9-116">-Context</span><span class="sxs-lookup"><span data-stu-id="6d2d9-116">-Context</span></span>
<span data-ttu-id="6d2d9-117">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6d2d9-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-118">This parameter is required.</span></span>

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

### <span data-ttu-id="6d2d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d2d9-119">-DefaultProfile</span></span>
<span data-ttu-id="6d2d9-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d2d9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d2d9-121">-InputObject</span></span>
<span data-ttu-id="6d2d9-122">Psapimanagementapıversionset 'in örneği.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="6d2d9-123">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-123">This parameter is required.</span></span>

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

### <span data-ttu-id="6d2d9-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6d2d9-124">-PassThru</span></span>
<span data-ttu-id="6d2d9-125">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="6d2d9-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="6d2d9-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d2d9-127">-Confirm</span></span>
<span data-ttu-id="6d2d9-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d2d9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d2d9-129">-WhatIf</span></span>
<span data-ttu-id="6d2d9-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d2d9-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d2d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d2d9-132">CommonParameters</span></span>
<span data-ttu-id="6d2d9-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d2d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d2d9-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d2d9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d2d9-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d2d9-135">INPUTS</span></span>

### <span data-ttu-id="6d2d9-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6d2d9-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6d2d9-137">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="6d2d9-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="6d2d9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6d2d9-138">System.String</span></span>

## <span data-ttu-id="6d2d9-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d2d9-139">OUTPUTS</span></span>

### <span data-ttu-id="6d2d9-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d2d9-140">System.Boolean</span></span>

## <span data-ttu-id="6d2d9-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d2d9-141">NOTES</span></span>

## <span data-ttu-id="6d2d9-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d2d9-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d2d9-143">Get-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="6d2d9-143">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="6d2d9-144">New-Azapsananagementapıversionset</span><span class="sxs-lookup"><span data-stu-id="6d2d9-144">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="6d2d9-145">Set-Azapsananagementapiversionset</span><span class="sxs-lookup"><span data-stu-id="6d2d9-145">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)