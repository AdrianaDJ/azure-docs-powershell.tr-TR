---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cadf5ad37119ab6b50191e50e8ec281fe4bce2d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934301"
---
# <span data-ttu-id="7ea5b-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="7ea5b-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="7ea5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ea5b-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea5b-103">Plan ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-103">Get the plan metrics.</span></span>

## <span data-ttu-id="7ea5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ea5b-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="7ea5b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ea5b-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea5b-106">Plan ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-106">Get the plan metrics.</span></span>

## <span data-ttu-id="7ea5b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ea5b-107">EXAMPLES</span></span>

### <span data-ttu-id="7ea5b-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7ea5b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="7ea5b-109">Planın ölçümlerini alın.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="7ea5b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ea5b-110">PARAMETERS</span></span>

### <span data-ttu-id="7ea5b-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="7ea5b-111">-PlanName</span></span>
<span data-ttu-id="7ea5b-112">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-112">Name of the plan.</span></span>

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

### <span data-ttu-id="7ea5b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea5b-113">-ResourceGroupName</span></span>
<span data-ttu-id="7ea5b-114">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="7ea5b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea5b-115">CommonParameters</span></span>
<span data-ttu-id="7ea5b-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ea5b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea5b-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea5b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea5b-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ea5b-118">INPUTS</span></span>

## <span data-ttu-id="7ea5b-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ea5b-119">OUTPUTS</span></span>

### <span data-ttu-id="7ea5b-120">Microsoft. AzureStack. Management. abonelikler. admin. modeller. metrik</span><span class="sxs-lookup"><span data-stu-id="7ea5b-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="7ea5b-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ea5b-121">NOTES</span></span>

## <span data-ttu-id="7ea5b-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ea5b-122">RELATED LINKS</span></span>

