---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: adfb6c4e1c10f2e12b4f631e14caa24f978c725e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751193"
---
# <span data-ttu-id="87ccb-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="87ccb-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="87ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="87ccb-103">Ürüne bir API ekler.</span><span class="sxs-lookup"><span data-stu-id="87ccb-103">Adds an API to a product.</span></span>

## <span data-ttu-id="87ccb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87ccb-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87ccb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="87ccb-106">**Add-Azapsananagementapıtoproduct** cmdlet 'i bir ürüne Azure API yönetim API 'si ekler.</span><span class="sxs-lookup"><span data-stu-id="87ccb-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="87ccb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="87ccb-108">Örnek 1: ürüne API ekleme</span><span class="sxs-lookup"><span data-stu-id="87ccb-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="87ccb-109">Bu komut belirtilen ürüne belirtilen API 'yi ekler.</span><span class="sxs-lookup"><span data-stu-id="87ccb-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="87ccb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87ccb-110">PARAMETERS</span></span>

### <span data-ttu-id="87ccb-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="87ccb-111">-ApiId</span></span>
<span data-ttu-id="87ccb-112">Ürüne eklenecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="87ccb-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="87ccb-113">-Context</span><span class="sxs-lookup"><span data-stu-id="87ccb-113">-Context</span></span>
<span data-ttu-id="87ccb-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="87ccb-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="87ccb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ccb-115">-DefaultProfile</span></span>
<span data-ttu-id="87ccb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87ccb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87ccb-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="87ccb-117">-PassThru</span></span>
<span data-ttu-id="87ccb-118">geçiş</span><span class="sxs-lookup"><span data-stu-id="87ccb-118">passthru</span></span>

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

### <span data-ttu-id="87ccb-119">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="87ccb-119">-ProductId</span></span>
<span data-ttu-id="87ccb-120">API 'nin ekleneceği ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="87ccb-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="87ccb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ccb-121">CommonParameters</span></span>
<span data-ttu-id="87ccb-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87ccb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ccb-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87ccb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ccb-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87ccb-124">INPUTS</span></span>

### <span data-ttu-id="87ccb-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="87ccb-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87ccb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="87ccb-126">System.String</span></span>

### <span data-ttu-id="87ccb-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87ccb-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="87ccb-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87ccb-128">OUTPUTS</span></span>

### <span data-ttu-id="87ccb-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87ccb-129">System.Boolean</span></span>

## <span data-ttu-id="87ccb-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87ccb-130">NOTES</span></span>

## <span data-ttu-id="87ccb-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87ccb-131">RELATED LINKS</span></span>

[<span data-ttu-id="87ccb-132">Remove-Azapsananagementapifromproduct</span><span class="sxs-lookup"><span data-stu-id="87ccb-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


