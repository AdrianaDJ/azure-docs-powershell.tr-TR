---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77d6a4861dbdb93dff2d5511faeceac30e3f9cf8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935041"
---
# <span data-ttu-id="e9cb5-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="e9cb5-101">Get-AzsOffer</span></span>

## <span data-ttu-id="e9cb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="e9cb5-103">Genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-103">Get the list of public offers.</span></span>

## <span data-ttu-id="e9cb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9cb5-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [[-Provider] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e9cb5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9cb5-105">DESCRIPTION</span></span>
<span data-ttu-id="e9cb5-106">Genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-106">Get the list of public offers.</span></span>

## <span data-ttu-id="e9cb5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9cb5-107">EXAMPLES</span></span>

### <span data-ttu-id="e9cb5-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="e9cb5-108">EXAMPLE 1</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="e9cb5-109">Genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-109">Get the list of public offers.</span></span>

## <span data-ttu-id="e9cb5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9cb5-110">PARAMETERS</span></span>

### <span data-ttu-id="e9cb5-111">-Atla</span><span class="sxs-lookup"><span data-stu-id="e9cb5-111">-Skip</span></span>
<span data-ttu-id="e9cb5-112">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e9cb5-113">-Üst</span><span class="sxs-lookup"><span data-stu-id="e9cb5-113">-Top</span></span>
<span data-ttu-id="e9cb5-114">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e9cb5-115">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e9cb5-116">-Sağlayıcı</span><span class="sxs-lookup"><span data-stu-id="e9cb5-116">-Provider</span></span>
<span data-ttu-id="e9cb5-117">Temsilci sağlayıcı adını belirtmek için isteğe bağlı parametre.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-117">Optional parameter to specify the delegated provider name.</span></span> <span data-ttu-id="e9cb5-118">Bu parametre kullanılmıyor ve gelecekte kullanım dışı olacak.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-118">This parameter is not being used and will be deprecated in future.</span></span>

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

### <span data-ttu-id="e9cb5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9cb5-119">CommonParameters</span></span>
<span data-ttu-id="e9cb5-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9cb5-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9cb5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9cb5-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9cb5-122">INPUTS</span></span>

## <span data-ttu-id="e9cb5-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9cb5-123">OUTPUTS</span></span>

### <span data-ttu-id="e9cb5-124">Microsoft. AzureStack. Management. Subscription. modeller.</span><span class="sxs-lookup"><span data-stu-id="e9cb5-124">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="e9cb5-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9cb5-125">NOTES</span></span>

## <span data-ttu-id="e9cb5-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9cb5-126">RELATED LINKS</span></span>
