---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 23881baf47536db4fa694cf2165b8550b7f8cd62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103863"
---
# <span data-ttu-id="ba54d-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ba54d-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="ba54d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba54d-102">SYNOPSIS</span></span>
<span data-ttu-id="ba54d-103">Bir API şemasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="ba54d-103">Modifies an API Schema</span></span>

## <span data-ttu-id="ba54d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba54d-104">SYNTAX</span></span>

### <span data-ttu-id="ba54d-105">ExpandedParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ba54d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba54d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ba54d-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba54d-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="ba54d-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba54d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba54d-108">DESCRIPTION</span></span>
<span data-ttu-id="ba54d-109">**Set-AzApiManagementApiSchema** cmdlet 'ı BIR Azure API yönetim API şemasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ba54d-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="ba54d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba54d-110">EXAMPLES</span></span>

### <span data-ttu-id="ba54d-111">Örnek 1: bir API şemasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="ba54d-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="ba54d-112">Örnekte API şeması güncelleştirilir</span><span class="sxs-lookup"><span data-stu-id="ba54d-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="ba54d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba54d-113">PARAMETERS</span></span>

### <span data-ttu-id="ba54d-114">-Apııd</span><span class="sxs-lookup"><span data-stu-id="ba54d-114">-ApiId</span></span>
<span data-ttu-id="ba54d-115">Var olan API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="ba54d-115">Identifier of existing API.</span></span>
<span data-ttu-id="ba54d-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ba54d-116">This parameter is required.</span></span>

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

### <span data-ttu-id="ba54d-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ba54d-117">-Context</span></span>
<span data-ttu-id="ba54d-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="ba54d-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ba54d-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ba54d-119">This parameter is required.</span></span>

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

### <span data-ttu-id="ba54d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba54d-120">-DefaultProfile</span></span>
<span data-ttu-id="ba54d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba54d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba54d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba54d-122">-InputObject</span></span>
<span data-ttu-id="ba54d-123">PsApiManagementApiSchema örneği.</span><span class="sxs-lookup"><span data-stu-id="ba54d-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="ba54d-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ba54d-124">This parameter is required.</span></span>

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

### <span data-ttu-id="ba54d-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ba54d-125">-PassThru</span></span>
<span data-ttu-id="ba54d-126">Eğer belirtilmişse, ayarlanmış API 'yi temsil eden Microsoft. Azure. Commands. Apsananad. ServiceManagement. model. Psapimanagementapı türü.</span><span class="sxs-lookup"><span data-stu-id="ba54d-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="ba54d-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ba54d-127">-ResourceId</span></span>
<span data-ttu-id="ba54d-128">Tanılama veya API şemasının ARM RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="ba54d-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="ba54d-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ba54d-129">This parameter is required.</span></span>

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

### <span data-ttu-id="ba54d-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="ba54d-130">-SchemaDocument</span></span>
<span data-ttu-id="ba54d-131">Dize olarak API şema belgesi.</span><span class="sxs-lookup"><span data-stu-id="ba54d-131">Api schema document as a string.</span></span> <span data-ttu-id="ba54d-132">Bu parametre gereklidir-SchemaDocumentFile belirtilmemiş.</span><span class="sxs-lookup"><span data-stu-id="ba54d-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="ba54d-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="ba54d-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="ba54d-134">API şemasının ContentType.</span><span class="sxs-lookup"><span data-stu-id="ba54d-134">ContentType of the api Schema.</span></span> <span data-ttu-id="ba54d-135">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ba54d-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="ba54d-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="ba54d-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="ba54d-137">API şema belge dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="ba54d-137">Api schema document file path.</span></span> <span data-ttu-id="ba54d-138">Bu parametre gereklidir-SchemaDocument belirtilmemiş.</span><span class="sxs-lookup"><span data-stu-id="ba54d-138">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="ba54d-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="ba54d-139">-SchemaId</span></span>
<span data-ttu-id="ba54d-140">Var olan şemanın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ba54d-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="ba54d-141">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ba54d-141">This parameter is required.</span></span>

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

### <span data-ttu-id="ba54d-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="ba54d-142">-Confirm</span></span>
<span data-ttu-id="ba54d-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ba54d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba54d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba54d-144">-WhatIf</span></span>
<span data-ttu-id="ba54d-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba54d-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba54d-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ba54d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba54d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba54d-147">CommonParameters</span></span>
<span data-ttu-id="ba54d-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba54d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba54d-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba54d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba54d-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba54d-150">INPUTS</span></span>

### <span data-ttu-id="ba54d-151">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="ba54d-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ba54d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ba54d-152">System.String</span></span>

### <span data-ttu-id="ba54d-153">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="ba54d-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="ba54d-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ba54d-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ba54d-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba54d-155">OUTPUTS</span></span>

### <span data-ttu-id="ba54d-156">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="ba54d-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="ba54d-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba54d-157">NOTES</span></span>

## <span data-ttu-id="ba54d-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba54d-158">RELATED LINKS</span></span>

[<span data-ttu-id="ba54d-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ba54d-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="ba54d-160">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ba54d-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="ba54d-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ba54d-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

