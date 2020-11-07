---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ef53ac2d32d71a68b7fe342f5d2d0cafc2a193f8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934567"
---
# <span data-ttu-id="a6037-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="a6037-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="a6037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6037-102">SYNOPSIS</span></span>
<span data-ttu-id="a6037-103">Belirtilen kullanıcı aboneliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a6037-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="a6037-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6037-104">SYNTAX</span></span>

### <span data-ttu-id="a6037-105">Ayarla (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6037-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6037-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a6037-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6037-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a6037-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6037-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6037-108">DESCRIPTION</span></span>
<span data-ttu-id="a6037-109">Belirtilen kullanıcı aboneliğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a6037-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="a6037-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6037-110">EXAMPLES</span></span>

### <span data-ttu-id="a6037-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6037-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="a6037-112">Aboneliği güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="a6037-112">Updates a subscription</span></span>

## <span data-ttu-id="a6037-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6037-113">PARAMETERS</span></span>

### <span data-ttu-id="a6037-114">-Delegatevseçprovidersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="a6037-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="a6037-115">Üst temsilci abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a6037-115">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="a6037-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a6037-116">-DisplayName</span></span>
<span data-ttu-id="a6037-117">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="a6037-117">Subscription name.</span></span>

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

### <span data-ttu-id="a6037-118">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="a6037-118">-ExternalReferenceId</span></span>
<span data-ttu-id="a6037-119">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a6037-119">External reference identifier.</span></span>

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

### <span data-ttu-id="a6037-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6037-120">-InputObject</span></span>
<span data-ttu-id="a6037-121">Microsoft. AzureStack. Management. Network. admin. model. Quota türünde giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a6037-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

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

### <span data-ttu-id="a6037-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="a6037-122">-Location</span></span>
<span data-ttu-id="a6037-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="a6037-123">Location of the resource.</span></span>

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

### <span data-ttu-id="a6037-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="a6037-124">-OfferId</span></span>
<span data-ttu-id="a6037-125">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="a6037-125">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="a6037-126">-Sahip</span><span class="sxs-lookup"><span data-stu-id="a6037-126">-Owner</span></span>
<span data-ttu-id="a6037-127">Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="a6037-127">Subscription owner.</span></span>

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

### <span data-ttu-id="a6037-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a6037-128">-ResourceId</span></span>
<span data-ttu-id="a6037-129">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a6037-129">The resource ID.</span></span>

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

### <span data-ttu-id="a6037-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="a6037-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="a6037-131">Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="a6037-131">Routing resource manager type.</span></span>

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

### <span data-ttu-id="a6037-132">Durumlu</span><span class="sxs-lookup"><span data-stu-id="a6037-132">-State</span></span>
<span data-ttu-id="a6037-133">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="a6037-133">Subscription state.</span></span>

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

### <span data-ttu-id="a6037-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a6037-134">-SubscriptionId</span></span>
<span data-ttu-id="a6037-135">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a6037-135">Subscription identifier.</span></span>

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

### <span data-ttu-id="a6037-136">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="a6037-136">-TenantId</span></span>
<span data-ttu-id="a6037-137">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="a6037-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="a6037-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6037-138">-Confirm</span></span>
<span data-ttu-id="a6037-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6037-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6037-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6037-140">-WhatIf</span></span>
<span data-ttu-id="a6037-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6037-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6037-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6037-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6037-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6037-143">CommonParameters</span></span>
<span data-ttu-id="a6037-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6037-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6037-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6037-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6037-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6037-146">INPUTS</span></span>

## <span data-ttu-id="a6037-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6037-147">OUTPUTS</span></span>

### <span data-ttu-id="a6037-148">Microsoft. AzureStack. Management. abonelikler. admin. modeller. abonelik</span><span class="sxs-lookup"><span data-stu-id="a6037-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="a6037-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6037-149">NOTES</span></span>

## <span data-ttu-id="a6037-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6037-150">RELATED LINKS</span></span>

