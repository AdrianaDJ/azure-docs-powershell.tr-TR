---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1256fa41d7accc175e79bb531c62f76ace6482d8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107070"
---
# <span data-ttu-id="da498-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="da498-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="da498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da498-102">SYNOPSIS</span></span>
<span data-ttu-id="da498-103">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="da498-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="da498-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da498-104">SYNTAX</span></span>

### <span data-ttu-id="da498-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="da498-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da498-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="da498-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da498-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="da498-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da498-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="da498-108">DESCRIPTION</span></span>
<span data-ttu-id="da498-109">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="da498-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="da498-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da498-110">EXAMPLES</span></span>

### <span data-ttu-id="da498-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="da498-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="da498-112">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="da498-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="da498-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da498-113">PARAMETERS</span></span>

### <span data-ttu-id="da498-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da498-114">-InputObject</span></span>
<span data-ttu-id="da498-115">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci türünde giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="da498-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

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

### <span data-ttu-id="da498-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="da498-116">-Location</span></span>
<span data-ttu-id="da498-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="da498-117">Location of the resource.</span></span>

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

### <span data-ttu-id="da498-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="da498-118">-Name</span></span>
<span data-ttu-id="da498-119">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="da498-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="da498-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="da498-120">-OfferName</span></span>
<span data-ttu-id="da498-121">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="da498-121">Name of an offer.</span></span>

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

### <span data-ttu-id="da498-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da498-122">-ResourceGroupName</span></span>
<span data-ttu-id="da498-123">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="da498-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="da498-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="da498-124">-ResourceId</span></span>
<span data-ttu-id="da498-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="da498-125">The resource id.</span></span>

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

### <span data-ttu-id="da498-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="da498-126">-SubscriptionId</span></span>
<span data-ttu-id="da498-127">Temsilci teklif alma aboneliğinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="da498-127">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="da498-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="da498-128">-Confirm</span></span>
<span data-ttu-id="da498-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da498-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da498-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da498-130">-WhatIf</span></span>
<span data-ttu-id="da498-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da498-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da498-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da498-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da498-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da498-133">CommonParameters</span></span>
<span data-ttu-id="da498-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da498-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da498-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da498-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da498-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da498-136">INPUTS</span></span>

## <span data-ttu-id="da498-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da498-137">OUTPUTS</span></span>

### <span data-ttu-id="da498-138">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci</span><span class="sxs-lookup"><span data-stu-id="da498-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="da498-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da498-139">NOTES</span></span>

## <span data-ttu-id="da498-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da498-140">RELATED LINKS</span></span>

