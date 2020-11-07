---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8228a8605462b71fce598c7dc44454a16e1d7c90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934494"
---
# <span data-ttu-id="6481a-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="6481a-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="6481a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6481a-102">SYNOPSIS</span></span>
<span data-ttu-id="6481a-103">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="6481a-103">Get the offer metrics.</span></span>

## <span data-ttu-id="6481a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6481a-104">SYNTAX</span></span>

```
Get-AzsOfferMetric [-OfferName] <String> [-ResourceGroupName] <String> [<CommonParameters>]
```

## <span data-ttu-id="6481a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6481a-105">DESCRIPTION</span></span>
<span data-ttu-id="6481a-106">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="6481a-106">Get the offer metrics.</span></span>

## <span data-ttu-id="6481a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6481a-107">EXAMPLES</span></span>

### <span data-ttu-id="6481a-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6481a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferMetric -ResourceGroupName rg1 -OfferName offername1
```

<span data-ttu-id="6481a-109">Teklif ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="6481a-109">Get the offer metrics.</span></span>

## <span data-ttu-id="6481a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6481a-110">PARAMETERS</span></span>

### <span data-ttu-id="6481a-111">-OfferName</span><span class="sxs-lookup"><span data-stu-id="6481a-111">-OfferName</span></span>
<span data-ttu-id="6481a-112">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="6481a-112">Name of an offer.</span></span>

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

### <span data-ttu-id="6481a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6481a-113">-ResourceGroupName</span></span>
<span data-ttu-id="6481a-114">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="6481a-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6481a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6481a-115">CommonParameters</span></span>
<span data-ttu-id="6481a-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6481a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6481a-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6481a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6481a-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6481a-118">INPUTS</span></span>

## <span data-ttu-id="6481a-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6481a-119">OUTPUTS</span></span>

### <span data-ttu-id="6481a-120">Microsoft. AzureStack. Management. abonelikler. admin. modeller. metrik</span><span class="sxs-lookup"><span data-stu-id="6481a-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="6481a-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6481a-121">NOTES</span></span>

## <span data-ttu-id="6481a-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6481a-122">RELATED LINKS</span></span>

