---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 3985f393e642645ddf9f023756e78db20074c214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595133"
---
# <span data-ttu-id="a6a64-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="a6a64-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="a6a64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a64-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a64-103">Bir dosyaya API 'YI dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="a6a64-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6a64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6a64-104">SYNTAX</span></span>

### <span data-ttu-id="a6a64-105">ExportToPipeline (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6a64-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a64-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="a6a64-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6a64-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6a64-107">DESCRIPTION</span></span>
<span data-ttu-id="a6a64-108">**Export-Azurermapımanagementapı** cmdlet 'i, BIR Azure API yönetimi API 'sini desteklenen biçimlerden birinde dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="a6a64-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="a6a64-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6a64-109">EXAMPLES</span></span>

### <span data-ttu-id="a6a64-110">Örnek 1: Web uygulaması tanımlama dili (WADL) biçiminde bir API 'YI dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="a6a64-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="a6a64-111">Bu komut, bir WADL dosyasına API dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="a6a64-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="a6a64-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6a64-112">PARAMETERS</span></span>

### <span data-ttu-id="a6a64-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="a6a64-113">-ApiId</span></span>
<span data-ttu-id="a6a64-114">Dışarı aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6a64-114">Specifies the ID of the API to export.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a64-115">-Context</span><span class="sxs-lookup"><span data-stu-id="a6a64-115">-Context</span></span>
<span data-ttu-id="a6a64-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6a64-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a64-117">-DefaultProfile</span></span>
<span data-ttu-id="a6a64-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6a64-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a64-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a6a64-119">-Force</span></span>
<span data-ttu-id="a6a64-120">Bu işlemin zaten varsa, aynı adın üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6a64-120">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a64-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a6a64-121">-PassThru</span></span>
<span data-ttu-id="a6a64-122">API başarıyla dışarı aktarıldığında bu işlemin $True geri aldığını veya başka türlü $False gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6a64-122">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a64-123">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="a6a64-123">-SaveAs</span></span>
<span data-ttu-id="a6a64-124">Dışarı aktarılan API 'nin kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6a64-124">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a64-125">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="a6a64-125">-SpecificationFormat</span></span>
<span data-ttu-id="a6a64-126">API biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6a64-126">Specifies the API format.</span></span>
<span data-ttu-id="a6a64-127">psdx_paramvalues Wadl ve Swagger.</span><span class="sxs-lookup"><span data-stu-id="a6a64-127">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a64-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6a64-128">-Confirm</span></span>
<span data-ttu-id="a6a64-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6a64-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a64-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6a64-130">-WhatIf</span></span>
<span data-ttu-id="a6a64-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6a64-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6a64-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6a64-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a64-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a64-133">CommonParameters</span></span>
<span data-ttu-id="a6a64-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6a64-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a64-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a64-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a64-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6a64-136">INPUTS</span></span>

### <span data-ttu-id="a6a64-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a6a64-137">None</span></span>
<span data-ttu-id="a6a64-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a6a64-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6a64-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6a64-139">OUTPUTS</span></span>

### <span data-ttu-id="a6a64-140">Dizisi</span><span class="sxs-lookup"><span data-stu-id="a6a64-140">String</span></span>
<span data-ttu-id="a6a64-141">Bu cmdlet, dışarı aktarılan API içeriğini dize olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="a6a64-141">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="a6a64-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6a64-142">NOTES</span></span>

## <span data-ttu-id="a6a64-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6a64-143">RELATED LINKS</span></span>

[<span data-ttu-id="a6a64-144">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a6a64-144">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="a6a64-145">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a6a64-145">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="a6a64-146">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a6a64-146">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="a6a64-147">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a6a64-147">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="a6a64-148">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="a6a64-148">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


