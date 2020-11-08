---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275914"
---
# <span data-ttu-id="5f7cb-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="5f7cb-101">New-AzReservation</span></span>

## <span data-ttu-id="5f7cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f7cb-102">SYNOPSIS</span></span>
<span data-ttu-id="5f7cb-103">Bir ayırma satın alma</span><span class="sxs-lookup"><span data-stu-id="5f7cb-103">Purchase a reservation</span></span>

## <span data-ttu-id="5f7cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f7cb-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f7cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f7cb-105">DESCRIPTION</span></span>
<span data-ttu-id="5f7cb-106">Bir ayırma örneği satın alın ve avantaj alın</span><span class="sxs-lookup"><span data-stu-id="5f7cb-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="5f7cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f7cb-107">EXAMPLES</span></span>

### <span data-ttu-id="5f7cb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5f7cb-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="5f7cb-109">Fiyat hesaplandıktan sonra, müşteri calculatePrice tarafından sağlanan</span><span class="sxs-lookup"><span data-stu-id="5f7cb-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="5f7cb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f7cb-110">PARAMETERS</span></span>

### <span data-ttu-id="5f7cb-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="5f7cb-111">-AppliedScope</span></span>
<span data-ttu-id="5f7cb-112">Avantajın uygulanacağı abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="5f7cb-113">Gerekli If--uygulandı-Scope-Type Single.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="5f7cb-114">Eğer-odaklı kapsam türünün paylaşılıp paylaşıldığını belirtme.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="5f7cb-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="5f7cb-115">-AppliedScopeType</span></span>
<span data-ttu-id="5f7cb-116">Ayırmayı "tek" veya "paylaşılan" ile güncelleştirmek için uygulanan kapsamın türü</span><span class="sxs-lookup"><span data-stu-id="5f7cb-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="5f7cb-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="5f7cb-117">-BillingPlan</span></span>
<span data-ttu-id="5f7cb-118">Bu SKU için sağlanan faturalandırma planı seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="5f7cb-119">"Aylık" veya "upfront"</span><span class="sxs-lookup"><span data-stu-id="5f7cb-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="5f7cb-120">-Billingscopeıd</span><span class="sxs-lookup"><span data-stu-id="5f7cb-120">-BillingScopeId</span></span>
<span data-ttu-id="5f7cb-121">Rezervasyon satın almak için ücretlendirilecek abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="5f7cb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f7cb-122">-DefaultProfile</span></span>
<span data-ttu-id="5f7cb-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f7cb-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5f7cb-124">-DisplayName</span></span>
<span data-ttu-id="5f7cb-125">Ayırmayı kolayca belirleyebilmesini sağlayan kolay ad.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="5f7cb-126">-Instanceesnekliği</span><span class="sxs-lookup"><span data-stu-id="5f7cb-126">-InstanceFlexibility</span></span>
<span data-ttu-id="5f7cb-127">{{Fill ınstanceesnekliği açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="5f7cb-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="5f7cb-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="5f7cb-128">-Location</span></span>
<span data-ttu-id="5f7cb-129">SKU 'nun uygun olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="5f7cb-130">-Miktar</span><span class="sxs-lookup"><span data-stu-id="5f7cb-130">-Quantity</span></span>
<span data-ttu-id="5f7cb-131">Fiyat veya satınalma hesaplaması için ürün miktarı.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="5f7cb-132">-Yenileme</span><span class="sxs-lookup"><span data-stu-id="5f7cb-132">-Renew</span></span>
<span data-ttu-id="5f7cb-133">Bunu doğruya ayarla son kullanma tarihi tarihinde otomatik olarak yeni bir rezervasyon satın alacaktır.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="5f7cb-134">-Rezervationorderıd</span><span class="sxs-lookup"><span data-stu-id="5f7cb-134">-ReservationOrderId</span></span>
<span data-ttu-id="5f7cb-135">Satın alınacak rezervasyon siparişinin ID, az rezervasyon rezervasyonu-sipariş hesaplaması.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="5f7cb-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="5f7cb-136">-ReservedResourceType</span></span>
<span data-ttu-id="5f7cb-137">SKU 'ların sağlanması gereken kaynağın türü.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="5f7cb-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="5f7cb-138">-Sku</span></span>
<span data-ttu-id="5f7cb-139">SKU adı</span><span class="sxs-lookup"><span data-stu-id="5f7cb-139">Sku name</span></span>

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

### <span data-ttu-id="5f7cb-140">Süreli</span><span class="sxs-lookup"><span data-stu-id="5f7cb-140">-Term</span></span>
<span data-ttu-id="5f7cb-141">Bu kaynak için kullanılabilir ayırma şartları.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="5f7cb-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f7cb-142">-Confirm</span></span>
<span data-ttu-id="5f7cb-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f7cb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f7cb-144">-WhatIf</span></span>
<span data-ttu-id="5f7cb-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f7cb-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f7cb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f7cb-147">CommonParameters</span></span>
<span data-ttu-id="5f7cb-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f7cb-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f7cb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f7cb-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f7cb-150">INPUTS</span></span>

### <span data-ttu-id="5f7cb-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5f7cb-151">None</span></span>

## <span data-ttu-id="5f7cb-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f7cb-152">OUTPUTS</span></span>

### <span data-ttu-id="5f7cb-153">Microsoft. Azure. Management. rezervasyonlar. modeller. Rezervlerorderresponse</span><span class="sxs-lookup"><span data-stu-id="5f7cb-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="5f7cb-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f7cb-154">NOTES</span></span>

## <span data-ttu-id="5f7cb-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f7cb-155">RELATED LINKS</span></span>
