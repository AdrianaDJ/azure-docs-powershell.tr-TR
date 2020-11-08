---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274220"
---
# <span data-ttu-id="5844c-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5844c-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="5844c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5844c-102">SYNOPSIS</span></span>
<span data-ttu-id="5844c-103">Bir dosyaya API 'YI dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="5844c-103">Exports an API to a file.</span></span>

## <span data-ttu-id="5844c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5844c-104">SYNTAX</span></span>

### <span data-ttu-id="5844c-105">ExportToPipeline (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5844c-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5844c-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="5844c-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5844c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5844c-107">DESCRIPTION</span></span>
<span data-ttu-id="5844c-108">**Export-Azapsananagementapı** cmdlet 'i, BIR Azure API yönetimi API 'sini desteklenen biçimlerden birinde dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="5844c-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="5844c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5844c-109">EXAMPLES</span></span>

### <span data-ttu-id="5844c-110">Örnek 1: Web uygulaması tanımlama dili (WADL) biçiminde bir API 'YI dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="5844c-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="5844c-111">Bu komut, bir WADL dosyasına API dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="5844c-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="5844c-112">Örnek 2: OpenApi 3,0 belirtim biçimindeki bir API 'YI JSON belgesi olarak dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="5844c-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="5844c-113">Bu komut, açık API biçiminde bir API tanımını JSON belgesi olarak dışarı aktarır</span><span class="sxs-lookup"><span data-stu-id="5844c-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="5844c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5844c-114">PARAMETERS</span></span>

### <span data-ttu-id="5844c-115">-Apııd</span><span class="sxs-lookup"><span data-stu-id="5844c-115">-ApiId</span></span>
<span data-ttu-id="5844c-116">Dışarı aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5844c-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="5844c-117">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="5844c-117">-ApiRevision</span></span>
<span data-ttu-id="5844c-118">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="5844c-118">Identifier of API Revision.</span></span> <span data-ttu-id="5844c-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="5844c-119">This parameter is optional.</span></span> <span data-ttu-id="5844c-120">Belirtilmezse, şu anda etkin olan API düzenlemesi için dışarı aktarma işlemi yapılır.</span><span class="sxs-lookup"><span data-stu-id="5844c-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="5844c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5844c-121">-Context</span></span>
<span data-ttu-id="5844c-122">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5844c-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5844c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5844c-123">-DefaultProfile</span></span>
<span data-ttu-id="5844c-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5844c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5844c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5844c-125">-Force</span></span>
<span data-ttu-id="5844c-126">Bu işlemin zaten varsa, aynı adın üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5844c-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="5844c-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5844c-127">-PassThru</span></span>
<span data-ttu-id="5844c-128">API başarıyla dışarı aktarıldığında bu işlemin $True geri aldığını veya başka türlü $False gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5844c-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="5844c-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="5844c-129">-SaveAs</span></span>
<span data-ttu-id="5844c-130">Dışarı aktarılan API 'nin kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5844c-130">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="5844c-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="5844c-131">-SpecificationFormat</span></span>
<span data-ttu-id="5844c-132">API biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5844c-132">Specifies the API format.</span></span>
<span data-ttu-id="5844c-133">psdx_paramvalues Wadl, WSDL, Swagger, Openapı ve Openapıjson</span><span class="sxs-lookup"><span data-stu-id="5844c-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5844c-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="5844c-134">-Confirm</span></span>
<span data-ttu-id="5844c-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5844c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5844c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5844c-136">-WhatIf</span></span>
<span data-ttu-id="5844c-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5844c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5844c-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5844c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5844c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5844c-139">CommonParameters</span></span>
<span data-ttu-id="5844c-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5844c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5844c-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5844c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5844c-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5844c-142">INPUTS</span></span>

### <span data-ttu-id="5844c-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="5844c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5844c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5844c-144">System.String</span></span>

### <span data-ttu-id="5844c-145">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapiformat</span><span class="sxs-lookup"><span data-stu-id="5844c-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="5844c-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5844c-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5844c-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5844c-147">OUTPUTS</span></span>

### <span data-ttu-id="5844c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5844c-148">System.String</span></span>

## <span data-ttu-id="5844c-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5844c-149">NOTES</span></span>

## <span data-ttu-id="5844c-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5844c-150">RELATED LINKS</span></span>

[<span data-ttu-id="5844c-151">Get-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="5844c-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="5844c-152">İçeri aktarma-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="5844c-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="5844c-153">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="5844c-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="5844c-154">Remove-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="5844c-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="5844c-155">Set-Azapsananagementapı</span><span class="sxs-lookup"><span data-stu-id="5844c-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


