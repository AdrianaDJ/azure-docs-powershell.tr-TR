---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: a4bbc330b5cd4d7eaeec1d2e68252ceb5dd261f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589926"
---
# <span data-ttu-id="68e72-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="68e72-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="68e72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68e72-102">SYNOPSIS</span></span>
<span data-ttu-id="68e72-103">Bir listeyi veya belirli bir ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="68e72-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68e72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68e72-104">SYNTAX</span></span>

### <span data-ttu-id="68e72-105">GetAllProducts (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68e72-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68e72-106">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="68e72-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68e72-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="68e72-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68e72-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="68e72-108">DESCRIPTION</span></span>
<span data-ttu-id="68e72-109">**Get-Azurermapsananagementproduct** cmdlet 'i bir liste veya belirli bir ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="68e72-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="68e72-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68e72-110">EXAMPLES</span></span>

### <span data-ttu-id="68e72-111">Örnek 1: tüm ürünleri alma</span><span class="sxs-lookup"><span data-stu-id="68e72-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="68e72-112">Bu komut tüm API yönetim ürünlerini alır.</span><span class="sxs-lookup"><span data-stu-id="68e72-112">This command get all API Management products.</span></span>

### <span data-ttu-id="68e72-113">Örnek 2: KIMLIĞE göre ürün alma</span><span class="sxs-lookup"><span data-stu-id="68e72-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="68e72-114">Bu komut, KIMLIĞE göre bir API yönetim ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="68e72-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="68e72-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68e72-115">PARAMETERS</span></span>

### <span data-ttu-id="68e72-116">-Context</span><span class="sxs-lookup"><span data-stu-id="68e72-116">-Context</span></span>
<span data-ttu-id="68e72-117">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="68e72-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="68e72-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e72-118">-DefaultProfile</span></span>
<span data-ttu-id="68e72-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68e72-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="68e72-120">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="68e72-120">-ProductId</span></span>
<span data-ttu-id="68e72-121">Aranacak ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68e72-121">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e72-122">-Başlık</span><span class="sxs-lookup"><span data-stu-id="68e72-122">-Title</span></span>
<span data-ttu-id="68e72-123">Bakılacak ürünün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68e72-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="68e72-124">Belirtilmişse, cmdlet ürünü başlığa göre almayı dener.</span><span class="sxs-lookup"><span data-stu-id="68e72-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: String
Parameter Sets: GetByTitle
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e72-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e72-125">CommonParameters</span></span>
<span data-ttu-id="68e72-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68e72-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e72-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e72-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e72-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68e72-128">INPUTS</span></span>

### <span data-ttu-id="68e72-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="68e72-129">None</span></span>
<span data-ttu-id="68e72-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="68e72-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68e72-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68e72-131">OUTPUTS</span></span>

### <span data-ttu-id="68e72-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="68e72-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>
<span data-ttu-id="68e72-133">API yönetim hizmetindeki ürünün ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="68e72-133">The details of the Product in API Management service.</span></span>

### <span data-ttu-id="68e72-134">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct></span><span class="sxs-lookup"><span data-stu-id="68e72-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>
<span data-ttu-id="68e72-135">API yönetim hizmetindeki ürün listesi.</span><span class="sxs-lookup"><span data-stu-id="68e72-135">The list of Product in API Management service.</span></span>

## <span data-ttu-id="68e72-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68e72-136">NOTES</span></span>

## <span data-ttu-id="68e72-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68e72-137">RELATED LINKS</span></span>

[<span data-ttu-id="68e72-138">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="68e72-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="68e72-139">Remove-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="68e72-139">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="68e72-140">Set-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="68e72-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


