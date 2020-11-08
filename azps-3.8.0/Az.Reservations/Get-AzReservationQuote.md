---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096794"
---
# <span data-ttu-id="f50c7-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="f50c7-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="f50c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f50c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f50c7-103">{{Synopsis} doldurun}}</span><span class="sxs-lookup"><span data-stu-id="f50c7-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="f50c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f50c7-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f50c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f50c7-105">DESCRIPTION</span></span>
<span data-ttu-id="f50c7-106">Rezervasyon siparişi yerleştirmek için fiyatı hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="f50c7-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="f50c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f50c7-107">EXAMPLES</span></span>

### <span data-ttu-id="f50c7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f50c7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="f50c7-109">Katalog aldıktan sonra, müşteri bu ürünü konuma göre alabilir.</span><span class="sxs-lookup"><span data-stu-id="f50c7-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="f50c7-110">Bu bilgileri kullanarak fiyatı uygun şekilde denetleyin</span><span class="sxs-lookup"><span data-stu-id="f50c7-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="f50c7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f50c7-111">PARAMETERS</span></span>

### <span data-ttu-id="f50c7-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="f50c7-112">-AppliedScope</span></span>
<span data-ttu-id="f50c7-113">Avantajın uygulanacağı abonelik.</span><span class="sxs-lookup"><span data-stu-id="f50c7-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="f50c7-114">Gerekli If--uygulandı-Scope-Type Single.</span><span class="sxs-lookup"><span data-stu-id="f50c7-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="f50c7-115">Eğer-odaklı kapsam türünün paylaşılıp paylaşıldığını belirtme.</span><span class="sxs-lookup"><span data-stu-id="f50c7-115">Do not specify if --applied-scope-type is Shared.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="f50c7-116">-AppliedScopeType</span></span>
<span data-ttu-id="f50c7-117">Ayırmayı "tek" veya "paylaşılan" ile güncelleştirmek için uygulanan kapsamın türü</span><span class="sxs-lookup"><span data-stu-id="f50c7-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="f50c7-118">-BillingPlan</span></span>
<span data-ttu-id="f50c7-119">Bu SKU için sağlanan faturalandırma planı seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="f50c7-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="f50c7-120">"Aylık" veya "upfront"</span><span class="sxs-lookup"><span data-stu-id="f50c7-120">"Monthly" or "Upfront"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-121">-Billingscopeıd</span><span class="sxs-lookup"><span data-stu-id="f50c7-121">-BillingScopeId</span></span>
<span data-ttu-id="f50c7-122">Rezervasyon satın almak için ücretlendirilecek abonelik.</span><span class="sxs-lookup"><span data-stu-id="f50c7-122">Subscription that will be charged for purchasing Reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f50c7-123">-DefaultProfile</span></span>
<span data-ttu-id="f50c7-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f50c7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f50c7-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f50c7-125">-DisplayName</span></span>
<span data-ttu-id="f50c7-126">Ayırmayı kolayca belirleyebilmesini sağlayan kolay ad.</span><span class="sxs-lookup"><span data-stu-id="f50c7-126">Friendly name for user to easily identified the reservation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-127">-Instanceesnekliği</span><span class="sxs-lookup"><span data-stu-id="f50c7-127">-InstanceFlexibility</span></span>
<span data-ttu-id="f50c7-128">Ayırmayı güncelleştirmek için örnek esnekliği türü.</span><span class="sxs-lookup"><span data-stu-id="f50c7-128">Type of the Instance Flexibility to update the reservation with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="f50c7-129">-Location</span></span>
<span data-ttu-id="f50c7-130">SKU 'nun uygun olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="f50c7-130">Location that the SKU is available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-131">-Miktar</span><span class="sxs-lookup"><span data-stu-id="f50c7-131">-Quantity</span></span>
<span data-ttu-id="f50c7-132">Fiyat veya satınalma hesaplaması için ürün miktarı.</span><span class="sxs-lookup"><span data-stu-id="f50c7-132">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-133">-Yenileme</span><span class="sxs-lookup"><span data-stu-id="f50c7-133">-Renew</span></span>
<span data-ttu-id="f50c7-134">Bunu doğruya ayarla son kullanma tarihi tarihinde otomatik olarak yeni bir rezervasyon satın alacaktır.</span><span class="sxs-lookup"><span data-stu-id="f50c7-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="f50c7-135">-ReservedResourceType</span></span>
<span data-ttu-id="f50c7-136">SKU 'ların sağlanması gereken kaynağın türü.</span><span class="sxs-lookup"><span data-stu-id="f50c7-136">Type of the resource for which the skus should be provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="f50c7-137">-Sku</span></span>
<span data-ttu-id="f50c7-138">SKU adı, şu komutu kullanarak SKU listesini alma az rezervasyonlar Katalog gösterisi</span><span class="sxs-lookup"><span data-stu-id="f50c7-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-139">Süreli</span><span class="sxs-lookup"><span data-stu-id="f50c7-139">-Term</span></span>
<span data-ttu-id="f50c7-140">Bu kaynak için kullanılabilir ayırma şartları.</span><span class="sxs-lookup"><span data-stu-id="f50c7-140">Available reservation terms for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f50c7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f50c7-141">CommonParameters</span></span>
<span data-ttu-id="f50c7-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f50c7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f50c7-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f50c7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f50c7-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f50c7-144">INPUTS</span></span>

### <span data-ttu-id="f50c7-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f50c7-145">None</span></span>

## <span data-ttu-id="f50c7-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f50c7-146">OUTPUTS</span></span>

### <span data-ttu-id="f50c7-147">Microsoft. Azure. Management. rezervasyonlar. modeller. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="f50c7-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="f50c7-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f50c7-148">NOTES</span></span>

## <span data-ttu-id="f50c7-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f50c7-149">RELATED LINKS</span></span>