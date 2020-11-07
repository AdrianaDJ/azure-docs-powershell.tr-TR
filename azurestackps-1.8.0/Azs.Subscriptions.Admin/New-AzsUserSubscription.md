---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d4b7abdeb085c7cfee6444c4afeeb6a3e79d99e9
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934591"
---
# <span data-ttu-id="b4694-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="b4694-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="b4694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4694-102">SYNOPSIS</span></span>
<span data-ttu-id="b4694-103">Yeni bir abonelik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b4694-103">Create a new subscription.</span></span>

## <span data-ttu-id="b4694-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4694-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4694-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4694-105">DESCRIPTION</span></span>
<span data-ttu-id="b4694-106">Yeni bir abonelik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b4694-106">Create a new subscription.</span></span>

## <span data-ttu-id="b4694-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4694-107">EXAMPLES</span></span>

### <span data-ttu-id="b4694-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b4694-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="b4694-109">Yeni bir kullanıcı aboneliği oluşturur</span><span class="sxs-lookup"><span data-stu-id="b4694-109">Creates a new user subscription</span></span>

## <span data-ttu-id="b4694-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4694-110">PARAMETERS</span></span>

### <span data-ttu-id="b4694-111">-Delegatevseçprovidersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="b4694-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="b4694-112">Üst temsilci abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="b4694-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4694-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b4694-113">-DisplayName</span></span>
<span data-ttu-id="b4694-114">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="b4694-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4694-115">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="b4694-115">-ExternalReferenceId</span></span>
<span data-ttu-id="b4694-116">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b4694-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4694-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="b4694-117">-OfferId</span></span>
<span data-ttu-id="b4694-118">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="b4694-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4694-119">-Sahip</span><span class="sxs-lookup"><span data-stu-id="b4694-119">-Owner</span></span>
<span data-ttu-id="b4694-120">Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="b4694-120">Subscription owner.</span></span>

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

### <span data-ttu-id="b4694-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="b4694-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="b4694-122">Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="b4694-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4694-123">Durumlu</span><span class="sxs-lookup"><span data-stu-id="b4694-123">-State</span></span>
<span data-ttu-id="b4694-124">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="b4694-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4694-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b4694-125">-SubscriptionId</span></span>
<span data-ttu-id="b4694-126">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b4694-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4694-127">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="b4694-127">-TenantId</span></span>
<span data-ttu-id="b4694-128">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b4694-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="b4694-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4694-129">-Confirm</span></span>
<span data-ttu-id="b4694-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4694-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4694-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4694-131">-WhatIf</span></span>
<span data-ttu-id="b4694-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4694-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4694-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4694-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4694-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4694-134">CommonParameters</span></span>
<span data-ttu-id="b4694-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4694-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4694-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4694-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4694-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4694-137">INPUTS</span></span>

## <span data-ttu-id="b4694-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4694-138">OUTPUTS</span></span>

### <span data-ttu-id="b4694-139">Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik</span><span class="sxs-lookup"><span data-stu-id="b4694-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="b4694-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4694-140">NOTES</span></span>

## <span data-ttu-id="b4694-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4694-141">RELATED LINKS</span></span>

