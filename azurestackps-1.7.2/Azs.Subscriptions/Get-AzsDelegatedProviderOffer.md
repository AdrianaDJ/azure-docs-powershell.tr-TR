---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8034887f8b44bef5c3dd59f73186027af1a1e5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934244"
---
# <span data-ttu-id="68b26-101">Get-AzsDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="68b26-101">Get-AzsDelegatedProviderOffer</span></span>

## <span data-ttu-id="68b26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68b26-102">SYNOPSIS</span></span>
<span data-ttu-id="68b26-103">Belirtilen temsilci seçilen sağlayıcı için teklifler listesini alın.</span><span class="sxs-lookup"><span data-stu-id="68b26-103">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="68b26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68b26-104">SYNTAX</span></span>

### <span data-ttu-id="68b26-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68b26-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="68b26-106">Al</span><span class="sxs-lookup"><span data-stu-id="68b26-106">Get</span></span>
```
Get-AzsDelegatedProviderOffer -Name <String> -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="68b26-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="68b26-107">DESCRIPTION</span></span>
<span data-ttu-id="68b26-108">Belirtilen temsilci seçilen sağlayıcı için teklifler listesini alın.</span><span class="sxs-lookup"><span data-stu-id="68b26-108">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="68b26-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68b26-109">EXAMPLES</span></span>

### <span data-ttu-id="68b26-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="68b26-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderOffer -DelegatedProviderId 4b763321-23f5-4a45-a44d-9ccfdd705a3d | fl
```

<span data-ttu-id="68b26-111">Belirtilen temsilci seçilen sağlayıcı için teklifler listesini alın.</span><span class="sxs-lookup"><span data-stu-id="68b26-111">Get the list of offers for the specified delegated provider.</span></span>

## <span data-ttu-id="68b26-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68b26-112">PARAMETERS</span></span>

### <span data-ttu-id="68b26-113">-Delegatevseçproviderıd</span><span class="sxs-lookup"><span data-stu-id="68b26-113">-DelegatedProviderId</span></span>
<span data-ttu-id="68b26-114">Temsilci sağlayıcı kimliği.</span><span class="sxs-lookup"><span data-stu-id="68b26-114">Id of the delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b26-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="68b26-115">-Name</span></span>
<span data-ttu-id="68b26-116">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="68b26-116">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: OfferName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b26-117">-Atla</span><span class="sxs-lookup"><span data-stu-id="68b26-117">-Skip</span></span>
<span data-ttu-id="68b26-118">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="68b26-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b26-119">-Üst</span><span class="sxs-lookup"><span data-stu-id="68b26-119">-Top</span></span>
<span data-ttu-id="68b26-120">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="68b26-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="68b26-121">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="68b26-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b26-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b26-122">CommonParameters</span></span>
<span data-ttu-id="68b26-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68b26-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b26-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68b26-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b26-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68b26-125">INPUTS</span></span>

## <span data-ttu-id="68b26-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68b26-126">OUTPUTS</span></span>

### <span data-ttu-id="68b26-127">Microsoft. AzureStack. Management. Subscription. modeller.</span><span class="sxs-lookup"><span data-stu-id="68b26-127">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="68b26-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68b26-128">NOTES</span></span>

## <span data-ttu-id="68b26-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68b26-129">RELATED LINKS</span></span>
