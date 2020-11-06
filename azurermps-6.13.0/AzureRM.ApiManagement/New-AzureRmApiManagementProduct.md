---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 636a969f6aef013ee947afbb43d398871848818a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592355"
---
# <span data-ttu-id="e3a69-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e3a69-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="e3a69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a69-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a69-103">Bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3a69-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3a69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3a69-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3a69-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3a69-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a69-106">**Yeni-Azurermapsananagementproduct** cmdlet 'ı bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3a69-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="e3a69-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3a69-107">EXAMPLES</span></span>

### <span data-ttu-id="e3a69-108">Örnek 1: abonelik gerektirmeyen bir ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3a69-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="e3a69-109">Bu komut bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3a69-109">This command creates an API Management product.</span></span>
<span data-ttu-id="e3a69-110">Abonelik gerekmez.</span><span class="sxs-lookup"><span data-stu-id="e3a69-110">No subscription is required.</span></span>

### <span data-ttu-id="e3a69-111">Örnek 2: abonelik ve onay gerektiren bir ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="e3a69-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="e3a69-112">Bu komut bir ürün oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3a69-112">This command creates a product.</span></span>
<span data-ttu-id="e3a69-113">Abonelik ve onay gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-113">A subscription and approval are required.</span></span>
<span data-ttu-id="e3a69-114">Bu komut, bildirim dönemini 10 gün olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e3a69-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="e3a69-115">Abonelik süresi bir yıl olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e3a69-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="e3a69-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3a69-116">PARAMETERS</span></span>

### <span data-ttu-id="e3a69-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="e3a69-117">-ApprovalRequired</span></span>
<span data-ttu-id="e3a69-118">Ürünün aboneliğinin onaylanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="e3a69-119">Varsayılan olarak bu parametre **$false**.</span><span class="sxs-lookup"><span data-stu-id="e3a69-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="e3a69-120">-Context</span><span class="sxs-lookup"><span data-stu-id="e3a69-120">-Context</span></span>
<span data-ttu-id="e3a69-121">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e3a69-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a69-122">-DefaultProfile</span></span>
<span data-ttu-id="e3a69-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3a69-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3a69-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e3a69-124">-Description</span></span>
<span data-ttu-id="e3a69-125">Ürün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="e3a69-126">-Yasalda MS</span><span class="sxs-lookup"><span data-stu-id="e3a69-126">-LegalTerms</span></span>
<span data-ttu-id="e3a69-127">Ürünün yasal kullanım şartlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="e3a69-128">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="e3a69-128">-ProductId</span></span>
<span data-ttu-id="e3a69-129">Yeni ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="e3a69-130">Bu parametreyi belirtmezseniz, yeni bir ürün oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e3a69-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="e3a69-131">Durumlu</span><span class="sxs-lookup"><span data-stu-id="e3a69-131">-State</span></span>
<span data-ttu-id="e3a69-132">Ürün durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-132">Specifies the product state.</span></span>
<span data-ttu-id="e3a69-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="e3a69-133">psdx_paramvalues</span></span>
- <span data-ttu-id="e3a69-134">Notyayımlanmadı</span><span class="sxs-lookup"><span data-stu-id="e3a69-134">NotPublished</span></span>
- <span data-ttu-id="e3a69-135">Yayımlandı varsayılan değer Notyayımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="e3a69-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="e3a69-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="e3a69-136">-SubscriptionRequired</span></span>
<span data-ttu-id="e3a69-137">Ürünün abonelik gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="e3a69-138">Varsayılan değer **$true**.</span><span class="sxs-lookup"><span data-stu-id="e3a69-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="e3a69-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="e3a69-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="e3a69-140">Eşzamanlı aboneliklerin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="e3a69-141">Varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-141">The default value is 1.</span></span>

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

### <span data-ttu-id="e3a69-142">-Başlık</span><span class="sxs-lookup"><span data-stu-id="e3a69-142">-Title</span></span>
<span data-ttu-id="e3a69-143">Ürün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3a69-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="e3a69-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a69-144">CommonParameters</span></span>
<span data-ttu-id="e3a69-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3a69-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a69-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a69-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a69-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3a69-147">INPUTS</span></span>

### <span data-ttu-id="e3a69-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e3a69-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e3a69-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e3a69-149">System.String</span></span>

### <span data-ttu-id="e3a69-150">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e3a69-150">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e3a69-151">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e3a69-151">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e3a69-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproductstate, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="e3a69-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e3a69-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3a69-153">OUTPUTS</span></span>

### <span data-ttu-id="e3a69-154">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="e3a69-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="e3a69-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3a69-155">NOTES</span></span>

## <span data-ttu-id="e3a69-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3a69-156">RELATED LINKS</span></span>

[<span data-ttu-id="e3a69-157">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="e3a69-157">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e3a69-158">Remove-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="e3a69-158">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e3a69-159">Set-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="e3a69-159">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


