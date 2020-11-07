---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 7b4163b18905fd0676543de1b0ead26d11c7096a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753614"
---
# <span data-ttu-id="133a4-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="133a4-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="133a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="133a4-102">SYNOPSIS</span></span>
<span data-ttu-id="133a4-103">Bir dosyaya API 'YI dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="133a4-103">Exports an API to a file.</span></span>

## <span data-ttu-id="133a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="133a4-104">SYNTAX</span></span>

### <span data-ttu-id="133a4-105">ExportToPipeline (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="133a4-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="133a4-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="133a4-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="133a4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="133a4-107">DESCRIPTION</span></span>
<span data-ttu-id="133a4-108">**Export-Azapsananagementapı** cmdlet 'i, BIR Azure API yönetimi API 'sini desteklenen biçimlerden birinde dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="133a4-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="133a4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="133a4-109">EXAMPLES</span></span>

### <span data-ttu-id="133a4-110">Örnek 1: Web uygulaması tanımlama dili (WADL) biçiminde bir API 'YI dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="133a4-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="133a4-111">Bu komut, bir WADL dosyasına API dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="133a4-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="133a4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="133a4-112">PARAMETERS</span></span>

### <span data-ttu-id="133a4-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="133a4-113">-ApiId</span></span>
<span data-ttu-id="133a4-114">Dışarı aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="133a4-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="133a4-115">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="133a4-115">-ApiRevision</span></span>
<span data-ttu-id="133a4-116">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="133a4-116">Identifier of API Revision.</span></span> <span data-ttu-id="133a4-117">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="133a4-117">This parameter is optional.</span></span> <span data-ttu-id="133a4-118">Belirtilmezse, şu anda etkin olan API düzenlemesi için dışarı aktarma işlemi yapılır.</span><span class="sxs-lookup"><span data-stu-id="133a4-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="133a4-119">-Context</span><span class="sxs-lookup"><span data-stu-id="133a4-119">-Context</span></span>
<span data-ttu-id="133a4-120">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="133a4-120">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="133a4-121">-DefaultProfile</span></span>
<span data-ttu-id="133a4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="133a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="133a4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="133a4-123">-Force</span></span>
<span data-ttu-id="133a4-124">Bu işlemin zaten varsa, aynı adın üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="133a4-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133a4-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="133a4-125">-PassThru</span></span>
<span data-ttu-id="133a4-126">API başarıyla dışarı aktarıldığında bu işlemin $True geri aldığını veya başka türlü $False gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="133a4-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133a4-127">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="133a4-127">-SaveAs</span></span>
<span data-ttu-id="133a4-128">Dışarı aktarılan API 'nin kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="133a4-128">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133a4-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="133a4-129">-SpecificationFormat</span></span>
<span data-ttu-id="133a4-130">API biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="133a4-130">Specifies the API format.</span></span>
<span data-ttu-id="133a4-131">psdx_paramvalues Wadl ve Swagger.</span><span class="sxs-lookup"><span data-stu-id="133a4-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="133a4-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="133a4-132">-Confirm</span></span>
<span data-ttu-id="133a4-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="133a4-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133a4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="133a4-134">-WhatIf</span></span>
<span data-ttu-id="133a4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="133a4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="133a4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="133a4-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133a4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133a4-137">CommonParameters</span></span>
<span data-ttu-id="133a4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="133a4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133a4-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="133a4-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133a4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="133a4-140">INPUTS</span></span>

### <span data-ttu-id="133a4-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="133a4-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="133a4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="133a4-142">System.String</span></span>

### <span data-ttu-id="133a4-143">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapiformat</span><span class="sxs-lookup"><span data-stu-id="133a4-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="133a4-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="133a4-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="133a4-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="133a4-145">OUTPUTS</span></span>

### <span data-ttu-id="133a4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="133a4-146">System.String</span></span>

## <span data-ttu-id="133a4-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="133a4-147">NOTES</span></span>

## <span data-ttu-id="133a4-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="133a4-148">RELATED LINKS</span></span>

[<span data-ttu-id="133a4-149">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="133a4-149">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="133a4-150">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="133a4-150">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="133a4-151">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="133a4-151">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="133a4-152">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="133a4-152">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="133a4-153">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="133a4-153">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


