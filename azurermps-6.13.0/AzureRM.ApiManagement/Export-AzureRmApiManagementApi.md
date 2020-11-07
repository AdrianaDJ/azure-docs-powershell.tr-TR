---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 7dc06f280595551a9e054c251339e96163b798b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762811"
---
# <span data-ttu-id="edcfd-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="edcfd-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="edcfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edcfd-102">SYNOPSIS</span></span>
<span data-ttu-id="edcfd-103">Bir dosyaya API 'YI dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="edcfd-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edcfd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edcfd-104">SYNTAX</span></span>

### <span data-ttu-id="edcfd-105">ExportToPipeline (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="edcfd-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edcfd-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="edcfd-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edcfd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="edcfd-107">DESCRIPTION</span></span>
<span data-ttu-id="edcfd-108">**Export-Azurermapımanagementapı** cmdlet 'i, BIR Azure API yönetimi API 'sini desteklenen biçimlerden birinde dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="edcfd-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="edcfd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edcfd-109">EXAMPLES</span></span>

### <span data-ttu-id="edcfd-110">Örnek 1: Web uygulaması tanımlama dili (WADL) biçiminde bir API 'YI dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="edcfd-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="edcfd-111">Bu komut, bir WADL dosyasına API dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="edcfd-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="edcfd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edcfd-112">PARAMETERS</span></span>

### <span data-ttu-id="edcfd-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="edcfd-113">-ApiId</span></span>
<span data-ttu-id="edcfd-114">Dışarı aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="edcfd-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="edcfd-115">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="edcfd-115">-ApiRevision</span></span>
<span data-ttu-id="edcfd-116">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="edcfd-116">Identifier of API Revision.</span></span> <span data-ttu-id="edcfd-117">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="edcfd-117">This parameter is optional.</span></span> <span data-ttu-id="edcfd-118">Belirtilmezse, şu anda etkin olan API düzenlemesi için dışarı aktarma işlemi yapılır.</span><span class="sxs-lookup"><span data-stu-id="edcfd-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="edcfd-119">-Context</span><span class="sxs-lookup"><span data-stu-id="edcfd-119">-Context</span></span>
<span data-ttu-id="edcfd-120">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="edcfd-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="edcfd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edcfd-121">-DefaultProfile</span></span>
<span data-ttu-id="edcfd-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edcfd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcfd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="edcfd-123">-Force</span></span>
<span data-ttu-id="edcfd-124">Bu işlemin zaten varsa, aynı adın üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="edcfd-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="edcfd-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="edcfd-125">-PassThru</span></span>
<span data-ttu-id="edcfd-126">API başarıyla dışarı aktarıldığında bu işlemin $True geri aldığını veya başka türlü $False gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="edcfd-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="edcfd-127">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="edcfd-127">-SaveAs</span></span>
<span data-ttu-id="edcfd-128">Dışarı aktarılan API 'nin kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="edcfd-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="edcfd-129">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="edcfd-129">-SpecificationFormat</span></span>
<span data-ttu-id="edcfd-130">API biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="edcfd-130">Specifies the API format.</span></span>
<span data-ttu-id="edcfd-131">psdx_paramvalues Wadl ve Swagger.</span><span class="sxs-lookup"><span data-stu-id="edcfd-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edcfd-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="edcfd-132">-Confirm</span></span>
<span data-ttu-id="edcfd-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edcfd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edcfd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edcfd-134">-WhatIf</span></span>
<span data-ttu-id="edcfd-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edcfd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edcfd-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edcfd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edcfd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edcfd-137">CommonParameters</span></span>
<span data-ttu-id="edcfd-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edcfd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edcfd-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edcfd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edcfd-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edcfd-140">INPUTS</span></span>

### <span data-ttu-id="edcfd-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="edcfd-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="edcfd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="edcfd-142">System.String</span></span>

### <span data-ttu-id="edcfd-143">Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementapiformat</span><span class="sxs-lookup"><span data-stu-id="edcfd-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="edcfd-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="edcfd-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="edcfd-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edcfd-145">OUTPUTS</span></span>

### <span data-ttu-id="edcfd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="edcfd-146">System.String</span></span>
<span data-ttu-id="edcfd-147">Bu cmdlet, dışarı aktarılan API içeriğini dize olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="edcfd-147">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="edcfd-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edcfd-148">NOTES</span></span>

## <span data-ttu-id="edcfd-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edcfd-149">RELATED LINKS</span></span>

[<span data-ttu-id="edcfd-150">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="edcfd-150">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="edcfd-151">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="edcfd-151">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="edcfd-152">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="edcfd-152">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="edcfd-153">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="edcfd-153">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="edcfd-154">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="edcfd-154">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


