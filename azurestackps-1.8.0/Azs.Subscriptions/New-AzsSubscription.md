---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934564"
---
# <span data-ttu-id="9564c-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="9564c-101">New-AzsSubscription</span></span>

## <span data-ttu-id="9564c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9564c-102">SYNOPSIS</span></span>
<span data-ttu-id="9564c-103">Abonelik oluşturma.</span><span class="sxs-lookup"><span data-stu-id="9564c-103">Create a subscription.</span></span>

## <span data-ttu-id="9564c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9564c-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9564c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9564c-105">DESCRIPTION</span></span>
<span data-ttu-id="9564c-106">Abonelik oluşturma.</span><span class="sxs-lookup"><span data-stu-id="9564c-106">Create a subscription.</span></span>

## <span data-ttu-id="9564c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9564c-107">EXAMPLES</span></span>

### <span data-ttu-id="9564c-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="9564c-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="9564c-109">Abonelik oluşturma.</span><span class="sxs-lookup"><span data-stu-id="9564c-109">Create a subscription.</span></span>

## <span data-ttu-id="9564c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9564c-110">PARAMETERS</span></span>

### <span data-ttu-id="9564c-111">-OfferId</span><span class="sxs-lookup"><span data-stu-id="9564c-111">-OfferId</span></span>
<span data-ttu-id="9564c-112">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="9564c-112">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="9564c-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9564c-113">-DisplayName</span></span>
<span data-ttu-id="9564c-114">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="9564c-114">Subscription name.</span></span>

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

### <span data-ttu-id="9564c-115">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="9564c-115">-TenantId</span></span>
<span data-ttu-id="9564c-116">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="9564c-116">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="9564c-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="9564c-117">-SubscriptionId</span></span>
<span data-ttu-id="9564c-118">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="9564c-118">Subscription identifier.</span></span>

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

### <span data-ttu-id="9564c-119">Durumlu</span><span class="sxs-lookup"><span data-stu-id="9564c-119">-State</span></span>
<span data-ttu-id="9564c-120">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="9564c-120">Subscription state.</span></span>

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

### <span data-ttu-id="9564c-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="9564c-121">-Location</span></span>
<span data-ttu-id="9564c-122">Kaynağın konum olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="9564c-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="9564c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9564c-123">-WhatIf</span></span>
<span data-ttu-id="9564c-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9564c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9564c-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9564c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9564c-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="9564c-126">-Confirm</span></span>
<span data-ttu-id="9564c-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9564c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9564c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9564c-128">CommonParameters</span></span>
<span data-ttu-id="9564c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9564c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9564c-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9564c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9564c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9564c-131">INPUTS</span></span>

## <span data-ttu-id="9564c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9564c-132">OUTPUTS</span></span>

### <span data-ttu-id="9564c-133">Microsoft. AzureStack. Management. Subscription. modeller. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="9564c-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="9564c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9564c-134">NOTES</span></span>

## <span data-ttu-id="9564c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9564c-135">RELATED LINKS</span></span>
