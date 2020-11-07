---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ea8b09e956410184dbc2dd2ed7fa8fc8b89c69b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934753"
---
# <span data-ttu-id="57fce-101">New-OfferDelegationObject</span><span class="sxs-lookup"><span data-stu-id="57fce-101">New-OfferDelegationObject</span></span>

## <span data-ttu-id="57fce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57fce-102">SYNOPSIS</span></span>
<span data-ttu-id="57fce-103">Temsilci seçme.</span><span class="sxs-lookup"><span data-stu-id="57fce-103">Offer delegation.</span></span>

## <span data-ttu-id="57fce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57fce-104">SYNTAX</span></span>

```
New-OfferDelegationObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-SubscriptionId] <String>]
 [[-Name] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="57fce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57fce-105">DESCRIPTION</span></span>
<span data-ttu-id="57fce-106">Temsilci seçme.</span><span class="sxs-lookup"><span data-stu-id="57fce-106">Offer delegation.</span></span>

## <span data-ttu-id="57fce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57fce-107">EXAMPLES</span></span>

### <span data-ttu-id="57fce-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="57fce-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="57fce-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="57fce-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="57fce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57fce-110">PARAMETERS</span></span>

### <span data-ttu-id="57fce-111">-ID</span><span class="sxs-lookup"><span data-stu-id="57fce-111">-Id</span></span>
<span data-ttu-id="57fce-112">Kaynağın URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="57fce-112">URI of the resource.</span></span>

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

### <span data-ttu-id="57fce-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="57fce-113">-Location</span></span>
<span data-ttu-id="57fce-114">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="57fce-114">Location of the resource.</span></span>

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

### <span data-ttu-id="57fce-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="57fce-115">-Name</span></span>
<span data-ttu-id="57fce-116">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="57fce-116">Name of the resource.</span></span>

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

### <span data-ttu-id="57fce-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="57fce-117">-SubscriptionId</span></span>
<span data-ttu-id="57fce-118">Temsilci teklif alma aboneliğinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="57fce-118">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="57fce-119">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="57fce-119">-Tags</span></span>
<span data-ttu-id="57fce-120">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="57fce-120">List of key-value pairs.</span></span>

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

### <span data-ttu-id="57fce-121">-Tür</span><span class="sxs-lookup"><span data-stu-id="57fce-121">-Type</span></span>
<span data-ttu-id="57fce-122">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="57fce-122">Type of resource.</span></span>

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

### <span data-ttu-id="57fce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fce-123">CommonParameters</span></span>
<span data-ttu-id="57fce-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57fce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fce-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57fce-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fce-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57fce-126">INPUTS</span></span>

## <span data-ttu-id="57fce-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57fce-127">OUTPUTS</span></span>

## <span data-ttu-id="57fce-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57fce-128">NOTES</span></span>

## <span data-ttu-id="57fce-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57fce-129">RELATED LINKS</span></span>

