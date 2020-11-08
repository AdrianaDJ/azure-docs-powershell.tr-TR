---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 3d14ef7dca35796baa3e3aecf0c3df98674bfb9b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097703"
---
# <span data-ttu-id="2feba-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2feba-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="2feba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2feba-102">SYNOPSIS</span></span>
<span data-ttu-id="2feba-103">Bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2feba-103">Creates an API Management product.</span></span>

## <span data-ttu-id="2feba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2feba-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2feba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2feba-105">DESCRIPTION</span></span>
<span data-ttu-id="2feba-106">**Yeni-Azapsananagementproduct** cmdlet 'ı bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2feba-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="2feba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2feba-107">EXAMPLES</span></span>

### <span data-ttu-id="2feba-108">Örnek 1: abonelik gerektirmeyen bir ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="2feba-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="2feba-109">Bu komut bir API yönetim ürünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2feba-109">This command creates an API Management product.</span></span>
<span data-ttu-id="2feba-110">Abonelik gerekmez.</span><span class="sxs-lookup"><span data-stu-id="2feba-110">No subscription is required.</span></span>

### <span data-ttu-id="2feba-111">Örnek 2: abonelik ve onay gerektiren bir ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="2feba-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="2feba-112">Bu komut bir ürün oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2feba-112">This command creates a product.</span></span>
<span data-ttu-id="2feba-113">Abonelik ve onay gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2feba-113">A subscription and approval are required.</span></span>
<span data-ttu-id="2feba-114">Bu komut, bildirim dönemini 10 gün olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2feba-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="2feba-115">Abonelik süresi bir yıl olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="2feba-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="2feba-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2feba-116">PARAMETERS</span></span>

### <span data-ttu-id="2feba-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="2feba-117">-ApprovalRequired</span></span>
<span data-ttu-id="2feba-118">Ürünün aboneliğinin onaylanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2feba-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="2feba-119">Varsayılan olarak bu parametre **$false**.</span><span class="sxs-lookup"><span data-stu-id="2feba-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="2feba-120">-Context</span><span class="sxs-lookup"><span data-stu-id="2feba-120">-Context</span></span>
<span data-ttu-id="2feba-121">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2feba-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2feba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2feba-122">-DefaultProfile</span></span>
<span data-ttu-id="2feba-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2feba-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2feba-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="2feba-124">-Description</span></span>
<span data-ttu-id="2feba-125">Ürün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2feba-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="2feba-126">-Yasalda MS</span><span class="sxs-lookup"><span data-stu-id="2feba-126">-LegalTerms</span></span>
<span data-ttu-id="2feba-127">Ürünün yasal kullanım şartlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2feba-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="2feba-128">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="2feba-128">-ProductId</span></span>
<span data-ttu-id="2feba-129">Yeni ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2feba-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="2feba-130">Bu parametreyi belirtmezseniz, yeni bir ürün oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2feba-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="2feba-131">Durumlu</span><span class="sxs-lookup"><span data-stu-id="2feba-131">-State</span></span>
<span data-ttu-id="2feba-132">Ürün durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2feba-132">Specifies the product state.</span></span>
<span data-ttu-id="2feba-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="2feba-133">psdx_paramvalues</span></span>
- <span data-ttu-id="2feba-134">Notyayımlanmadı</span><span class="sxs-lookup"><span data-stu-id="2feba-134">NotPublished</span></span>
- <span data-ttu-id="2feba-135">Yayımlandı varsayılan değer Notyayımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2feba-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="2feba-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="2feba-136">-SubscriptionRequired</span></span>
<span data-ttu-id="2feba-137">Ürünün abonelik gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2feba-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="2feba-138">Varsayılan değer **$true**.</span><span class="sxs-lookup"><span data-stu-id="2feba-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="2feba-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="2feba-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="2feba-140">Eşzamanlı aboneliklerin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2feba-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="2feba-141">Varsayılan değer yok 'Tur.</span><span class="sxs-lookup"><span data-stu-id="2feba-141">The default value is None.</span></span>

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

### <span data-ttu-id="2feba-142">-Başlık</span><span class="sxs-lookup"><span data-stu-id="2feba-142">-Title</span></span>
<span data-ttu-id="2feba-143">Ürün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2feba-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="2feba-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2feba-144">CommonParameters</span></span>
<span data-ttu-id="2feba-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2feba-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2feba-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2feba-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2feba-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2feba-147">INPUTS</span></span>

### <span data-ttu-id="2feba-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="2feba-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2feba-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2feba-149">System.String</span></span>

### <span data-ttu-id="2feba-150">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="2feba-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2feba-151">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="2feba-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2feba-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproductstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="2feba-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2feba-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2feba-153">OUTPUTS</span></span>

### <span data-ttu-id="2feba-154">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="2feba-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="2feba-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2feba-155">NOTES</span></span>

## <span data-ttu-id="2feba-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2feba-156">RELATED LINKS</span></span>

[<span data-ttu-id="2feba-157">Get-Azapsanana,</span><span class="sxs-lookup"><span data-stu-id="2feba-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="2feba-158">Remove-Azapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="2feba-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="2feba-159">Set-Azapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="2feba-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)

