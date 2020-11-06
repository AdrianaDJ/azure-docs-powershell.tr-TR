---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572505"
---
# <span data-ttu-id="63fed-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="63fed-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="63fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63fed-102">SYNOPSIS</span></span>
<span data-ttu-id="63fed-103">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="63fed-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="63fed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63fed-104">SYNTAX</span></span>

### <span data-ttu-id="63fed-105">Ayarla (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63fed-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63fed-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="63fed-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fed-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="63fed-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63fed-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="63fed-108">DESCRIPTION</span></span>
<span data-ttu-id="63fed-109">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="63fed-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="63fed-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63fed-110">EXAMPLES</span></span>

### <span data-ttu-id="63fed-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="63fed-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="63fed-112">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="63fed-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="63fed-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63fed-113">PARAMETERS</span></span>

### <span data-ttu-id="63fed-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="63fed-114">-DisplayName</span></span>
<span data-ttu-id="63fed-115">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="63fed-115">Subscription name.</span></span>

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

### <span data-ttu-id="63fed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63fed-116">-InputObject</span></span>
<span data-ttu-id="63fed-117">Get-AzsNetworkQuota tarafından döndürülen ağ kotasını da değiştirdi.</span><span class="sxs-lookup"><span data-stu-id="63fed-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="63fed-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="63fed-118">-Location</span></span>
<span data-ttu-id="63fed-119">Kaynağın konum olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="63fed-119">Location where resource is location.</span></span>

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

### <span data-ttu-id="63fed-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="63fed-120">-OfferId</span></span>
<span data-ttu-id="63fed-121">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="63fed-121">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="63fed-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="63fed-122">-ResourceId</span></span>
<span data-ttu-id="63fed-123">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="63fed-123">The resource ID.</span></span>

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

### <span data-ttu-id="63fed-124">Durumlu</span><span class="sxs-lookup"><span data-stu-id="63fed-124">-State</span></span>
<span data-ttu-id="63fed-125">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="63fed-125">Subscription state.</span></span>

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

### <span data-ttu-id="63fed-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="63fed-126">-SubscriptionId</span></span>
<span data-ttu-id="63fed-127">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="63fed-127">Subscription identifier.</span></span>

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

### <span data-ttu-id="63fed-128">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="63fed-128">-Tags</span></span>
<span data-ttu-id="63fed-129">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="63fed-129">List of key-value pairs.</span></span>

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

### <span data-ttu-id="63fed-130">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="63fed-130">-TenantId</span></span>
<span data-ttu-id="63fed-131">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="63fed-131">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="63fed-132">-Tür</span><span class="sxs-lookup"><span data-stu-id="63fed-132">-Type</span></span>
<span data-ttu-id="63fed-133">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="63fed-133">Type of resource.</span></span>

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

### <span data-ttu-id="63fed-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="63fed-134">-Confirm</span></span>
<span data-ttu-id="63fed-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63fed-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63fed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63fed-136">-WhatIf</span></span>
<span data-ttu-id="63fed-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63fed-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63fed-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63fed-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63fed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fed-139">CommonParameters</span></span>
<span data-ttu-id="63fed-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63fed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fed-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fed-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fed-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63fed-142">INPUTS</span></span>

## <span data-ttu-id="63fed-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63fed-143">OUTPUTS</span></span>

### <span data-ttu-id="63fed-144">Microsoft. AzureStack. Management. Subscription. modeller. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="63fed-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="63fed-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63fed-145">NOTES</span></span>

## <span data-ttu-id="63fed-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63fed-146">RELATED LINKS</span></span>

