---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 16bb651efd13d42b25509834637faea866678459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763925"
---
# <span data-ttu-id="d7757-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="d7757-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="d7757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7757-102">SYNOPSIS</span></span>
<span data-ttu-id="d7757-103">Ürüne bir API ekler.</span><span class="sxs-lookup"><span data-stu-id="d7757-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7757-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7757-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7757-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7757-105">DESCRIPTION</span></span>
<span data-ttu-id="d7757-106">**Add-Azurermapımanagementapıtoproduct** cmdlet 'i bir ürüne Azure API yönetim API 'si ekler.</span><span class="sxs-lookup"><span data-stu-id="d7757-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="d7757-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7757-107">EXAMPLES</span></span>

### <span data-ttu-id="d7757-108">Örnek 1: ürüne API ekleme</span><span class="sxs-lookup"><span data-stu-id="d7757-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="d7757-109">Bu komut belirtilen ürüne belirtilen API 'yi ekler.</span><span class="sxs-lookup"><span data-stu-id="d7757-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="d7757-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7757-110">PARAMETERS</span></span>

### <span data-ttu-id="d7757-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="d7757-111">-ApiId</span></span>
<span data-ttu-id="d7757-112">Ürüne eklenecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7757-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="d7757-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d7757-113">-Context</span></span>
<span data-ttu-id="d7757-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7757-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d7757-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7757-115">-DefaultProfile</span></span>
<span data-ttu-id="d7757-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7757-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7757-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d7757-117">-PassThru</span></span>
<span data-ttu-id="d7757-118">geçiş</span><span class="sxs-lookup"><span data-stu-id="d7757-118">passthru</span></span>

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

### <span data-ttu-id="d7757-119">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="d7757-119">-ProductId</span></span>
<span data-ttu-id="d7757-120">API 'nin ekleneceği ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7757-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="d7757-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7757-121">CommonParameters</span></span>
<span data-ttu-id="d7757-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7757-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7757-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7757-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7757-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7757-124">INPUTS</span></span>

### <span data-ttu-id="d7757-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="d7757-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d7757-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d7757-126">System.String</span></span>

### <span data-ttu-id="d7757-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7757-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7757-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7757-128">OUTPUTS</span></span>

### <span data-ttu-id="d7757-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7757-129">System.Boolean</span></span>

## <span data-ttu-id="d7757-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7757-130">NOTES</span></span>

## <span data-ttu-id="d7757-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7757-131">RELATED LINKS</span></span>

[<span data-ttu-id="d7757-132">Remove-Azurermapımanagementapifromproduct</span><span class="sxs-lookup"><span data-stu-id="d7757-132">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


