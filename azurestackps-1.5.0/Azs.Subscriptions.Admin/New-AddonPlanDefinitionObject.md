---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7074752cda5997bba0536cf891675f59e734e509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572297"
---
# <span data-ttu-id="f4e61-101">New-AddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="f4e61-101">New-AddonPlanDefinitionObject</span></span>

## <span data-ttu-id="f4e61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e61-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e61-103">Bir teklifin bağlanacağı veya bağlantısının istendiği istenen planın adını içerir.</span><span class="sxs-lookup"><span data-stu-id="f4e61-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="f4e61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4e61-104">SYNTAX</span></span>

```
New-AddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="f4e61-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4e61-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e61-106">Bir teklifin bağlanacağı veya bağlantısının istendiği istenen planın adını içerir.</span><span class="sxs-lookup"><span data-stu-id="f4e61-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="f4e61-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4e61-107">EXAMPLES</span></span>

### <span data-ttu-id="f4e61-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f4e61-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="f4e61-109">Belirtilen plan için 500 alma sınırı ile yeni bir plan tanımı nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f4e61-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="f4e61-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4e61-110">PARAMETERS</span></span>

### <span data-ttu-id="f4e61-111">-Maxtanışan</span><span class="sxs-lookup"><span data-stu-id="f4e61-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="f4e61-112">Tek bir abonelikle edinildiği en fazla örnek sayısı.</span><span class="sxs-lookup"><span data-stu-id="f4e61-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="f4e61-113">Belirtilmemişse, kabul edilen değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="f4e61-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e61-114">-Plankimliği</span><span class="sxs-lookup"><span data-stu-id="f4e61-114">-PlanId</span></span>
<span data-ttu-id="f4e61-115">Plan tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f4e61-115">Plan identifier.</span></span>

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

### <span data-ttu-id="f4e61-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e61-116">CommonParameters</span></span>
<span data-ttu-id="f4e61-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4e61-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e61-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e61-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e61-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4e61-119">INPUTS</span></span>

## <span data-ttu-id="f4e61-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4e61-120">OUTPUTS</span></span>

## <span data-ttu-id="f4e61-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4e61-121">NOTES</span></span>

## <span data-ttu-id="f4e61-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4e61-122">RELATED LINKS</span></span>

