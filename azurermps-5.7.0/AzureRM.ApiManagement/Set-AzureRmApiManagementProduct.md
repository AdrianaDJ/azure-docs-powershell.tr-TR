---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: b050b55c978313cf038e8a27d5be0f7ad722905b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764733"
---
# <span data-ttu-id="e2403-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e2403-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="e2403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2403-102">SYNOPSIS</span></span>
<span data-ttu-id="e2403-103">API yönetimi ürün ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e2403-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2403-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2403-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2403-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2403-105">DESCRIPTION</span></span>
<span data-ttu-id="e2403-106">**Set-Azurermapsananagementproduct** cmdlet 'ı, API yönetimi ürün ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e2403-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="e2403-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2403-107">EXAMPLES</span></span>

### <span data-ttu-id="e2403-108">Örnek 1: ürün ayrıntılarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e2403-108">Example 1: Update the product details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="e2403-109">Bu komut API yönetimi ürün ayrıntılarını güncelleştirir, bir abonelik gerektirir ve sonra yayımdan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e2403-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="e2403-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2403-110">PARAMETERS</span></span>

### <span data-ttu-id="e2403-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="e2403-111">-ApprovalRequired</span></span>
<span data-ttu-id="e2403-112">Ürün aboneliğinin onaylanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2403-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="e2403-113">Varsayılan değer **$false**.</span><span class="sxs-lookup"><span data-stu-id="e2403-113">The default value is **$False**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2403-114">-Context</span><span class="sxs-lookup"><span data-stu-id="e2403-114">-Context</span></span>
<span data-ttu-id="e2403-115">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2403-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e2403-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2403-116">-DefaultProfile</span></span>
<span data-ttu-id="e2403-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2403-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e2403-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e2403-118">-Description</span></span>
<span data-ttu-id="e2403-119">Ürün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2403-119">Specifies the product description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2403-120">-Yasalda MS</span><span class="sxs-lookup"><span data-stu-id="e2403-120">-LegalTerms</span></span>
<span data-ttu-id="e2403-121">Ürünün yasal kullanım şartlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2403-121">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2403-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e2403-122">-PassThru</span></span>
<span data-ttu-id="e2403-123">geçiş</span><span class="sxs-lookup"><span data-stu-id="e2403-123">passthru</span></span>

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

### <span data-ttu-id="e2403-124">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="e2403-124">-ProductId</span></span>
<span data-ttu-id="e2403-125">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2403-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="e2403-126">Durumlu</span><span class="sxs-lookup"><span data-stu-id="e2403-126">-State</span></span>
<span data-ttu-id="e2403-127">Ürün durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2403-127">Specifies the product state.</span></span>
<span data-ttu-id="e2403-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="e2403-128">psdx_paramvalues</span></span>

- <span data-ttu-id="e2403-129">Notyayımlanmadı</span><span class="sxs-lookup"><span data-stu-id="e2403-129">NotPublished</span></span>
- <span data-ttu-id="e2403-130">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="e2403-130">Published</span></span>

```yaml
Type: PsApiManagementProductState
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2403-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="e2403-131">-SubscriptionRequired</span></span>
<span data-ttu-id="e2403-132">Ürünün abonelik gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2403-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="e2403-133">Bu parametrenin varsayılan değeri **$true**.</span><span class="sxs-lookup"><span data-stu-id="e2403-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2403-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="e2403-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="e2403-135">Eşzamanlı aboneliklerin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2403-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="e2403-136">Bu parametre için varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="e2403-136">The default value for this parameter is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2403-137">-Başlık</span><span class="sxs-lookup"><span data-stu-id="e2403-137">-Title</span></span>
<span data-ttu-id="e2403-138">Bu cmdlet kümelerinin ürün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e2403-138">Specifies the product title this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2403-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2403-139">CommonParameters</span></span>
<span data-ttu-id="e2403-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2403-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2403-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2403-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2403-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2403-142">INPUTS</span></span>

### <span data-ttu-id="e2403-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e2403-143">None</span></span>
<span data-ttu-id="e2403-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e2403-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e2403-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2403-145">OUTPUTS</span></span>

### <span data-ttu-id="e2403-146">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="e2403-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="e2403-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2403-147">NOTES</span></span>

## <span data-ttu-id="e2403-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2403-148">RELATED LINKS</span></span>

[<span data-ttu-id="e2403-149">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="e2403-149">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e2403-150">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="e2403-150">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e2403-151">Remove-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="e2403-151">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


