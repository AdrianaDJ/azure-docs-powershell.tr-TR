---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 430264a27cfff11416b322285a0db05b230b3bbc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753463"
---
# <span data-ttu-id="f614f-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="f614f-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="f614f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f614f-102">SYNOPSIS</span></span>
<span data-ttu-id="f614f-103">Tanılama varlığını genel veya API Düzey kapsamından kaldırın.</span><span class="sxs-lookup"><span data-stu-id="f614f-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="f614f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f614f-104">SYNTAX</span></span>

### <span data-ttu-id="f614f-105">Byresourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f614f-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f614f-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="f614f-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f614f-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f614f-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f614f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f614f-108">DESCRIPTION</span></span>
<span data-ttu-id="f614f-109">**Remove-Azapsananagementdiagnostic** cmdlet 'i `DiagnosticId` genel kapsamdan veya bir kapsamdan belirtilen tanılama varlığını kaldırır `ApiId`</span><span class="sxs-lookup"><span data-stu-id="f614f-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="f614f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f614f-110">EXAMPLES</span></span>

### <span data-ttu-id="f614f-111">Örnek 1: Tanılama varlığını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f614f-111">Example 1 : Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="f614f-112">Bu örnekte, tanılama `applicationinsights` API yönetimi hizmetinden kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="f614f-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="f614f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f614f-113">PARAMETERS</span></span>

### <span data-ttu-id="f614f-114">-Apııd</span><span class="sxs-lookup"><span data-stu-id="f614f-114">-ApiId</span></span>
<span data-ttu-id="f614f-115">API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="f614f-115">Identifier of the API.</span></span>
<span data-ttu-id="f614f-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f614f-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="f614f-117">-Context</span></span>
<span data-ttu-id="f614f-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="f614f-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f614f-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f614f-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f614f-120">-DefaultProfile</span></span>
<span data-ttu-id="f614f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f614f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f614f-122">-Diagnosticıd</span><span class="sxs-lookup"><span data-stu-id="f614f-122">-DiagnosticId</span></span>
<span data-ttu-id="f614f-123">Var olan ürünün tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="f614f-123">Identifier of existing product.</span></span>
<span data-ttu-id="f614f-124">Belirtilmişse ürün kapsam ilkesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f614f-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="f614f-125">Bu parametreler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f614f-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f614f-126">-InputObject</span></span>
<span data-ttu-id="f614f-127">PsApiManagementDiagnostic örneği.</span><span class="sxs-lookup"><span data-stu-id="f614f-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="f614f-128">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f614f-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f614f-129">-PassThru</span></span>
<span data-ttu-id="f614f-130">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="f614f-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="f614f-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f614f-131">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f614f-132">-ResourceId</span></span>
<span data-ttu-id="f614f-133">Tanının kullanımı</span><span class="sxs-lookup"><span data-stu-id="f614f-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="f614f-134">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f614f-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f614f-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="f614f-135">-Confirm</span></span>
<span data-ttu-id="f614f-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f614f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f614f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f614f-137">-WhatIf</span></span>
<span data-ttu-id="f614f-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f614f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f614f-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f614f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f614f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f614f-140">CommonParameters</span></span>
<span data-ttu-id="f614f-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f614f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f614f-142">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f614f-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f614f-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f614f-143">INPUTS</span></span>

### <span data-ttu-id="f614f-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f614f-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f614f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f614f-145">System.String</span></span>

### <span data-ttu-id="f614f-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f614f-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f614f-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f614f-147">OUTPUTS</span></span>

### <span data-ttu-id="f614f-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f614f-148">System.Boolean</span></span>

## <span data-ttu-id="f614f-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f614f-149">NOTES</span></span>

## <span data-ttu-id="f614f-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f614f-150">RELATED LINKS</span></span>

[<span data-ttu-id="f614f-151">Get-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="f614f-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="f614f-152">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="f614f-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="f614f-153">Set-Azapsananagementdiagnostic</span><span class="sxs-lookup"><span data-stu-id="f614f-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)