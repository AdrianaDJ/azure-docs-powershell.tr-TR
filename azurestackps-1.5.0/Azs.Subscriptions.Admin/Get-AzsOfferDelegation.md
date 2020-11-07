---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761801"
---
# <span data-ttu-id="24a5b-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="24a5b-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="24a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="24a5b-103">Temsilci seçilen tekliflerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="24a5b-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="24a5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24a5b-104">SYNTAX</span></span>

### <span data-ttu-id="24a5b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="24a5b-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="24a5b-106">Al</span><span class="sxs-lookup"><span data-stu-id="24a5b-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="24a5b-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="24a5b-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="24a5b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="24a5b-108">DESCRIPTION</span></span>
<span data-ttu-id="24a5b-109">Temsilci seçilen tekliflerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="24a5b-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="24a5b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24a5b-110">EXAMPLES</span></span>

### <span data-ttu-id="24a5b-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="24a5b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="24a5b-112">Temsilci seçilen tekliflerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="24a5b-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="24a5b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24a5b-113">PARAMETERS</span></span>

### <span data-ttu-id="24a5b-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="24a5b-114">-Name</span></span>
<span data-ttu-id="24a5b-115">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="24a5b-115">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a5b-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="24a5b-116">-OfferName</span></span>
<span data-ttu-id="24a5b-117">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="24a5b-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a5b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a5b-118">-ResourceGroupName</span></span>
<span data-ttu-id="24a5b-119">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="24a5b-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a5b-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="24a5b-120">-ResourceId</span></span>
<span data-ttu-id="24a5b-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="24a5b-121">The resource id.</span></span>

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

### <span data-ttu-id="24a5b-122">-Atla</span><span class="sxs-lookup"><span data-stu-id="24a5b-122">-Skip</span></span>
<span data-ttu-id="24a5b-123">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="24a5b-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a5b-124">-Üst</span><span class="sxs-lookup"><span data-stu-id="24a5b-124">-Top</span></span>
<span data-ttu-id="24a5b-125">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="24a5b-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="24a5b-126">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="24a5b-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24a5b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a5b-127">CommonParameters</span></span>
<span data-ttu-id="24a5b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24a5b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a5b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24a5b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24a5b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24a5b-130">INPUTS</span></span>

## <span data-ttu-id="24a5b-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24a5b-131">OUTPUTS</span></span>

### <span data-ttu-id="24a5b-132">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci</span><span class="sxs-lookup"><span data-stu-id="24a5b-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="24a5b-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24a5b-133">NOTES</span></span>

## <span data-ttu-id="24a5b-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24a5b-134">RELATED LINKS</span></span>

