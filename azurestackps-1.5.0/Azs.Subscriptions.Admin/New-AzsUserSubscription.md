---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 33544da0c95e6b53da2a0dc189ca0dfe538da270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571934"
---
# <span data-ttu-id="3b3ea-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="3b3ea-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="3b3ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3ea-103">Yeni bir abonelik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-103">Create a new subscription.</span></span>

## <span data-ttu-id="3b3ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b3ea-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3b3ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3ea-106">Yeni bir abonelik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-106">Create a new subscription.</span></span>

## <span data-ttu-id="3b3ea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b3ea-107">EXAMPLES</span></span>

### <span data-ttu-id="3b3ea-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3b3ea-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="3b3ea-109">Yeni bir kullanıcı aboneliği oluşturur</span><span class="sxs-lookup"><span data-stu-id="3b3ea-109">Creates a new user subscription</span></span>

## <span data-ttu-id="3b3ea-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b3ea-110">PARAMETERS</span></span>

### <span data-ttu-id="3b3ea-111">-Delegatevseçprovidersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="3b3ea-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="3b3ea-112">Üst temsilci abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="3b3ea-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3b3ea-113">-DisplayName</span></span>
<span data-ttu-id="3b3ea-114">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-114">Subscription name.</span></span>

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

### <span data-ttu-id="3b3ea-115">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="3b3ea-115">-ExternalReferenceId</span></span>
<span data-ttu-id="3b3ea-116">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-116">External reference identifier.</span></span>

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

### <span data-ttu-id="3b3ea-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="3b3ea-117">-OfferId</span></span>
<span data-ttu-id="3b3ea-118">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="3b3ea-119">-Sahip</span><span class="sxs-lookup"><span data-stu-id="3b3ea-119">-Owner</span></span>
<span data-ttu-id="3b3ea-120">Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-120">Subscription owner.</span></span>

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

### <span data-ttu-id="3b3ea-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="3b3ea-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="3b3ea-122">Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-122">Routing resource manager type.</span></span>

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

### <span data-ttu-id="3b3ea-123">Durumlu</span><span class="sxs-lookup"><span data-stu-id="3b3ea-123">-State</span></span>
<span data-ttu-id="3b3ea-124">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-124">Subscription state.</span></span>

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

### <span data-ttu-id="3b3ea-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3b3ea-125">-SubscriptionId</span></span>
<span data-ttu-id="3b3ea-126">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-126">Subscription identifier.</span></span>

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

### <span data-ttu-id="3b3ea-127">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="3b3ea-127">-TenantId</span></span>
<span data-ttu-id="3b3ea-128">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="3b3ea-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b3ea-129">-Confirm</span></span>
<span data-ttu-id="3b3ea-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b3ea-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3ea-131">-WhatIf</span></span>
<span data-ttu-id="3b3ea-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b3ea-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b3ea-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3ea-134">CommonParameters</span></span>
<span data-ttu-id="3b3ea-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b3ea-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3ea-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3ea-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3ea-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b3ea-137">INPUTS</span></span>

## <span data-ttu-id="3b3ea-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b3ea-138">OUTPUTS</span></span>

### <span data-ttu-id="3b3ea-139">Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik</span><span class="sxs-lookup"><span data-stu-id="3b3ea-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="3b3ea-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b3ea-140">NOTES</span></span>

## <span data-ttu-id="3b3ea-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b3ea-141">RELATED LINKS</span></span>

