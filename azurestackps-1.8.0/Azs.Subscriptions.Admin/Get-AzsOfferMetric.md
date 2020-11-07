---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d0dad3650338d2bba4976ce66806b714bd9e0fe
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934773"
---
# <span data-ttu-id="30900-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="30900-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="30900-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30900-102">SYNOPSIS</span></span>
<span data-ttu-id="30900-103">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="30900-103">Get the offer metrics.</span></span>

## <span data-ttu-id="30900-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30900-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="30900-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30900-105">DESCRIPTION</span></span>
<span data-ttu-id="30900-106">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="30900-106">Get the offer metrics.</span></span>

## <span data-ttu-id="30900-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30900-107">EXAMPLES</span></span>

### <span data-ttu-id="30900-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="30900-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="30900-109">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="30900-109">Get the offer metrics.</span></span>

## <span data-ttu-id="30900-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30900-110">PARAMETERS</span></span>

### <span data-ttu-id="30900-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="30900-111">-OfferName</span></span>
<span data-ttu-id="30900-112">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="30900-112">Name of an offer.</span></span>

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

### <span data-ttu-id="30900-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30900-113">-ResourceGroupName</span></span>
<span data-ttu-id="30900-114">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="30900-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="30900-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30900-115">CommonParameters</span></span>
<span data-ttu-id="30900-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30900-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30900-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30900-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30900-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30900-118">INPUTS</span></span>

## <span data-ttu-id="30900-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30900-119">OUTPUTS</span></span>

### <span data-ttu-id="30900-120">Microsoft. AzureStack. Management. abonelikler. admin. modeller. metrik</span><span class="sxs-lookup"><span data-stu-id="30900-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="30900-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30900-121">NOTES</span></span>

## <span data-ttu-id="30900-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30900-122">RELATED LINKS</span></span>

