---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 617a7ac7d949eb54ab08b0d0cb06c0fca3ba79bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761785"
---
# <span data-ttu-id="752c1-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="752c1-101">New-AzsSubscription</span></span>

## <span data-ttu-id="752c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="752c1-102">SYNOPSIS</span></span>
<span data-ttu-id="752c1-103">Abonelik oluşturma.</span><span class="sxs-lookup"><span data-stu-id="752c1-103">Create a subscription.</span></span>

## <span data-ttu-id="752c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="752c1-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="752c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="752c1-105">DESCRIPTION</span></span>
<span data-ttu-id="752c1-106">Abonelik oluşturma.</span><span class="sxs-lookup"><span data-stu-id="752c1-106">Create a subscription.</span></span>

## <span data-ttu-id="752c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="752c1-107">EXAMPLES</span></span>

### <span data-ttu-id="752c1-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="752c1-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="752c1-109">Abonelik oluşturma.</span><span class="sxs-lookup"><span data-stu-id="752c1-109">Create a subscription.</span></span>

## <span data-ttu-id="752c1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="752c1-110">PARAMETERS</span></span>

### <span data-ttu-id="752c1-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="752c1-111">-DisplayName</span></span>
<span data-ttu-id="752c1-112">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="752c1-112">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c1-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="752c1-113">-Location</span></span>
<span data-ttu-id="752c1-114">Kaynağın konum olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="752c1-114">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c1-115">-OfferId</span><span class="sxs-lookup"><span data-stu-id="752c1-115">-OfferId</span></span>
<span data-ttu-id="752c1-116">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="752c1-116">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c1-117">Durumlu</span><span class="sxs-lookup"><span data-stu-id="752c1-117">-State</span></span>
<span data-ttu-id="752c1-118">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="752c1-118">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c1-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="752c1-119">-SubscriptionId</span></span>
<span data-ttu-id="752c1-120">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="752c1-120">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c1-121">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="752c1-121">-TenantId</span></span>
<span data-ttu-id="752c1-122">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="752c1-122">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="752c1-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="752c1-123">-Confirm</span></span>
<span data-ttu-id="752c1-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="752c1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="752c1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="752c1-125">-WhatIf</span></span>
<span data-ttu-id="752c1-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="752c1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="752c1-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="752c1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="752c1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752c1-128">CommonParameters</span></span>
<span data-ttu-id="752c1-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="752c1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752c1-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="752c1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752c1-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="752c1-131">INPUTS</span></span>

## <span data-ttu-id="752c1-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="752c1-132">OUTPUTS</span></span>

### <span data-ttu-id="752c1-133">Microsoft. AzureStack. Management. Subscription. modeller. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="752c1-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="752c1-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="752c1-134">NOTES</span></span>

## <span data-ttu-id="752c1-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="752c1-135">RELATED LINKS</span></span>
