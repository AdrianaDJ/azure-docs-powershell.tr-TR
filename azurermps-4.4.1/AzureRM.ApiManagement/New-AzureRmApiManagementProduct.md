---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: a978fce4d44a061796597f2f3ae08c78c1021bdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591217"
---
# <span data-ttu-id="5923b-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5923b-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="5923b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5923b-102">SYNOPSIS</span></span>
<span data-ttu-id="5923b-103">Bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5923b-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5923b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5923b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5923b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5923b-105">DESCRIPTION</span></span>
<span data-ttu-id="5923b-106">**Yeni-Azurermapsananagementproduct** cmdlet 'ı bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5923b-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="5923b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5923b-107">EXAMPLES</span></span>

### <span data-ttu-id="5923b-108">Örnek 1: abonelik gerektirmeyen bir ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="5923b-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="5923b-109">Bu komut bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5923b-109">This command creates an API Management product.</span></span>
<span data-ttu-id="5923b-110">Abonelik gerekmez.</span><span class="sxs-lookup"><span data-stu-id="5923b-110">No subscription is required.</span></span>

### <span data-ttu-id="5923b-111">Örnek 2: abonelik ve onay gerektiren bir ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="5923b-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="5923b-112">Bu komut bir ürün oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5923b-112">This command creates a product.</span></span>
<span data-ttu-id="5923b-113">Abonelik ve onay gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5923b-113">A subscription and approval are required.</span></span>
<span data-ttu-id="5923b-114">Bu komut, bildirim dönemini 10 gün olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5923b-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="5923b-115">Abonelik süresi bir yıl olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5923b-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="5923b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5923b-116">PARAMETERS</span></span>

### <span data-ttu-id="5923b-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="5923b-117">-ApprovalRequired</span></span>
<span data-ttu-id="5923b-118">Ürünün aboneliğinin onaylanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5923b-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="5923b-119">Varsayılan olarak bu parametre **$false**.</span><span class="sxs-lookup"><span data-stu-id="5923b-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="5923b-120">-Context</span><span class="sxs-lookup"><span data-stu-id="5923b-120">-Context</span></span>
<span data-ttu-id="5923b-121">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5923b-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5923b-122">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="5923b-122">-Description</span></span>
<span data-ttu-id="5923b-123">Ürün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5923b-123">Specifies the product description.</span></span>

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

### <span data-ttu-id="5923b-124">-Yasalda MS</span><span class="sxs-lookup"><span data-stu-id="5923b-124">-LegalTerms</span></span>
<span data-ttu-id="5923b-125">Ürünün yasal kullanım şartlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5923b-125">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="5923b-126">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="5923b-126">-ProductId</span></span>
<span data-ttu-id="5923b-127">Yeni ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5923b-127">Specifies the identifier of new product.</span></span>
<span data-ttu-id="5923b-128">Bu parametreyi belirtmezseniz, yeni bir ürün oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5923b-128">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="5923b-129">Durumlu</span><span class="sxs-lookup"><span data-stu-id="5923b-129">-State</span></span>
<span data-ttu-id="5923b-130">Ürün durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5923b-130">Specifies the product state.</span></span>
<span data-ttu-id="5923b-131">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="5923b-131">psdx_paramvalues</span></span>

- <span data-ttu-id="5923b-132">Notyayımlanmadı</span><span class="sxs-lookup"><span data-stu-id="5923b-132">NotPublished</span></span>
- <span data-ttu-id="5923b-133">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="5923b-133">Published</span></span> 

<span data-ttu-id="5923b-134">Varsayılan değer Notyayınlandı.</span><span class="sxs-lookup"><span data-stu-id="5923b-134">The default value is NotPublished.</span></span>

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

### <span data-ttu-id="5923b-135">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="5923b-135">-SubscriptionRequired</span></span>
<span data-ttu-id="5923b-136">Ürünün abonelik gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5923b-136">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="5923b-137">Varsayılan değer **$true**.</span><span class="sxs-lookup"><span data-stu-id="5923b-137">The default value is **$True**.</span></span>

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

### <span data-ttu-id="5923b-138">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="5923b-138">-SubscriptionsLimit</span></span>
<span data-ttu-id="5923b-139">Eşzamanlı aboneliklerin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5923b-139">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="5923b-140">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="5923b-140">The default value is 1.</span></span>

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

### <span data-ttu-id="5923b-141">-Başlık</span><span class="sxs-lookup"><span data-stu-id="5923b-141">-Title</span></span>
<span data-ttu-id="5923b-142">Ürün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5923b-142">Specifies the product title.</span></span>

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

### <span data-ttu-id="5923b-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5923b-143">-DefaultProfile</span></span>
<span data-ttu-id="5923b-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5923b-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5923b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5923b-145">CommonParameters</span></span>
<span data-ttu-id="5923b-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5923b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5923b-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5923b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5923b-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5923b-148">INPUTS</span></span>

## <span data-ttu-id="5923b-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5923b-149">OUTPUTS</span></span>

### <span data-ttu-id="5923b-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="5923b-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="5923b-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5923b-151">NOTES</span></span>

## <span data-ttu-id="5923b-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5923b-152">RELATED LINKS</span></span>

[<span data-ttu-id="5923b-153">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="5923b-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="5923b-154">Remove-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="5923b-154">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="5923b-155">Set-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="5923b-155">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


