---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 285b9509241e9035c007f871ac6395008a1f9cde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934329"
---
# <span data-ttu-id="65642-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="65642-101">Set-AzsOffer</span></span>

## <span data-ttu-id="65642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65642-102">SYNOPSIS</span></span>
<span data-ttu-id="65642-103">Teklifi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="65642-103">Update the offer.</span></span>

## <span data-ttu-id="65642-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65642-104">SYNTAX</span></span>

### <span data-ttu-id="65642-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65642-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65642-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="65642-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65642-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="65642-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65642-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="65642-108">DESCRIPTION</span></span>
<span data-ttu-id="65642-109">Teklifi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="65642-109">Update the offer.</span></span>

## <span data-ttu-id="65642-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65642-110">EXAMPLES</span></span>

### <span data-ttu-id="65642-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="65642-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="65642-112">Teklifi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="65642-112">Update the offer.</span></span>

## <span data-ttu-id="65642-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65642-113">PARAMETERS</span></span>

### <span data-ttu-id="65642-114">-Add</span><span class="sxs-lookup"><span data-stu-id="65642-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="65642-115">Bir kiracının isteğe bağlı olarak teklifin bir parçası olarak edinebileceğiniz eklenti planlarına yönelik başvurular.</span><span class="sxs-lookup"><span data-stu-id="65642-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

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

### <span data-ttu-id="65642-116">-Temelplankimlikleri</span><span class="sxs-lookup"><span data-stu-id="65642-116">-BasePlanIds</span></span>
<span data-ttu-id="65642-117">Kiracı teklife abone olduğunda kiracıya hemen sağlanan temel planların tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="65642-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

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

### <span data-ttu-id="65642-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="65642-118">-Description</span></span>
<span data-ttu-id="65642-119">Teklifin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="65642-119">Description of offer.</span></span>

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

### <span data-ttu-id="65642-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="65642-120">-DisplayName</span></span>
<span data-ttu-id="65642-121">Teklifin adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="65642-121">Display name of offer.</span></span>

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

### <span data-ttu-id="65642-122">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="65642-122">-ExternalReferenceId</span></span>
<span data-ttu-id="65642-123">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="65642-123">External reference identifier.</span></span>

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

### <span data-ttu-id="65642-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65642-124">-InputObject</span></span>
<span data-ttu-id="65642-125">Microsoft. AzureStack. Management. abonelikler. admin. modeller. teklifini yazın.</span><span class="sxs-lookup"><span data-stu-id="65642-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

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

### <span data-ttu-id="65642-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="65642-126">-Location</span></span>
<span data-ttu-id="65642-127">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="65642-127">Location of the resource.</span></span>

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

### <span data-ttu-id="65642-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="65642-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="65642-129">Hesap başına maksimum abonelik.</span><span class="sxs-lookup"><span data-stu-id="65642-129">Maximum subscriptions per account.</span></span>

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

### <span data-ttu-id="65642-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="65642-130">-Name</span></span>
<span data-ttu-id="65642-131">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="65642-131">Name of an offer.</span></span>

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

### <span data-ttu-id="65642-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65642-132">-ResourceGroupName</span></span>
<span data-ttu-id="65642-133">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="65642-133">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="65642-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="65642-134">-ResourceId</span></span>
<span data-ttu-id="65642-135">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="65642-135">The resource id.</span></span>

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

### <span data-ttu-id="65642-136">Durumlu</span><span class="sxs-lookup"><span data-stu-id="65642-136">-State</span></span>
<span data-ttu-id="65642-137">Erişilebilirlik durumunu sunma.</span><span class="sxs-lookup"><span data-stu-id="65642-137">Offer accessibility state.</span></span>

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

### <span data-ttu-id="65642-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="65642-138">-SubscriptionCount</span></span>
<span data-ttu-id="65642-139">Geçerli abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="65642-139">Current subscription count.</span></span>

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

### <span data-ttu-id="65642-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="65642-140">-Confirm</span></span>
<span data-ttu-id="65642-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65642-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65642-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65642-142">-WhatIf</span></span>
<span data-ttu-id="65642-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65642-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65642-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65642-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65642-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65642-145">CommonParameters</span></span>
<span data-ttu-id="65642-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65642-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65642-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65642-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65642-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65642-148">INPUTS</span></span>

## <span data-ttu-id="65642-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65642-149">OUTPUTS</span></span>

### <span data-ttu-id="65642-150">Microsoft. AzureStack. Management. abonelikler. admin. modeller. teklifini</span><span class="sxs-lookup"><span data-stu-id="65642-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="65642-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65642-151">NOTES</span></span>

## <span data-ttu-id="65642-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65642-152">RELATED LINKS</span></span>

