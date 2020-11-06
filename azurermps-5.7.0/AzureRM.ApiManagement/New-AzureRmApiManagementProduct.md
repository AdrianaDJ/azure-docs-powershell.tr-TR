---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 673aa943263a789e7d8be0a63634ddd176e09cae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586844"
---
# <span data-ttu-id="9763a-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9763a-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="9763a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9763a-102">SYNOPSIS</span></span>
<span data-ttu-id="9763a-103">Bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9763a-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9763a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9763a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9763a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9763a-105">DESCRIPTION</span></span>
<span data-ttu-id="9763a-106">**Yeni-Azurermapsananagementproduct** cmdlet 'ı bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9763a-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="9763a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9763a-107">EXAMPLES</span></span>

### <span data-ttu-id="9763a-108">Örnek 1: abonelik gerektirmeyen bir ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="9763a-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="9763a-109">Bu komut bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9763a-109">This command creates an API Management product.</span></span>
<span data-ttu-id="9763a-110">Abonelik gerekmez.</span><span class="sxs-lookup"><span data-stu-id="9763a-110">No subscription is required.</span></span>

### <span data-ttu-id="9763a-111">Örnek 2: abonelik ve onay gerektiren bir ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="9763a-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="9763a-112">Bu komut bir ürün oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9763a-112">This command creates a product.</span></span>
<span data-ttu-id="9763a-113">Abonelik ve onay gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9763a-113">A subscription and approval are required.</span></span>
<span data-ttu-id="9763a-114">Bu komut, bildirim dönemini 10 gün olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9763a-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="9763a-115">Abonelik süresi bir yıl olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9763a-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="9763a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9763a-116">PARAMETERS</span></span>

### <span data-ttu-id="9763a-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="9763a-117">-ApprovalRequired</span></span>
<span data-ttu-id="9763a-118">Ürünün aboneliğinin onaylanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9763a-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="9763a-119">Varsayılan olarak bu parametre **$false**.</span><span class="sxs-lookup"><span data-stu-id="9763a-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="9763a-120">-Context</span><span class="sxs-lookup"><span data-stu-id="9763a-120">-Context</span></span>
<span data-ttu-id="9763a-121">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9763a-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9763a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9763a-122">-DefaultProfile</span></span>
<span data-ttu-id="9763a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9763a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="9763a-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9763a-124">-Description</span></span>
<span data-ttu-id="9763a-125">Ürün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9763a-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="9763a-126">-Yasalda MS</span><span class="sxs-lookup"><span data-stu-id="9763a-126">-LegalTerms</span></span>
<span data-ttu-id="9763a-127">Ürünün yasal kullanım şartlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9763a-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="9763a-128">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="9763a-128">-ProductId</span></span>
<span data-ttu-id="9763a-129">Yeni ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9763a-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="9763a-130">Bu parametreyi belirtmezseniz, yeni bir ürün oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9763a-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="9763a-131">Durumlu</span><span class="sxs-lookup"><span data-stu-id="9763a-131">-State</span></span>
<span data-ttu-id="9763a-132">Ürün durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9763a-132">Specifies the product state.</span></span>
<span data-ttu-id="9763a-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="9763a-133">psdx_paramvalues</span></span>

- <span data-ttu-id="9763a-134">Notyayımlanmadı</span><span class="sxs-lookup"><span data-stu-id="9763a-134">NotPublished</span></span>
- <span data-ttu-id="9763a-135">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="9763a-135">Published</span></span> 

<span data-ttu-id="9763a-136">Varsayılan değer Notyayınlandı.</span><span class="sxs-lookup"><span data-stu-id="9763a-136">The default value is NotPublished.</span></span>

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

### <span data-ttu-id="9763a-137">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="9763a-137">-SubscriptionRequired</span></span>
<span data-ttu-id="9763a-138">Ürünün abonelik gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9763a-138">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="9763a-139">Varsayılan değer **$true**.</span><span class="sxs-lookup"><span data-stu-id="9763a-139">The default value is **$True**.</span></span>

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

### <span data-ttu-id="9763a-140">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="9763a-140">-SubscriptionsLimit</span></span>
<span data-ttu-id="9763a-141">Eşzamanlı aboneliklerin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9763a-141">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="9763a-142">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="9763a-142">The default value is 1.</span></span>

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

### <span data-ttu-id="9763a-143">-Başlık</span><span class="sxs-lookup"><span data-stu-id="9763a-143">-Title</span></span>
<span data-ttu-id="9763a-144">Ürün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9763a-144">Specifies the product title.</span></span>

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

### <span data-ttu-id="9763a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9763a-145">CommonParameters</span></span>
<span data-ttu-id="9763a-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9763a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9763a-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9763a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9763a-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9763a-148">INPUTS</span></span>

### <span data-ttu-id="9763a-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9763a-149">None</span></span>
<span data-ttu-id="9763a-150">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9763a-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9763a-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9763a-151">OUTPUTS</span></span>

### <span data-ttu-id="9763a-152">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="9763a-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="9763a-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9763a-153">NOTES</span></span>

## <span data-ttu-id="9763a-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9763a-154">RELATED LINKS</span></span>

[<span data-ttu-id="9763a-155">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="9763a-155">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="9763a-156">Remove-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="9763a-156">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="9763a-157">Set-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="9763a-157">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


