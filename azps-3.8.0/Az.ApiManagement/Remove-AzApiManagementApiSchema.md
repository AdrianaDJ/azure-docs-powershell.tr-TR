---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: fb144bfa228b07501c374f054970d1e3e0337ec1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94105069"
---
# <span data-ttu-id="640b1-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="640b1-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="640b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="640b1-102">SYNOPSIS</span></span>
<span data-ttu-id="640b1-103">API 'dan API şemasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="640b1-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="640b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="640b1-104">SYNTAX</span></span>

### <span data-ttu-id="640b1-105">Byaplarbu (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="640b1-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="640b1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="640b1-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="640b1-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="640b1-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="640b1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="640b1-108">DESCRIPTION</span></span>
<span data-ttu-id="640b1-109">API 'dan **Remove-Azapsananagementschema** cmdlet 'i.</span><span class="sxs-lookup"><span data-stu-id="640b1-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="640b1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="640b1-110">EXAMPLES</span></span>

### <span data-ttu-id="640b1-111">Örnek 1: API 'yi API 'den kaldırır</span><span class="sxs-lookup"><span data-stu-id="640b1-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="640b1-112">Başvurulmuyorsa, komut dosyası şemayı `2` API 'den kaldırır `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="640b1-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="640b1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="640b1-113">PARAMETERS</span></span>

### <span data-ttu-id="640b1-114">-Apııd</span><span class="sxs-lookup"><span data-stu-id="640b1-114">-ApiId</span></span>
<span data-ttu-id="640b1-115">API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="640b1-115">Identifier of the API.</span></span>
<span data-ttu-id="640b1-116">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="640b1-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640b1-117">-Context</span><span class="sxs-lookup"><span data-stu-id="640b1-117">-Context</span></span>
<span data-ttu-id="640b1-118">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="640b1-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="640b1-119">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="640b1-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="640b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="640b1-120">-DefaultProfile</span></span>
<span data-ttu-id="640b1-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="640b1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="640b1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="640b1-122">-InputObject</span></span>
<span data-ttu-id="640b1-123">PsApiManagementApiSchema örneği.</span><span class="sxs-lookup"><span data-stu-id="640b1-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="640b1-124">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="640b1-124">This parameter is required.</span></span>

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

### <span data-ttu-id="640b1-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="640b1-125">-PassThru</span></span>
<span data-ttu-id="640b1-126">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="640b1-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="640b1-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="640b1-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="640b1-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="640b1-128">-ResourceId</span></span>
<span data-ttu-id="640b1-129">Mirama</span><span class="sxs-lookup"><span data-stu-id="640b1-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="640b1-130">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="640b1-130">This parameter is required.</span></span>

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

### <span data-ttu-id="640b1-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="640b1-131">-SchemaId</span></span>
<span data-ttu-id="640b1-132">API şemasının tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="640b1-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="640b1-133">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="640b1-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="640b1-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="640b1-134">-Confirm</span></span>
<span data-ttu-id="640b1-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="640b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="640b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="640b1-136">-WhatIf</span></span>
<span data-ttu-id="640b1-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="640b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="640b1-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="640b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="640b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="640b1-139">CommonParameters</span></span>
<span data-ttu-id="640b1-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="640b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="640b1-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="640b1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="640b1-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="640b1-142">INPUTS</span></span>

### <span data-ttu-id="640b1-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="640b1-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="640b1-144">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="640b1-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="640b1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="640b1-145">System.String</span></span>

## <span data-ttu-id="640b1-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="640b1-146">OUTPUTS</span></span>

### <span data-ttu-id="640b1-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="640b1-147">System.Boolean</span></span>

## <span data-ttu-id="640b1-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="640b1-148">NOTES</span></span>

## <span data-ttu-id="640b1-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="640b1-149">RELATED LINKS</span></span>

[<span data-ttu-id="640b1-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="640b1-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="640b1-151">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="640b1-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="640b1-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="640b1-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
