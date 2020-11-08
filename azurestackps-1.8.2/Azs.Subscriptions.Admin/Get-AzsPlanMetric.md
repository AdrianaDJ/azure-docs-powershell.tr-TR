---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8ef41d414d12182c15d9ec5b01138e0110dee9f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107096"
---
# <span data-ttu-id="18b51-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="18b51-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="18b51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b51-102">SYNOPSIS</span></span>
<span data-ttu-id="18b51-103">Plan ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="18b51-103">Get the plan metrics.</span></span>

## <span data-ttu-id="18b51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18b51-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="18b51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18b51-105">DESCRIPTION</span></span>
<span data-ttu-id="18b51-106">Plan ölçülerini edinin.</span><span class="sxs-lookup"><span data-stu-id="18b51-106">Get the plan metrics.</span></span>

## <span data-ttu-id="18b51-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18b51-107">EXAMPLES</span></span>

### <span data-ttu-id="18b51-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="18b51-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="18b51-109">Planın ölçümlerini alın.</span><span class="sxs-lookup"><span data-stu-id="18b51-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="18b51-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18b51-110">PARAMETERS</span></span>

### <span data-ttu-id="18b51-111">-PlanName</span><span class="sxs-lookup"><span data-stu-id="18b51-111">-PlanName</span></span>
<span data-ttu-id="18b51-112">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="18b51-112">Name of the plan.</span></span>

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

### <span data-ttu-id="18b51-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18b51-113">-ResourceGroupName</span></span>
<span data-ttu-id="18b51-114">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="18b51-114">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="18b51-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b51-115">CommonParameters</span></span>
<span data-ttu-id="18b51-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18b51-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b51-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b51-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b51-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18b51-118">INPUTS</span></span>

## <span data-ttu-id="18b51-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18b51-119">OUTPUTS</span></span>

### <span data-ttu-id="18b51-120">Microsoft. AzureStack. Management. abonelikler. admin. modeller. metrik</span><span class="sxs-lookup"><span data-stu-id="18b51-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="18b51-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18b51-121">NOTES</span></span>

## <span data-ttu-id="18b51-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18b51-122">RELATED LINKS</span></span>

