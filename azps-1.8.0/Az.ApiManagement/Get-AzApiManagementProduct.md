---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9b2eb9f45f04b858e0773215ee1ed9fd98f20ff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751152"
---
# <span data-ttu-id="54c09-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="54c09-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="54c09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54c09-102">SYNOPSIS</span></span>
<span data-ttu-id="54c09-103">Bir listeyi veya belirli bir ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="54c09-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="54c09-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54c09-104">SYNTAX</span></span>

### <span data-ttu-id="54c09-105">GetAllProducts (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54c09-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54c09-106">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="54c09-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54c09-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="54c09-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54c09-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="54c09-108">DESCRIPTION</span></span>
<span data-ttu-id="54c09-109">**Get-Azapsananagementproduct** cmdlet 'i bir liste veya belirli bir ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="54c09-109">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="54c09-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54c09-110">EXAMPLES</span></span>

### <span data-ttu-id="54c09-111">Örnek 1: tüm ürünleri alma</span><span class="sxs-lookup"><span data-stu-id="54c09-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="54c09-112">Bu komut tüm API yönetim ürünlerini alır.</span><span class="sxs-lookup"><span data-stu-id="54c09-112">This command get all API Management products.</span></span>

### <span data-ttu-id="54c09-113">Örnek 2: KIMLIĞE göre ürün alma</span><span class="sxs-lookup"><span data-stu-id="54c09-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="54c09-114">Bu komut, KIMLIĞE göre bir API yönetim ürünü alır.</span><span class="sxs-lookup"><span data-stu-id="54c09-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="54c09-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54c09-115">PARAMETERS</span></span>

### <span data-ttu-id="54c09-116">-Context</span><span class="sxs-lookup"><span data-stu-id="54c09-116">-Context</span></span>
<span data-ttu-id="54c09-117">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c09-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="54c09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c09-118">-DefaultProfile</span></span>
<span data-ttu-id="54c09-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54c09-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54c09-120">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="54c09-120">-ProductId</span></span>
<span data-ttu-id="54c09-121">Aranacak ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c09-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="54c09-122">-Başlık</span><span class="sxs-lookup"><span data-stu-id="54c09-122">-Title</span></span>
<span data-ttu-id="54c09-123">Bakılacak ürünün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54c09-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="54c09-124">Belirtilmişse, cmdlet ürünü başlığa göre almayı dener.</span><span class="sxs-lookup"><span data-stu-id="54c09-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="54c09-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c09-125">CommonParameters</span></span>
<span data-ttu-id="54c09-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54c09-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c09-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c09-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c09-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54c09-128">INPUTS</span></span>

### <span data-ttu-id="54c09-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="54c09-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="54c09-130">System. String</span><span class="sxs-lookup"><span data-stu-id="54c09-130">System.String</span></span>

## <span data-ttu-id="54c09-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54c09-131">OUTPUTS</span></span>

### <span data-ttu-id="54c09-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="54c09-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="54c09-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54c09-133">NOTES</span></span>

## <span data-ttu-id="54c09-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54c09-134">RELATED LINKS</span></span>

[<span data-ttu-id="54c09-135">Yeni-Azsız ürün</span><span class="sxs-lookup"><span data-stu-id="54c09-135">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="54c09-136">Remove-Azapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="54c09-136">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="54c09-137">Set-Azapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="54c09-137">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


