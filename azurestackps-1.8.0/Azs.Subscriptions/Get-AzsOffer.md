---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934733"
---
# <span data-ttu-id="23972-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="23972-101">Get-AzsOffer</span></span>

## <span data-ttu-id="23972-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23972-102">SYNOPSIS</span></span>
<span data-ttu-id="23972-103">Genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="23972-103">Get the list of public offers.</span></span>

## <span data-ttu-id="23972-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23972-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="23972-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23972-105">DESCRIPTION</span></span>
<span data-ttu-id="23972-106">Genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="23972-106">Get the list of public offers.</span></span>

## <span data-ttu-id="23972-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23972-107">EXAMPLES</span></span>

### <span data-ttu-id="23972-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="23972-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="23972-109">Genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="23972-109">Get the list of public offers.</span></span>

## <span data-ttu-id="23972-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23972-110">PARAMETERS</span></span>

### <span data-ttu-id="23972-111">-Atla</span><span class="sxs-lookup"><span data-stu-id="23972-111">-Skip</span></span>
<span data-ttu-id="23972-112">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="23972-112">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23972-113">-Üst</span><span class="sxs-lookup"><span data-stu-id="23972-113">-Top</span></span>
<span data-ttu-id="23972-114">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="23972-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="23972-115">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="23972-115">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23972-116">-Sağlayıcı</span><span class="sxs-lookup"><span data-stu-id="23972-116">-Provider</span></span>
<span data-ttu-id="23972-117">Temsilci sağlayıcı adını belirtmek için isteğe bağlı parametre.</span><span class="sxs-lookup"><span data-stu-id="23972-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="23972-118">Bu parametre kullanılmıyor ve gelecekte kullanım dışı olacak.</span><span class="sxs-lookup"><span data-stu-id="23972-118">This parameter is not being used and will be deprecated in future.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23972-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23972-119">CommonParameters</span></span>
<span data-ttu-id="23972-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23972-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23972-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23972-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23972-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23972-122">INPUTS</span></span>

## <span data-ttu-id="23972-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23972-123">OUTPUTS</span></span>

### <span data-ttu-id="23972-124">Microsoft. AzureStack. Management. Subscription. modeller.</span><span class="sxs-lookup"><span data-stu-id="23972-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="23972-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23972-125">NOTES</span></span>

## <span data-ttu-id="23972-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23972-126">RELATED LINKS</span></span>
