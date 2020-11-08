---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106853"
---
# <span data-ttu-id="661b9-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="661b9-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="661b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="661b9-102">SYNOPSIS</span></span>
<span data-ttu-id="661b9-103">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="661b9-103">Get the offer metrics.</span></span>

## <span data-ttu-id="661b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="661b9-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="661b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="661b9-105">DESCRIPTION</span></span>
<span data-ttu-id="661b9-106">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="661b9-106">Get the offer metrics.</span></span>

## <span data-ttu-id="661b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="661b9-107">EXAMPLES</span></span>

### <span data-ttu-id="661b9-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="661b9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="661b9-109">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="661b9-109">Get the offer metrics.</span></span>

## <span data-ttu-id="661b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="661b9-110">PARAMETERS</span></span>

### <span data-ttu-id="661b9-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="661b9-111">-OfferName</span></span>
<span data-ttu-id="661b9-112">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="661b9-112">Name of an offer.</span></span>

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

### <span data-ttu-id="661b9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="661b9-113">-ResourceGroupName</span></span>
<span data-ttu-id="661b9-114">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="661b9-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="661b9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661b9-115">CommonParameters</span></span>
<span data-ttu-id="661b9-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="661b9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661b9-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="661b9-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661b9-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="661b9-118">INPUTS</span></span>

## <span data-ttu-id="661b9-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="661b9-119">OUTPUTS</span></span>

### <span data-ttu-id="661b9-120">Microsoft. AzureStack. Management. abonelikler. admin. modeller. metrik</span><span class="sxs-lookup"><span data-stu-id="661b9-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="661b9-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="661b9-121">NOTES</span></span>

## <span data-ttu-id="661b9-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="661b9-122">RELATED LINKS</span></span>

