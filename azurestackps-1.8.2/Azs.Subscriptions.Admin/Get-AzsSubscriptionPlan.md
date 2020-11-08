---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2cb2886e84b42d499fb04693757cee333458f9b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106873"
---
# <span data-ttu-id="410c2-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="410c2-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="410c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="410c2-102">SYNOPSIS</span></span>
<span data-ttu-id="410c2-103">Aboneliğin erişimi olan tüm alınan planların koleksiyonunu edinin.</span><span class="sxs-lookup"><span data-stu-id="410c2-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="410c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="410c2-104">SYNTAX</span></span>

### <span data-ttu-id="410c2-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="410c2-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="410c2-106">Al</span><span class="sxs-lookup"><span data-stu-id="410c2-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="410c2-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="410c2-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="410c2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="410c2-108">DESCRIPTION</span></span>
<span data-ttu-id="410c2-109">Aboneliğin erişimi olan tüm alınan planların koleksiyonunu edinin.</span><span class="sxs-lookup"><span data-stu-id="410c2-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="410c2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="410c2-110">EXAMPLES</span></span>

### <span data-ttu-id="410c2-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="410c2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="410c2-112">Aboneliğin erişimi olan tüm alınan planların koleksiyonunu edinin.</span><span class="sxs-lookup"><span data-stu-id="410c2-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="410c2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="410c2-113">PARAMETERS</span></span>

### <span data-ttu-id="410c2-114">-Tanışın kimliği</span><span class="sxs-lookup"><span data-stu-id="410c2-114">-AcquisitionId</span></span>
<span data-ttu-id="410c2-115">Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="410c2-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="410c2-116">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="410c2-116">-ResourceId</span></span>
<span data-ttu-id="410c2-117">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="410c2-117">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="410c2-118">-Atla</span><span class="sxs-lookup"><span data-stu-id="410c2-118">-Skip</span></span>
<span data-ttu-id="410c2-119">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="410c2-119">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="410c2-120">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="410c2-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="410c2-121">Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="410c2-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="410c2-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="410c2-122">-Top</span></span>
<span data-ttu-id="410c2-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="410c2-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="410c2-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="410c2-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="410c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="410c2-125">CommonParameters</span></span>
<span data-ttu-id="410c2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="410c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="410c2-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="410c2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="410c2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="410c2-128">INPUTS</span></span>

## <span data-ttu-id="410c2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="410c2-129">OUTPUTS</span></span>

### <span data-ttu-id="410c2-130">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Planalımı</span><span class="sxs-lookup"><span data-stu-id="410c2-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="410c2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="410c2-131">NOTES</span></span>

## <span data-ttu-id="410c2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="410c2-132">RELATED LINKS</span></span>

