---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 885fef88b1042fb538c4e07b62410943063cb53d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571874"
---
# <span data-ttu-id="80991-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="80991-101">Get-AzsOffer</span></span>

## <span data-ttu-id="80991-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80991-102">SYNOPSIS</span></span>
<span data-ttu-id="80991-103">Genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="80991-103">Get the list of public offers.</span></span>

## <span data-ttu-id="80991-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80991-104">SYNTAX</span></span>

```
Get-AzsOffer [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="80991-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80991-105">DESCRIPTION</span></span>
<span data-ttu-id="80991-106">Genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="80991-106">Get the list of public offers.</span></span>

## <span data-ttu-id="80991-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80991-107">EXAMPLES</span></span>

### <span data-ttu-id="80991-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="80991-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOffer | fl
```

<span data-ttu-id="80991-109">Genel teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="80991-109">Get the list of public offers.</span></span>

## <span data-ttu-id="80991-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80991-110">PARAMETERS</span></span>

### <span data-ttu-id="80991-111">-Atla</span><span class="sxs-lookup"><span data-stu-id="80991-111">-Skip</span></span>
<span data-ttu-id="80991-112">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="80991-112">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="80991-113">-Üst</span><span class="sxs-lookup"><span data-stu-id="80991-113">-Top</span></span>
<span data-ttu-id="80991-114">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="80991-114">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="80991-115">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="80991-115">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="80991-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80991-116">CommonParameters</span></span>
<span data-ttu-id="80991-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80991-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80991-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80991-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80991-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80991-119">INPUTS</span></span>

## <span data-ttu-id="80991-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80991-120">OUTPUTS</span></span>

### <span data-ttu-id="80991-121">Microsoft. AzureStack. Management. Subscription. modeller.</span><span class="sxs-lookup"><span data-stu-id="80991-121">Microsoft.AzureStack.Management.Subscription.Models.Offer</span></span>

## <span data-ttu-id="80991-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80991-122">NOTES</span></span>

## <span data-ttu-id="80991-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80991-123">RELATED LINKS</span></span>

