---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87ad48de1fa4ae05f90f067e8a0a2eac2c4fdd0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934523"
---
# <span data-ttu-id="69240-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="69240-101">New-AzsOffer</span></span>

## <span data-ttu-id="69240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69240-102">SYNOPSIS</span></span>
<span data-ttu-id="69240-103">Yeni bir teklif oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69240-103">Creates a new offer.</span></span>

## <span data-ttu-id="69240-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69240-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69240-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69240-105">DESCRIPTION</span></span>
<span data-ttu-id="69240-106">Teklifi oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="69240-106">Create or update the offer.</span></span>

## <span data-ttu-id="69240-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69240-107">EXAMPLES</span></span>

### <span data-ttu-id="69240-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="69240-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="69240-109">Yeni bir teklif oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69240-109">Creates a new offer.</span></span>

## <span data-ttu-id="69240-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69240-110">PARAMETERS</span></span>

### <span data-ttu-id="69240-111">-Add</span><span class="sxs-lookup"><span data-stu-id="69240-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="69240-112">Bir kiracının isteğe bağlı olarak teklifin bir parçası olarak edinebileceğiniz eklenti planlarına yönelik başvurular.</span><span class="sxs-lookup"><span data-stu-id="69240-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69240-113">-Temelplankimlikleri</span><span class="sxs-lookup"><span data-stu-id="69240-113">-BasePlanIds</span></span>
<span data-ttu-id="69240-114">Kiracı teklife abone olduğunda kiracıya hemen sağlanan temel planların tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="69240-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69240-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="69240-115">-Description</span></span>
<span data-ttu-id="69240-116">Teklifin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="69240-116">Description of offer.</span></span>

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

### <span data-ttu-id="69240-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="69240-117">-DisplayName</span></span>
<span data-ttu-id="69240-118">Teklifin adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="69240-118">Display name of offer.</span></span>

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

### <span data-ttu-id="69240-119">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="69240-119">-ExternalReferenceId</span></span>
<span data-ttu-id="69240-120">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="69240-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69240-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="69240-121">-Location</span></span>
<span data-ttu-id="69240-122">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="69240-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69240-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="69240-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="69240-124">Hesap başına maksimum abonelik.</span><span class="sxs-lookup"><span data-stu-id="69240-124">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69240-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="69240-125">-Name</span></span>
<span data-ttu-id="69240-126">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="69240-126">Name of an offer.</span></span>

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

### <span data-ttu-id="69240-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69240-127">-ResourceGroupName</span></span>
<span data-ttu-id="69240-128">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="69240-128">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69240-129">Durumlu</span><span class="sxs-lookup"><span data-stu-id="69240-129">-State</span></span>
<span data-ttu-id="69240-130">Erişilebilirlik durumunu sunma.</span><span class="sxs-lookup"><span data-stu-id="69240-130">Offer accessibility state.</span></span>
<span data-ttu-id="69240-131">Varsayılan değer özeldir.</span><span class="sxs-lookup"><span data-stu-id="69240-131">Default value is Private.</span></span>
<span data-ttu-id="69240-132">Bu parametre gelecekteki bir sürümde kullanımdan kalkacaktır</span><span class="sxs-lookup"><span data-stu-id="69240-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69240-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="69240-133">-SubscriptionCount</span></span>
<span data-ttu-id="69240-134">Geçerli abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="69240-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69240-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="69240-135">-Confirm</span></span>
<span data-ttu-id="69240-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69240-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69240-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69240-137">-WhatIf</span></span>
<span data-ttu-id="69240-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69240-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69240-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69240-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69240-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69240-140">CommonParameters</span></span>
<span data-ttu-id="69240-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69240-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69240-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69240-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69240-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69240-143">INPUTS</span></span>

## <span data-ttu-id="69240-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69240-144">OUTPUTS</span></span>

### <span data-ttu-id="69240-145">Microsoft. AzureStack. Management. abonelikler. admin. modeller. teklifini</span><span class="sxs-lookup"><span data-stu-id="69240-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="69240-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69240-146">NOTES</span></span>

## <span data-ttu-id="69240-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69240-147">RELATED LINKS</span></span>

