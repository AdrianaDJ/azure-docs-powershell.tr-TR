---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 78c0e9d2796cd6edf1a2d094cc6dd3b37614e3aa
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107003"
---
# <span data-ttu-id="3fa30-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="3fa30-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="3fa30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fa30-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa30-103">Yeni bir teklif temsilcisi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3fa30-103">Create a new offer delegation.</span></span>

## <span data-ttu-id="3fa30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3fa30-104">SYNTAX</span></span>

```
New-AzsOfferDelegation [-Name] <String> [-OfferName] <String> [-SubscriptionId] <String>
 [-ResourceGroupName] <String> [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fa30-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3fa30-105">DESCRIPTION</span></span>
<span data-ttu-id="3fa30-106">Yeni bir teklif temsilcisi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3fa30-106">Create a new offer delegation.</span></span>

## <span data-ttu-id="3fa30-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3fa30-107">EXAMPLES</span></span>

### <span data-ttu-id="3fa30-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3fa30-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="3fa30-109">Yeni bir teklif temsilcisi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3fa30-109">Create a new offer delegation.</span></span>

## <span data-ttu-id="3fa30-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3fa30-110">PARAMETERS</span></span>

### <span data-ttu-id="3fa30-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="3fa30-111">-Location</span></span>
<span data-ttu-id="3fa30-112">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="3fa30-112">Location of the resource.</span></span>

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

### <span data-ttu-id="3fa30-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3fa30-113">-Name</span></span>
<span data-ttu-id="3fa30-114">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="3fa30-114">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="3fa30-115">-OfferName</span><span class="sxs-lookup"><span data-stu-id="3fa30-115">-OfferName</span></span>
<span data-ttu-id="3fa30-116">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="3fa30-116">Name of an offer.</span></span>

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

### <span data-ttu-id="3fa30-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa30-117">-ResourceGroupName</span></span>
<span data-ttu-id="3fa30-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3fa30-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3fa30-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3fa30-119">-SubscriptionId</span></span>
<span data-ttu-id="3fa30-120">Temsilci teklif alma aboneliğinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3fa30-120">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="3fa30-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="3fa30-121">-Confirm</span></span>
<span data-ttu-id="3fa30-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3fa30-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fa30-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fa30-123">-WhatIf</span></span>
<span data-ttu-id="3fa30-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3fa30-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fa30-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3fa30-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fa30-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa30-126">CommonParameters</span></span>
<span data-ttu-id="3fa30-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3fa30-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa30-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa30-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa30-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3fa30-129">INPUTS</span></span>

## <span data-ttu-id="3fa30-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3fa30-130">OUTPUTS</span></span>

### <span data-ttu-id="3fa30-131">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci</span><span class="sxs-lookup"><span data-stu-id="3fa30-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="3fa30-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3fa30-132">NOTES</span></span>

## <span data-ttu-id="3fa30-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3fa30-133">RELATED LINKS</span></span>

