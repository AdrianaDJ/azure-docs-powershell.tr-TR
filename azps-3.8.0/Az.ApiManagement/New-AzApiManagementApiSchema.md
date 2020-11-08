---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: ad931b574af8445947e9f3f4df12c35c2baa1bf7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097741"
---
# <span data-ttu-id="137c8-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="137c8-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="137c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="137c8-102">SYNOPSIS</span></span>
<span data-ttu-id="137c8-103">Yeni API 'yi, Apımanai hizmetinde oluşturur</span><span class="sxs-lookup"><span data-stu-id="137c8-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="137c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="137c8-104">SYNTAX</span></span>

### <span data-ttu-id="137c8-105">Schemabelgelertinline (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="137c8-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="137c8-106">Schemabelgelertfromdosyası</span><span class="sxs-lookup"><span data-stu-id="137c8-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="137c8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="137c8-107">DESCRIPTION</span></span>
<span data-ttu-id="137c8-108">API 'nin yeni API şemasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="137c8-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="137c8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="137c8-109">EXAMPLES</span></span>

### <span data-ttu-id="137c8-110">Örnek 1: Swagger petstore kapsamlı API için yeni şema oluşturma</span><span class="sxs-lookup"><span data-stu-id="137c8-110">Example 1 : Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="137c8-111">**New-AzApiManagementApiSchema** cmdlet 'i API 'yi oluşturur veya oluşturur `swagger-petstore-extensive` .</span><span class="sxs-lookup"><span data-stu-id="137c8-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="137c8-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="137c8-112">PARAMETERS</span></span>

### <span data-ttu-id="137c8-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="137c8-113">-ApiId</span></span>
<span data-ttu-id="137c8-114">API tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="137c8-114">Identifier of api.</span></span> <span data-ttu-id="137c8-115">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="137c8-115">This parameter is required.</span></span>

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

### <span data-ttu-id="137c8-116">-Context</span><span class="sxs-lookup"><span data-stu-id="137c8-116">-Context</span></span>
<span data-ttu-id="137c8-117">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="137c8-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="137c8-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="137c8-118">This parameter is required.</span></span>

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

### <span data-ttu-id="137c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="137c8-119">-DefaultProfile</span></span>
<span data-ttu-id="137c8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="137c8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="137c8-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="137c8-121">-SchemaDocument</span></span>
<span data-ttu-id="137c8-122">Dize olarak API şema belgesi.</span><span class="sxs-lookup"><span data-stu-id="137c8-122">Api schema document as a string.</span></span> <span data-ttu-id="137c8-123">Bu parametre gereklidir-SchemaDocumentFile belirtilmemiş.</span><span class="sxs-lookup"><span data-stu-id="137c8-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="137c8-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="137c8-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="137c8-125">API şemasının ContentType.</span><span class="sxs-lookup"><span data-stu-id="137c8-125">ContentType of the api Schema.</span></span> <span data-ttu-id="137c8-126">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="137c8-126">This parameter is required.</span></span>

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

### <span data-ttu-id="137c8-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="137c8-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="137c8-128">API şema belge dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="137c8-128">Api schema document file path.</span></span> <span data-ttu-id="137c8-129">Bu parametre gereklidir-SchemaDocument belirtilmemiş.</span><span class="sxs-lookup"><span data-stu-id="137c8-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="137c8-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="137c8-130">-SchemaId</span></span>
<span data-ttu-id="137c8-131">Yeni şemanın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="137c8-131">Identifier of new schema.</span></span>
<span data-ttu-id="137c8-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="137c8-132">This parameter is optional.</span></span>
<span data-ttu-id="137c8-133">Belirtilmemişse,.</span><span class="sxs-lookup"><span data-stu-id="137c8-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="137c8-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="137c8-134">-Confirm</span></span>
<span data-ttu-id="137c8-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="137c8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="137c8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="137c8-136">-WhatIf</span></span>
<span data-ttu-id="137c8-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="137c8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="137c8-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="137c8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="137c8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="137c8-139">CommonParameters</span></span>
<span data-ttu-id="137c8-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="137c8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="137c8-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="137c8-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="137c8-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="137c8-142">INPUTS</span></span>

### <span data-ttu-id="137c8-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="137c8-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="137c8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="137c8-144">System.String</span></span>

## <span data-ttu-id="137c8-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="137c8-145">OUTPUTS</span></span>

### <span data-ttu-id="137c8-146">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="137c8-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="137c8-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="137c8-147">NOTES</span></span>

## <span data-ttu-id="137c8-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="137c8-148">RELATED LINKS</span></span>

[<span data-ttu-id="137c8-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="137c8-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="137c8-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="137c8-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="137c8-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="137c8-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)