---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e0c752c3ffd266a3615fdd5a1f5193e0202b29a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934328"
---
# <span data-ttu-id="26742-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="26742-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="26742-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26742-102">SYNOPSIS</span></span>
<span data-ttu-id="26742-103">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="26742-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="26742-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26742-104">SYNTAX</span></span>

### <span data-ttu-id="26742-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26742-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26742-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="26742-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26742-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="26742-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26742-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="26742-108">DESCRIPTION</span></span>
<span data-ttu-id="26742-109">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="26742-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="26742-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26742-110">EXAMPLES</span></span>

### <span data-ttu-id="26742-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="26742-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="26742-112">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="26742-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="26742-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26742-113">PARAMETERS</span></span>

### <span data-ttu-id="26742-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26742-114">-InputObject</span></span>
<span data-ttu-id="26742-115">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci türünde giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="26742-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26742-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="26742-116">-Location</span></span>
<span data-ttu-id="26742-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="26742-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26742-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="26742-118">-Name</span></span>
<span data-ttu-id="26742-119">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="26742-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="26742-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="26742-120">-OfferName</span></span>
<span data-ttu-id="26742-121">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="26742-121">Name of an offer.</span></span>

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

### <span data-ttu-id="26742-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26742-122">-ResourceGroupName</span></span>
<span data-ttu-id="26742-123">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="26742-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="26742-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="26742-124">-ResourceId</span></span>
<span data-ttu-id="26742-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="26742-125">The resource id.</span></span>

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

### <span data-ttu-id="26742-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="26742-126">-SubscriptionId</span></span>
<span data-ttu-id="26742-127">Temsilci teklif alma aboneliğinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="26742-127">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26742-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="26742-128">-Confirm</span></span>
<span data-ttu-id="26742-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26742-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26742-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26742-130">-WhatIf</span></span>
<span data-ttu-id="26742-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26742-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26742-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26742-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26742-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26742-133">CommonParameters</span></span>
<span data-ttu-id="26742-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26742-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26742-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26742-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26742-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26742-136">INPUTS</span></span>

## <span data-ttu-id="26742-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26742-137">OUTPUTS</span></span>

### <span data-ttu-id="26742-138">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci</span><span class="sxs-lookup"><span data-stu-id="26742-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="26742-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26742-139">NOTES</span></span>

## <span data-ttu-id="26742-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26742-140">RELATED LINKS</span></span>
