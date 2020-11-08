---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106946"
---
# <span data-ttu-id="a3204-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="a3204-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="a3204-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3204-102">SYNOPSIS</span></span>
<span data-ttu-id="a3204-103">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="a3204-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="a3204-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3204-104">SYNTAX</span></span>

### <span data-ttu-id="a3204-105">Ayarla (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3204-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3204-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a3204-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3204-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a3204-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3204-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3204-108">DESCRIPTION</span></span>
<span data-ttu-id="a3204-109">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="a3204-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="a3204-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3204-110">EXAMPLES</span></span>

### <span data-ttu-id="a3204-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="a3204-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="a3204-112">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="a3204-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="a3204-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3204-113">PARAMETERS</span></span>

### <span data-ttu-id="a3204-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="a3204-114">-OfferId</span></span>
<span data-ttu-id="a3204-115">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a3204-115">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-116">-Tür</span><span class="sxs-lookup"><span data-stu-id="a3204-116">-Type</span></span>
<span data-ttu-id="a3204-117">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="a3204-117">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-118">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="a3204-118">-Tags</span></span>
<span data-ttu-id="a3204-119">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="a3204-119">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a3204-120">-SubscriptionId</span></span>
<span data-ttu-id="a3204-121">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a3204-121">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-122">Durumlu</span><span class="sxs-lookup"><span data-stu-id="a3204-122">-State</span></span>
<span data-ttu-id="a3204-123">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="a3204-123">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-124">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="a3204-124">-TenantId</span></span>
<span data-ttu-id="a3204-125">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a3204-125">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a3204-126">-DisplayName</span></span>
<span data-ttu-id="a3204-127">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="a3204-127">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="a3204-128">-Location</span></span>
<span data-ttu-id="a3204-129">Kaynağın konum olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="a3204-129">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a3204-130">-ResourceId</span></span>
<span data-ttu-id="a3204-131">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3204-131">The resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3204-132">-InputObject</span></span>
<span data-ttu-id="a3204-133">Get-AzsNetworkQuota tarafından döndürülen ağ kotasını da değiştirdi.</span><span class="sxs-lookup"><span data-stu-id="a3204-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3204-134">-WhatIf</span></span>
<span data-ttu-id="a3204-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3204-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3204-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a3204-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="a3204-137">-Confirm</span></span>
<span data-ttu-id="a3204-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a3204-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3204-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3204-139">CommonParameters</span></span>
<span data-ttu-id="a3204-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3204-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3204-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3204-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3204-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3204-142">INPUTS</span></span>

## <span data-ttu-id="a3204-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3204-143">OUTPUTS</span></span>

### <span data-ttu-id="a3204-144">Microsoft. AzureStack. Management. Subscription. modeller. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="a3204-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="a3204-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3204-145">NOTES</span></span>

## <span data-ttu-id="a3204-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3204-146">RELATED LINKS</span></span>
