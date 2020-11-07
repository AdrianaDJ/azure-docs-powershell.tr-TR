---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 08d6d8e5ecbcaa8b6810bd173062c5bb244ec5e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763066"
---
# <span data-ttu-id="001a1-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="001a1-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="001a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="001a1-102">SYNOPSIS</span></span>
<span data-ttu-id="001a1-103">Ürüne bir API ekler.</span><span class="sxs-lookup"><span data-stu-id="001a1-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="001a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="001a1-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="001a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="001a1-105">DESCRIPTION</span></span>
<span data-ttu-id="001a1-106">**Add-Azurermapımanagementapıtoproduct** cmdlet 'i bir ürüne Azure API yönetim API 'si ekler.</span><span class="sxs-lookup"><span data-stu-id="001a1-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="001a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="001a1-107">EXAMPLES</span></span>

### <span data-ttu-id="001a1-108">Örnek 1: ürüne API ekleme</span><span class="sxs-lookup"><span data-stu-id="001a1-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="001a1-109">Bu komut belirtilen ürüne belirtilen API 'yi ekler.</span><span class="sxs-lookup"><span data-stu-id="001a1-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="001a1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="001a1-110">PARAMETERS</span></span>

### <span data-ttu-id="001a1-111">-Apııd</span><span class="sxs-lookup"><span data-stu-id="001a1-111">-ApiId</span></span>
<span data-ttu-id="001a1-112">Ürüne eklenecek API 'nin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="001a1-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="001a1-113">-Context</span><span class="sxs-lookup"><span data-stu-id="001a1-113">-Context</span></span>
<span data-ttu-id="001a1-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="001a1-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="001a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="001a1-115">-DefaultProfile</span></span>
<span data-ttu-id="001a1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="001a1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="001a1-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="001a1-117">-PassThru</span></span>
<span data-ttu-id="001a1-118">geçiş</span><span class="sxs-lookup"><span data-stu-id="001a1-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="001a1-119">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="001a1-119">-ProductId</span></span>
<span data-ttu-id="001a1-120">API 'nin ekleneceği ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="001a1-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="001a1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001a1-121">CommonParameters</span></span>
<span data-ttu-id="001a1-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="001a1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001a1-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="001a1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001a1-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="001a1-124">INPUTS</span></span>

### <span data-ttu-id="001a1-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="001a1-125">None</span></span>
<span data-ttu-id="001a1-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="001a1-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="001a1-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="001a1-127">OUTPUTS</span></span>

### <span data-ttu-id="001a1-128">Boole</span><span class="sxs-lookup"><span data-stu-id="001a1-128">Boolean</span></span>

## <span data-ttu-id="001a1-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="001a1-129">NOTES</span></span>

## <span data-ttu-id="001a1-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="001a1-130">RELATED LINKS</span></span>

[<span data-ttu-id="001a1-131">Remove-Azurermapımanagementapifromproduct</span><span class="sxs-lookup"><span data-stu-id="001a1-131">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


