---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 8e59cbb9885587ee57103b78400ce8ece9aafd46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097402"
---
# <span data-ttu-id="f8965-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f8965-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="f8965-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8965-102">SYNOPSIS</span></span>
<span data-ttu-id="f8965-103">Bir listeyi veya belirli bir ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="f8965-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="f8965-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8965-104">SYNTAX</span></span>

### <span data-ttu-id="f8965-105">GetAllProducts (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f8965-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8965-106">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="f8965-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8965-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="f8965-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8965-108">Getbyapııd</span><span class="sxs-lookup"><span data-stu-id="f8965-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8965-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8965-109">DESCRIPTION</span></span>
<span data-ttu-id="f8965-110">**Get-Azapsananagementproduct** cmdlet 'i bir liste veya belirli bir ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="f8965-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="f8965-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8965-111">EXAMPLES</span></span>

### <span data-ttu-id="f8965-112">Örnek 1: tüm ürünleri alma</span><span class="sxs-lookup"><span data-stu-id="f8965-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="f8965-113">Bu komut tüm API yönetim ürünlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f8965-113">This command get all API Management products.</span></span>

### <span data-ttu-id="f8965-114">Örnek 2: KIMLIĞE göre ürün alma</span><span class="sxs-lookup"><span data-stu-id="f8965-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="f8965-115">Bu komut, KIMLIĞE göre bir API yönetim ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="f8965-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="f8965-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8965-116">PARAMETERS</span></span>

### <span data-ttu-id="f8965-117">-Apııd</span><span class="sxs-lookup"><span data-stu-id="f8965-117">-ApiId</span></span>
<span data-ttu-id="f8965-118">İlgili ürünleri bulmak için API 'nin IID 'Si.</span><span class="sxs-lookup"><span data-stu-id="f8965-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="f8965-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f8965-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8965-120">-Context</span><span class="sxs-lookup"><span data-stu-id="f8965-120">-Context</span></span>
<span data-ttu-id="f8965-121">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8965-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8965-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8965-122">-DefaultProfile</span></span>
<span data-ttu-id="f8965-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8965-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8965-124">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="f8965-124">-ProductId</span></span>
<span data-ttu-id="f8965-125">Aranacak ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8965-125">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8965-126">-Başlık</span><span class="sxs-lookup"><span data-stu-id="f8965-126">-Title</span></span>
<span data-ttu-id="f8965-127">Bakılacak ürünün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8965-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="f8965-128">Belirtilmişse, cmdlet ürünü başlığa göre almayı dener.</span><span class="sxs-lookup"><span data-stu-id="f8965-128">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8965-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8965-129">CommonParameters</span></span>
<span data-ttu-id="f8965-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8965-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8965-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f8965-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8965-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8965-132">INPUTS</span></span>

### <span data-ttu-id="f8965-133">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="f8965-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f8965-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f8965-134">System.String</span></span>

## <span data-ttu-id="f8965-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8965-135">OUTPUTS</span></span>

### <span data-ttu-id="f8965-136">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="f8965-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="f8965-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8965-137">NOTES</span></span>

## <span data-ttu-id="f8965-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8965-138">RELATED LINKS</span></span>

[<span data-ttu-id="f8965-139">Yeni-Azsız ürün</span><span class="sxs-lookup"><span data-stu-id="f8965-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="f8965-140">Remove-Azapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="f8965-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="f8965-141">Set-Azapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="f8965-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)

