---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 02091c1a207bc10fbdb539fb9a301d002b631827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753427"
---
# <span data-ttu-id="d139a-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d139a-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="d139a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d139a-102">SYNOPSIS</span></span>
<span data-ttu-id="d139a-103">Bir API şemasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="d139a-103">Modifies an API Schema</span></span>

## <span data-ttu-id="d139a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d139a-104">SYNTAX</span></span>

### <span data-ttu-id="d139a-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d139a-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d139a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d139a-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d139a-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="d139a-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d139a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d139a-108">DESCRIPTION</span></span>
<span data-ttu-id="d139a-109">**Set-AzApiManagementApiSchema** cmdlet 'ı BIR Azure API yönetim API şemasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d139a-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="d139a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d139a-110">EXAMPLES</span></span>

### <span data-ttu-id="d139a-111">Örnek 1: bir API şemasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="d139a-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="d139a-112">Örnekte API şeması güncelleştirilir</span><span class="sxs-lookup"><span data-stu-id="d139a-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="d139a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d139a-113">PARAMETERS</span></span>

### <span data-ttu-id="d139a-114">-Apııd</span><span class="sxs-lookup"><span data-stu-id="d139a-114">-ApiId</span></span>
<span data-ttu-id="d139a-115">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="d139a-115">Identifier of existing API.</span></span>
<span data-ttu-id="d139a-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d139a-116">This parameter is required.</span></span>

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

### <span data-ttu-id="d139a-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d139a-117">-Context</span></span>
<span data-ttu-id="d139a-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="d139a-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d139a-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d139a-119">This parameter is required.</span></span>

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

### <span data-ttu-id="d139a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d139a-120">-DefaultProfile</span></span>
<span data-ttu-id="d139a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d139a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d139a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d139a-122">-InputObject</span></span>
<span data-ttu-id="d139a-123">PsApiManagementApiSchema örneği.</span><span class="sxs-lookup"><span data-stu-id="d139a-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="d139a-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d139a-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d139a-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d139a-125">-PassThru</span></span>
<span data-ttu-id="d139a-126">Eğer belirtilmişse, ayarlanmış API 'yi temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapimanagementapı türü.</span><span class="sxs-lookup"><span data-stu-id="d139a-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="d139a-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d139a-127">-ResourceId</span></span>
<span data-ttu-id="d139a-128">Tanılama veya API şemasının ARM RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="d139a-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="d139a-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d139a-129">This parameter is required.</span></span>

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

### <span data-ttu-id="d139a-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="d139a-130">-SchemaDocument</span></span>
<span data-ttu-id="d139a-131">Dize olarak API şema belgesi.</span><span class="sxs-lookup"><span data-stu-id="d139a-131">Api schema document as a string.</span></span> <span data-ttu-id="d139a-132">Bu parametre gereklidir-SchemaDocumentFile belirtilmemiş.</span><span class="sxs-lookup"><span data-stu-id="d139a-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d139a-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="d139a-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="d139a-134">API şemasının ContentType.</span><span class="sxs-lookup"><span data-stu-id="d139a-134">ContentType of the api Schema.</span></span> <span data-ttu-id="d139a-135">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d139a-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d139a-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="d139a-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="d139a-137">API şema belge dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="d139a-137">Api schema document file path.</span></span> <span data-ttu-id="d139a-138">Bu parametre gereklidir-SchemaDocument belirtilmemiş.</span><span class="sxs-lookup"><span data-stu-id="d139a-138">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d139a-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="d139a-139">-SchemaId</span></span>
<span data-ttu-id="d139a-140">Var olan şemanın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d139a-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="d139a-141">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d139a-141">This parameter is required.</span></span>

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

### <span data-ttu-id="d139a-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="d139a-142">-Confirm</span></span>
<span data-ttu-id="d139a-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d139a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d139a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d139a-144">-WhatIf</span></span>
<span data-ttu-id="d139a-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d139a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d139a-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d139a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d139a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d139a-147">CommonParameters</span></span>
<span data-ttu-id="d139a-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d139a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d139a-149">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d139a-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d139a-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d139a-150">INPUTS</span></span>

### <span data-ttu-id="d139a-151">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="d139a-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d139a-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d139a-152">System.String</span></span>

### <span data-ttu-id="d139a-153">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="d139a-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="d139a-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d139a-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d139a-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d139a-155">OUTPUTS</span></span>

### <span data-ttu-id="d139a-156">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="d139a-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d139a-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d139a-157">NOTES</span></span>

## <span data-ttu-id="d139a-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d139a-158">RELATED LINKS</span></span>

[<span data-ttu-id="d139a-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d139a-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="d139a-160">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d139a-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="d139a-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="d139a-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

