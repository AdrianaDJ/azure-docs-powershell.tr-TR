---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106753"
---
# <span data-ttu-id="39163-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="39163-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="39163-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39163-102">SYNOPSIS</span></span>
<span data-ttu-id="39163-103">Temsilci seçme.</span><span class="sxs-lookup"><span data-stu-id="39163-103">Offer delegation.</span></span>

## <span data-ttu-id="39163-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39163-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="39163-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="39163-105">DESCRIPTION</span></span>
<span data-ttu-id="39163-106">Temsilci seçme.</span><span class="sxs-lookup"><span data-stu-id="39163-106">Offer delegation.</span></span>

## <span data-ttu-id="39163-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39163-107">EXAMPLES</span></span>

### <span data-ttu-id="39163-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="39163-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="39163-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="39163-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="39163-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39163-110">PARAMETERS</span></span>

### <span data-ttu-id="39163-111">-ID</span><span class="sxs-lookup"><span data-stu-id="39163-111">-Id</span></span>
<span data-ttu-id="39163-112">Kaynağın URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="39163-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39163-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="39163-113">-Location</span></span>
<span data-ttu-id="39163-114">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="39163-114">Location of the resource.</span></span>

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

### <span data-ttu-id="39163-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="39163-115">-Name</span></span>
<span data-ttu-id="39163-116">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="39163-116">Name of the resource.</span></span>

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

### <span data-ttu-id="39163-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="39163-117">-SubscriptionId</span></span>
<span data-ttu-id="39163-118">Temsilci teklif alma aboneliğinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="39163-118">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39163-119">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="39163-119">-Tags</span></span>
<span data-ttu-id="39163-120">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="39163-120">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39163-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="39163-121">-Type</span></span>
<span data-ttu-id="39163-122">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="39163-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39163-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39163-123">CommonParameters</span></span>
<span data-ttu-id="39163-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39163-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39163-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39163-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39163-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39163-126">INPUTS</span></span>

## <span data-ttu-id="39163-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39163-127">OUTPUTS</span></span>

## <span data-ttu-id="39163-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39163-128">NOTES</span></span>

## <span data-ttu-id="39163-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39163-129">RELATED LINKS</span></span>

