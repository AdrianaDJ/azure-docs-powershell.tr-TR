---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934926"
---
# <span data-ttu-id="7aa2f-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="7aa2f-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="7aa2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aa2f-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa2f-103">Yeni bir teklif temsilcisi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="7aa2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7aa2f-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aa2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7aa2f-105">DESCRIPTION</span></span>
<span data-ttu-id="7aa2f-106">Yeni bir teklif temsilcisi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="7aa2f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7aa2f-107">EXAMPLES</span></span>

### <span data-ttu-id="7aa2f-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7aa2f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="7aa2f-109">Yeni bir teklif temsilcisi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="7aa2f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7aa2f-110">PARAMETERS</span></span>

### <span data-ttu-id="7aa2f-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="7aa2f-111">-Location</span></span>
<span data-ttu-id="7aa2f-112">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-112">Location of the resource.</span></span>

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

### <span data-ttu-id="7aa2f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7aa2f-113">-Name</span></span>
<span data-ttu-id="7aa2f-114">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="7aa2f-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="7aa2f-115">-OfferName</span></span>
<span data-ttu-id="7aa2f-116">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-116">Name of an offer.</span></span>

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

### <span data-ttu-id="7aa2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa2f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7aa2f-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa2f-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7aa2f-119">-SubscriptionId</span></span>
<span data-ttu-id="7aa2f-120">Temsilci teklif alma aboneliğinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="7aa2f-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="7aa2f-121">-Confirm</span></span>
<span data-ttu-id="7aa2f-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aa2f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aa2f-123">-WhatIf</span></span>
<span data-ttu-id="7aa2f-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aa2f-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aa2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa2f-126">CommonParameters</span></span>
<span data-ttu-id="7aa2f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7aa2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa2f-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aa2f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa2f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7aa2f-129">INPUTS</span></span>

## <span data-ttu-id="7aa2f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7aa2f-130">OUTPUTS</span></span>

### <span data-ttu-id="7aa2f-131">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci</span><span class="sxs-lookup"><span data-stu-id="7aa2f-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="7aa2f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7aa2f-132">NOTES</span></span>

## <span data-ttu-id="7aa2f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7aa2f-133">RELATED LINKS</span></span>

