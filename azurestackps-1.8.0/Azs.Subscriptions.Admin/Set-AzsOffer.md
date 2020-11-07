---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b08aed00a4c16bd2031608ff795a4dde8491859
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934748"
---
# <span data-ttu-id="369d1-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="369d1-101">Set-AzsOffer</span></span>

## <span data-ttu-id="369d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="369d1-102">SYNOPSIS</span></span>
<span data-ttu-id="369d1-103">Teklifi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="369d1-103">Update the offer.</span></span>

## <span data-ttu-id="369d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="369d1-104">SYNTAX</span></span>

### <span data-ttu-id="369d1-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="369d1-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="369d1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="369d1-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="369d1-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="369d1-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="369d1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="369d1-108">DESCRIPTION</span></span>
<span data-ttu-id="369d1-109">Teklifi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="369d1-109">Update the offer.</span></span>

## <span data-ttu-id="369d1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="369d1-110">EXAMPLES</span></span>

### <span data-ttu-id="369d1-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="369d1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="369d1-112">Teklifi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="369d1-112">Update the offer.</span></span>

## <span data-ttu-id="369d1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="369d1-113">PARAMETERS</span></span>

### <span data-ttu-id="369d1-114">-Add</span><span class="sxs-lookup"><span data-stu-id="369d1-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="369d1-115">Bir kiracının isteğe bağlı olarak teklifin bir parçası olarak edinebileceğiniz eklenti planlarına yönelik başvurular.</span><span class="sxs-lookup"><span data-stu-id="369d1-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-116">-Temelplankimlikleri</span><span class="sxs-lookup"><span data-stu-id="369d1-116">-BasePlanIds</span></span>
<span data-ttu-id="369d1-117">Kiracı teklife abone olduğunda kiracıya hemen sağlanan temel planların tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="369d1-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="369d1-118">-Description</span></span>
<span data-ttu-id="369d1-119">Teklifin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="369d1-119">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="369d1-120">-DisplayName</span></span>
<span data-ttu-id="369d1-121">Teklifin adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="369d1-121">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-122">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="369d1-122">-ExternalReferenceId</span></span>
<span data-ttu-id="369d1-123">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="369d1-123">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="369d1-124">-InputObject</span></span>
<span data-ttu-id="369d1-125">Microsoft. AzureStack. Management. abonelikler. admin. modeller. teklifini yazın.</span><span class="sxs-lookup"><span data-stu-id="369d1-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="369d1-126">-Location</span></span>
<span data-ttu-id="369d1-127">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="369d1-127">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="369d1-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="369d1-129">Hesap başına maksimum abonelik.</span><span class="sxs-lookup"><span data-stu-id="369d1-129">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="369d1-130">-Name</span></span>
<span data-ttu-id="369d1-131">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="369d1-131">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="369d1-132">-ResourceGroupName</span></span>
<span data-ttu-id="369d1-133">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="369d1-133">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="369d1-134">-ResourceId</span></span>
<span data-ttu-id="369d1-135">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="369d1-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-136">Durumlu</span><span class="sxs-lookup"><span data-stu-id="369d1-136">-State</span></span>
<span data-ttu-id="369d1-137">Erişilebilirlik durumunu sunma.</span><span class="sxs-lookup"><span data-stu-id="369d1-137">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="369d1-138">-SubscriptionCount</span></span>
<span data-ttu-id="369d1-139">Geçerli abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="369d1-139">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="369d1-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="369d1-140">-Confirm</span></span>
<span data-ttu-id="369d1-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="369d1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="369d1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="369d1-142">-WhatIf</span></span>
<span data-ttu-id="369d1-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="369d1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="369d1-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="369d1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="369d1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="369d1-145">CommonParameters</span></span>
<span data-ttu-id="369d1-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="369d1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="369d1-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="369d1-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="369d1-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="369d1-148">INPUTS</span></span>

## <span data-ttu-id="369d1-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="369d1-149">OUTPUTS</span></span>

### <span data-ttu-id="369d1-150">Microsoft. AzureStack. Management. abonelikler. admin. modeller. teklifini</span><span class="sxs-lookup"><span data-stu-id="369d1-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="369d1-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="369d1-151">NOTES</span></span>

## <span data-ttu-id="369d1-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="369d1-152">RELATED LINKS</span></span>

