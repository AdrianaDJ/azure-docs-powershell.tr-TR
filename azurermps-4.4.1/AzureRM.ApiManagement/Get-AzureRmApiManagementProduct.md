---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: ab0aeb77bd5f28520e39548f539d07516cd17ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591249"
---
# <span data-ttu-id="add8d-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="add8d-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="add8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="add8d-102">SYNOPSIS</span></span>
<span data-ttu-id="add8d-103">Bir listeyi veya belirli bir ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="add8d-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="add8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="add8d-104">SYNTAX</span></span>

### <span data-ttu-id="add8d-105">Tüm herkesi al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="add8d-105">Get all producst (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="add8d-106">Kimliğe göre al</span><span class="sxs-lookup"><span data-stu-id="add8d-106">Get by Id</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add8d-107">Başlığa göre al</span><span class="sxs-lookup"><span data-stu-id="add8d-107">Get by Title</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="add8d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="add8d-108">DESCRIPTION</span></span>
<span data-ttu-id="add8d-109">**Get-Azurermapsananagementproduct** cmdlet 'i bir liste veya belirli bir ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="add8d-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="add8d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="add8d-110">EXAMPLES</span></span>

### <span data-ttu-id="add8d-111">Örnek 1: tüm ürünleri alma</span><span class="sxs-lookup"><span data-stu-id="add8d-111">Example 1: Get all products</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext
```

<span data-ttu-id="add8d-112">Bu komut tüm API yönetim ürünlerini alır.</span><span class="sxs-lookup"><span data-stu-id="add8d-112">This command get all API Management products.</span></span>

### <span data-ttu-id="add8d-113">Örnek 2: KIMLIĞE göre ürün alma</span><span class="sxs-lookup"><span data-stu-id="add8d-113">Example 2: Get a product by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="add8d-114">Bu komut, KIMLIĞE göre bir API yönetim ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="add8d-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="add8d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="add8d-115">PARAMETERS</span></span>

### <span data-ttu-id="add8d-116">-Context</span><span class="sxs-lookup"><span data-stu-id="add8d-116">-Context</span></span>
<span data-ttu-id="add8d-117">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="add8d-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="add8d-118">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="add8d-118">-ProductId</span></span>
<span data-ttu-id="add8d-119">Aranacak ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="add8d-119">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="add8d-120">-Başlık</span><span class="sxs-lookup"><span data-stu-id="add8d-120">-Title</span></span>
<span data-ttu-id="add8d-121">Bakılacak ürünün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="add8d-121">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="add8d-122">Belirtilmişse, cmdlet ürünü başlığa göre almayı dener.</span><span class="sxs-lookup"><span data-stu-id="add8d-122">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Title
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="add8d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add8d-123">-DefaultProfile</span></span>
<span data-ttu-id="add8d-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="add8d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="add8d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add8d-125">CommonParameters</span></span>
<span data-ttu-id="add8d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="add8d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add8d-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add8d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add8d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="add8d-128">INPUTS</span></span>

## <span data-ttu-id="add8d-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="add8d-129">OUTPUTS</span></span>

### <span data-ttu-id="add8d-130">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct></span><span class="sxs-lookup"><span data-stu-id="add8d-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>

## <span data-ttu-id="add8d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="add8d-131">NOTES</span></span>

## <span data-ttu-id="add8d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="add8d-132">RELATED LINKS</span></span>

[<span data-ttu-id="add8d-133">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="add8d-133">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="add8d-134">Remove-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="add8d-134">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="add8d-135">Set-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="add8d-135">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


