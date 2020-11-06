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
ms.locfileid: "93571446"
---
# <span data-ttu-id="6b12e-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="6b12e-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="6b12e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b12e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b12e-103">Yeni bir abonelik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b12e-103">Create a new subscription.</span></span>

## <span data-ttu-id="6b12e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b12e-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b12e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b12e-105">DESCRIPTION</span></span>
<span data-ttu-id="6b12e-106">Yeni bir abonelik oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6b12e-106">Create a new subscription.</span></span>

## <span data-ttu-id="6b12e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b12e-107">EXAMPLES</span></span>

### <span data-ttu-id="6b12e-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6b12e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="6b12e-109">Yeni bir kullanıcı aboneliği oluşturur</span><span class="sxs-lookup"><span data-stu-id="6b12e-109">Creates a new user subscription</span></span>

## <span data-ttu-id="6b12e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b12e-110">PARAMETERS</span></span>

### <span data-ttu-id="6b12e-111">-Delegatevseçprovidersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="6b12e-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="6b12e-112">Üst temsilci abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6b12e-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="6b12e-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6b12e-113">-DisplayName</span></span>
<span data-ttu-id="6b12e-114">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="6b12e-114">Subscription name.</span></span>

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

### <span data-ttu-id="6b12e-115">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="6b12e-115">-ExternalReferenceId</span></span>
<span data-ttu-id="6b12e-116">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6b12e-116">External reference identifier.</span></span>

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

### <span data-ttu-id="6b12e-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="6b12e-117">-OfferId</span></span>
<span data-ttu-id="6b12e-118">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="6b12e-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="6b12e-119">-Sahip</span><span class="sxs-lookup"><span data-stu-id="6b12e-119">-Owner</span></span>
<span data-ttu-id="6b12e-120">Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="6b12e-120">Subscription owner.</span></span>

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

### <span data-ttu-id="6b12e-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="6b12e-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="6b12e-122">Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="6b12e-122">Routing resource manager type.</span></span>

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

### <span data-ttu-id="6b12e-123">Durumlu</span><span class="sxs-lookup"><span data-stu-id="6b12e-123">-State</span></span>
<span data-ttu-id="6b12e-124">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="6b12e-124">Subscription state.</span></span>

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

### <span data-ttu-id="6b12e-125">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6b12e-125">-SubscriptionId</span></span>
<span data-ttu-id="6b12e-126">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6b12e-126">Subscription identifier.</span></span>

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

### <span data-ttu-id="6b12e-127">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="6b12e-127">-TenantId</span></span>
<span data-ttu-id="6b12e-128">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6b12e-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="6b12e-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b12e-129">-Confirm</span></span>
<span data-ttu-id="6b12e-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b12e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b12e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b12e-131">-WhatIf</span></span>
<span data-ttu-id="6b12e-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b12e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b12e-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b12e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b12e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b12e-134">CommonParameters</span></span>
<span data-ttu-id="6b12e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b12e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b12e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b12e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b12e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b12e-137">INPUTS</span></span>

## <span data-ttu-id="6b12e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b12e-138">OUTPUTS</span></span>

### <span data-ttu-id="6b12e-139">Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik</span><span class="sxs-lookup"><span data-stu-id="6b12e-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="6b12e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b12e-140">NOTES</span></span>

## <span data-ttu-id="6b12e-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b12e-141">RELATED LINKS</span></span>

