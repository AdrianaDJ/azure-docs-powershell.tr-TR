---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106972"
---
# <span data-ttu-id="ad4d2-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="ad4d2-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="ad4d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad4d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4d2-103">Temsilci seçilen tekliflerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="ad4d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad4d2-104">SYNTAX</span></span>

### <span data-ttu-id="ad4d2-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad4d2-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad4d2-106">Al</span><span class="sxs-lookup"><span data-stu-id="ad4d2-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="ad4d2-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="ad4d2-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ad4d2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad4d2-108">DESCRIPTION</span></span>
<span data-ttu-id="ad4d2-109">Temsilci seçilen tekliflerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="ad4d2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad4d2-110">EXAMPLES</span></span>

### <span data-ttu-id="ad4d2-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ad4d2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="ad4d2-112">Temsilci seçilen tekliflerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="ad4d2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad4d2-113">PARAMETERS</span></span>

### <span data-ttu-id="ad4d2-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad4d2-114">-Name</span></span>
<span data-ttu-id="ad4d2-115">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="ad4d2-116">-OfferName</span><span class="sxs-lookup"><span data-stu-id="ad4d2-116">-OfferName</span></span>
<span data-ttu-id="ad4d2-117">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-117">Name of an offer.</span></span>

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

### <span data-ttu-id="ad4d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="ad4d2-119">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="ad4d2-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ad4d2-120">-ResourceId</span></span>
<span data-ttu-id="ad4d2-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-121">The resource id.</span></span>

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

### <span data-ttu-id="ad4d2-122">-Atla</span><span class="sxs-lookup"><span data-stu-id="ad4d2-122">-Skip</span></span>
<span data-ttu-id="ad4d2-123">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ad4d2-124">-Üst</span><span class="sxs-lookup"><span data-stu-id="ad4d2-124">-Top</span></span>
<span data-ttu-id="ad4d2-125">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ad4d2-126">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ad4d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4d2-127">CommonParameters</span></span>
<span data-ttu-id="ad4d2-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad4d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4d2-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4d2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4d2-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad4d2-130">INPUTS</span></span>

## <span data-ttu-id="ad4d2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad4d2-131">OUTPUTS</span></span>

### <span data-ttu-id="ad4d2-132">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Offertemsilci</span><span class="sxs-lookup"><span data-stu-id="ad4d2-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="ad4d2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad4d2-133">NOTES</span></span>

## <span data-ttu-id="ad4d2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad4d2-134">RELATED LINKS</span></span>

