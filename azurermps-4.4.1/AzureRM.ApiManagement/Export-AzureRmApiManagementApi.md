---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 09400d3111ffb3fda232e1cbb71fd0aac063a74c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763414"
---
# <span data-ttu-id="1e979-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1e979-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="1e979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e979-102">SYNOPSIS</span></span>
<span data-ttu-id="1e979-103">Bir dosyaya API 'YI dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="1e979-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e979-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e979-104">SYNTAX</span></span>

### <span data-ttu-id="1e979-105">Ardışık düzene dışarı aktarma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1e979-105">Export to pipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e979-106">Dosyaya aktar</span><span class="sxs-lookup"><span data-stu-id="1e979-106">Export to File</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e979-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e979-107">DESCRIPTION</span></span>
<span data-ttu-id="1e979-108">**Export-Azurermapımanagementapı** cmdlet 'i, BIR Azure API yönetimi API 'sini desteklenen biçimlerden birinde dosyaya aktarır.</span><span class="sxs-lookup"><span data-stu-id="1e979-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="1e979-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e979-109">EXAMPLES</span></span>

### <span data-ttu-id="1e979-110">Örnek 1: Web uygulaması tanımlama dili (WADL) biçiminde bir API 'YI dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="1e979-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="1e979-111">Bu komut, bir WADL dosyasına API dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="1e979-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="1e979-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e979-112">PARAMETERS</span></span>

### <span data-ttu-id="1e979-113">-Apııd</span><span class="sxs-lookup"><span data-stu-id="1e979-113">-ApiId</span></span>
<span data-ttu-id="1e979-114">Dışarı aktarılacak API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e979-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="1e979-115">-Context</span><span class="sxs-lookup"><span data-stu-id="1e979-115">-Context</span></span>
<span data-ttu-id="1e979-116">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e979-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1e979-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1e979-117">-Force</span></span>
<span data-ttu-id="1e979-118">Bu işlemin zaten varsa, aynı adın üzerine yazabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e979-118">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e979-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1e979-119">-PassThru</span></span>
<span data-ttu-id="1e979-120">API başarıyla dışarı aktarıldığında bu işlemin $True geri aldığını veya başka türlü $False gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e979-120">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e979-121">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="1e979-121">-SaveAs</span></span>
<span data-ttu-id="1e979-122">Dışarı aktarılan API 'nin kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e979-122">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e979-123">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="1e979-123">-SpecificationFormat</span></span>
<span data-ttu-id="1e979-124">API biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e979-124">Specifies the API format.</span></span>
<span data-ttu-id="1e979-125">psdx_paramvalues Wadl ve Swagger.</span><span class="sxs-lookup"><span data-stu-id="1e979-125">psdx_paramvalues Wadl and Swagger.</span></span>

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

### <span data-ttu-id="1e979-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e979-126">-Confirm</span></span>
<span data-ttu-id="1e979-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e979-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e979-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e979-128">-WhatIf</span></span>
<span data-ttu-id="1e979-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e979-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e979-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e979-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e979-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e979-131">-DefaultProfile</span></span>
<span data-ttu-id="1e979-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e979-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e979-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e979-133">CommonParameters</span></span>
<span data-ttu-id="1e979-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e979-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e979-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e979-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e979-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e979-136">INPUTS</span></span>

## <span data-ttu-id="1e979-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e979-137">OUTPUTS</span></span>

### <span data-ttu-id="1e979-138">Dizisi</span><span class="sxs-lookup"><span data-stu-id="1e979-138">String</span></span>
<span data-ttu-id="1e979-139">Bu cmdlet, dışarı aktarılan API içeriğini dize olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="1e979-139">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="1e979-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e979-140">NOTES</span></span>

## <span data-ttu-id="1e979-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e979-141">RELATED LINKS</span></span>

[<span data-ttu-id="1e979-142">Get-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="1e979-142">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="1e979-143">Import-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="1e979-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="1e979-144">Yeni-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="1e979-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="1e979-145">Remove-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="1e979-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="1e979-146">Set-Azurermapımanagementapı</span><span class="sxs-lookup"><span data-stu-id="1e979-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


