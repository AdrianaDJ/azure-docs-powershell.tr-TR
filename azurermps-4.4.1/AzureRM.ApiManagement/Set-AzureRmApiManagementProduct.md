---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: dac6e48faba1590897161ab59fed05f1f0b331df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591208"
---
# <span data-ttu-id="2b95c-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2b95c-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="2b95c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b95c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b95c-103">API yönetimi ürün ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2b95c-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b95c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b95c-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b95c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b95c-105">DESCRIPTION</span></span>
<span data-ttu-id="2b95c-106">**Set-Azurermapsananagementproduct** cmdlet 'ı, API yönetimi ürün ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2b95c-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="2b95c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b95c-107">EXAMPLES</span></span>

### <span data-ttu-id="2b95c-108">Örnek 1: ürün ayrıntılarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2b95c-108">Example 1: Update the product details</span></span>
```
PS C:\>Set-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="2b95c-109">Bu komut API yönetimi ürün ayrıntılarını güncelleştirir, bir abonelik gerektirir ve sonra yayımdan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2b95c-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="2b95c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b95c-110">PARAMETERS</span></span>

### <span data-ttu-id="2b95c-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="2b95c-111">-ApprovalRequired</span></span>
<span data-ttu-id="2b95c-112">Ürün aboneliğinin onaylanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="2b95c-113">Varsayılan değer **$false**.</span><span class="sxs-lookup"><span data-stu-id="2b95c-113">The default value is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b95c-114">-Context</span><span class="sxs-lookup"><span data-stu-id="2b95c-114">-Context</span></span>
<span data-ttu-id="2b95c-115">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2b95c-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="2b95c-116">-Description</span></span>
<span data-ttu-id="2b95c-117">Ürün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-117">Specifies the product description.</span></span>

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

### <span data-ttu-id="2b95c-118">-Yasalda MS</span><span class="sxs-lookup"><span data-stu-id="2b95c-118">-LegalTerms</span></span>
<span data-ttu-id="2b95c-119">Ürünün yasal kullanım şartlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-119">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="2b95c-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2b95c-120">-PassThru</span></span>
<span data-ttu-id="2b95c-121">geçiş</span><span class="sxs-lookup"><span data-stu-id="2b95c-121">passthru</span></span>

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

### <span data-ttu-id="2b95c-122">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="2b95c-122">-ProductId</span></span>
<span data-ttu-id="2b95c-123">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-123">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="2b95c-124">Durumlu</span><span class="sxs-lookup"><span data-stu-id="2b95c-124">-State</span></span>
<span data-ttu-id="2b95c-125">Ürün durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-125">Specifies the product state.</span></span>
<span data-ttu-id="2b95c-126">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="2b95c-126">psdx_paramvalues</span></span>

- <span data-ttu-id="2b95c-127">Notyayımlanmadı</span><span class="sxs-lookup"><span data-stu-id="2b95c-127">NotPublished</span></span>
- <span data-ttu-id="2b95c-128">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="2b95c-128">Published</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b95c-129">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="2b95c-129">-SubscriptionRequired</span></span>
<span data-ttu-id="2b95c-130">Ürünün abonelik gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-130">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="2b95c-131">Bu parametrenin varsayılan değeri **$true**.</span><span class="sxs-lookup"><span data-stu-id="2b95c-131">The default value for this parameter is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b95c-132">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="2b95c-132">-SubscriptionsLimit</span></span>
<span data-ttu-id="2b95c-133">Eşzamanlı aboneliklerin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-133">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="2b95c-134">Bu parametre için varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-134">The default value for this parameter is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b95c-135">-Başlık</span><span class="sxs-lookup"><span data-stu-id="2b95c-135">-Title</span></span>
<span data-ttu-id="2b95c-136">Bu cmdlet kümelerinin ürün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b95c-136">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="2b95c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b95c-137">-DefaultProfile</span></span>
<span data-ttu-id="2b95c-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b95c-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b95c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b95c-139">CommonParameters</span></span>
<span data-ttu-id="2b95c-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b95c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b95c-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b95c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b95c-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b95c-142">INPUTS</span></span>

## <span data-ttu-id="2b95c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b95c-143">OUTPUTS</span></span>

### <span data-ttu-id="2b95c-144">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="2b95c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="2b95c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b95c-145">NOTES</span></span>

## <span data-ttu-id="2b95c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b95c-146">RELATED LINKS</span></span>

[<span data-ttu-id="2b95c-147">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="2b95c-147">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="2b95c-148">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="2b95c-148">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="2b95c-149">Remove-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="2b95c-149">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


