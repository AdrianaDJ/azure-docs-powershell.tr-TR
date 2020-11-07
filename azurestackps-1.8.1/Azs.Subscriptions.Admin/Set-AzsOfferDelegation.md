---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1256fa41d7accc175e79bb531c62f76ace6482d8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934868"
---
# <span data-ttu-id="58ff6-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="58ff6-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="58ff6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="58ff6-103">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="58ff6-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="58ff6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58ff6-104">SYNTAX</span></span>

### <span data-ttu-id="58ff6-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58ff6-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ff6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="58ff6-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ff6-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="58ff6-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ff6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="58ff6-108">DESCRIPTION</span></span>
<span data-ttu-id="58ff6-109">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="58ff6-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="58ff6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58ff6-110">EXAMPLES</span></span>

### <span data-ttu-id="58ff6-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="58ff6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="58ff6-112">Temsilci teklifini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="58ff6-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="58ff6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58ff6-113">PARAMETERS</span></span>

### <span data-ttu-id="58ff6-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58ff6-114">-InputObject</span></span>
<span data-ttu-id="58ff6-115">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci türünde giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="58ff6-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

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

### <span data-ttu-id="58ff6-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="58ff6-116">-Location</span></span>
<span data-ttu-id="58ff6-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="58ff6-117">Location of the resource.</span></span>

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

### <span data-ttu-id="58ff6-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="58ff6-118">-Name</span></span>
<span data-ttu-id="58ff6-119">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="58ff6-119">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="58ff6-120">-OfferName</span><span class="sxs-lookup"><span data-stu-id="58ff6-120">-OfferName</span></span>
<span data-ttu-id="58ff6-121">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="58ff6-121">Name of an offer.</span></span>

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

### <span data-ttu-id="58ff6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ff6-122">-ResourceGroupName</span></span>
<span data-ttu-id="58ff6-123">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="58ff6-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="58ff6-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="58ff6-124">-ResourceId</span></span>
<span data-ttu-id="58ff6-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="58ff6-125">The resource id.</span></span>

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

### <span data-ttu-id="58ff6-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="58ff6-126">-SubscriptionId</span></span>
<span data-ttu-id="58ff6-127">Temsilci teklif alma aboneliğinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="58ff6-127">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="58ff6-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="58ff6-128">-Confirm</span></span>
<span data-ttu-id="58ff6-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58ff6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ff6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ff6-130">-WhatIf</span></span>
<span data-ttu-id="58ff6-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58ff6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58ff6-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="58ff6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ff6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ff6-133">CommonParameters</span></span>
<span data-ttu-id="58ff6-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58ff6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ff6-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ff6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ff6-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58ff6-136">INPUTS</span></span>

## <span data-ttu-id="58ff6-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58ff6-137">OUTPUTS</span></span>

### <span data-ttu-id="58ff6-138">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci</span><span class="sxs-lookup"><span data-stu-id="58ff6-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="58ff6-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58ff6-139">NOTES</span></span>

## <span data-ttu-id="58ff6-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58ff6-140">RELATED LINKS</span></span>

