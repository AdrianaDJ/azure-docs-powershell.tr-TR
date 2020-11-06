---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 106293e9d959aefe25ae3e4b27519639a39193d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571789"
---
# <span data-ttu-id="52503-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="52503-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="52503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52503-102">SYNOPSIS</span></span>
<span data-ttu-id="52503-103">Belirtilen kullanıcı aboneliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="52503-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="52503-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52503-104">SYNTAX</span></span>

### <span data-ttu-id="52503-105">Ayarla (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52503-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52503-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="52503-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52503-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="52503-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52503-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="52503-108">DESCRIPTION</span></span>
<span data-ttu-id="52503-109">Belirtilen kullanıcı aboneliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="52503-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="52503-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52503-110">EXAMPLES</span></span>

### <span data-ttu-id="52503-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="52503-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="52503-112">Aboneliği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="52503-112">Updates a subscription</span></span>

## <span data-ttu-id="52503-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52503-113">PARAMETERS</span></span>

### <span data-ttu-id="52503-114">-Delegatevseçprovidersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="52503-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="52503-115">Üst temsilci abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="52503-115">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="52503-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="52503-116">-DisplayName</span></span>
<span data-ttu-id="52503-117">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="52503-117">Subscription name.</span></span>

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

### <span data-ttu-id="52503-118">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="52503-118">-ExternalReferenceId</span></span>
<span data-ttu-id="52503-119">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="52503-119">External reference identifier.</span></span>

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

### <span data-ttu-id="52503-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52503-120">-InputObject</span></span>
<span data-ttu-id="52503-121">Microsoft. AzureStack. Management. Network. admin. model. Quota türünde giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="52503-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52503-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="52503-122">-Location</span></span>
<span data-ttu-id="52503-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="52503-123">Location of the resource.</span></span>

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

### <span data-ttu-id="52503-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="52503-124">-OfferId</span></span>
<span data-ttu-id="52503-125">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="52503-125">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="52503-126">-Sahip</span><span class="sxs-lookup"><span data-stu-id="52503-126">-Owner</span></span>
<span data-ttu-id="52503-127">Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="52503-127">Subscription owner.</span></span>

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

### <span data-ttu-id="52503-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="52503-128">-ResourceId</span></span>
<span data-ttu-id="52503-129">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="52503-129">The resource ID.</span></span>

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

### <span data-ttu-id="52503-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="52503-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="52503-131">Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="52503-131">Routing resource manager type.</span></span>

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

### <span data-ttu-id="52503-132">Durumlu</span><span class="sxs-lookup"><span data-stu-id="52503-132">-State</span></span>
<span data-ttu-id="52503-133">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="52503-133">Subscription state.</span></span>

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

### <span data-ttu-id="52503-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="52503-134">-SubscriptionId</span></span>
<span data-ttu-id="52503-135">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="52503-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52503-136">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="52503-136">-TenantId</span></span>
<span data-ttu-id="52503-137">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="52503-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="52503-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="52503-138">-Confirm</span></span>
<span data-ttu-id="52503-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="52503-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52503-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52503-140">-WhatIf</span></span>
<span data-ttu-id="52503-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="52503-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52503-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="52503-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52503-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52503-143">CommonParameters</span></span>
<span data-ttu-id="52503-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52503-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52503-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52503-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52503-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52503-146">INPUTS</span></span>

## <span data-ttu-id="52503-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52503-147">OUTPUTS</span></span>

### <span data-ttu-id="52503-148">Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik</span><span class="sxs-lookup"><span data-stu-id="52503-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="52503-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52503-149">NOTES</span></span>

## <span data-ttu-id="52503-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52503-150">RELATED LINKS</span></span>

