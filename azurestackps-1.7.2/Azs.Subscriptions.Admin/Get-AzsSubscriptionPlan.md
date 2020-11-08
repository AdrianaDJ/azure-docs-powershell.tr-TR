---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb583ca37f610d47c880fd2e15ae3e7b8182b5ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934251"
---
# <span data-ttu-id="cbfa5-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="cbfa5-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="cbfa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbfa5-102">SYNOPSIS</span></span>
<span data-ttu-id="cbfa5-103">Aboneliğin erişimi olan tüm alınan planların koleksiyonunu edinin.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="cbfa5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cbfa5-104">SYNTAX</span></span>

### <span data-ttu-id="cbfa5-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cbfa5-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cbfa5-106">Al</span><span class="sxs-lookup"><span data-stu-id="cbfa5-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="cbfa5-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="cbfa5-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cbfa5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cbfa5-108">DESCRIPTION</span></span>
<span data-ttu-id="cbfa5-109">Aboneliğin erişimi olan tüm alınan planların koleksiyonunu edinin.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="cbfa5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cbfa5-110">EXAMPLES</span></span>

### <span data-ttu-id="cbfa5-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cbfa5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="cbfa5-112">Aboneliğin erişimi olan tüm alınan planların koleksiyonunu edinin.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="cbfa5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cbfa5-113">PARAMETERS</span></span>

### <span data-ttu-id="cbfa5-114">-Tanışın kimliği</span><span class="sxs-lookup"><span data-stu-id="cbfa5-114">-AcquisitionId</span></span>
<span data-ttu-id="cbfa5-115">Plan alma tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="cbfa5-115">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="cbfa5-116">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cbfa5-116">-ResourceId</span></span>
<span data-ttu-id="cbfa5-117">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-117">The resource id.</span></span>

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

### <span data-ttu-id="cbfa5-118">-Atla</span><span class="sxs-lookup"><span data-stu-id="cbfa5-118">-Skip</span></span>
<span data-ttu-id="cbfa5-119">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-119">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="cbfa5-120">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="cbfa5-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="cbfa5-121">Hedef abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-121">The target subscription ID.</span></span>

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

### <span data-ttu-id="cbfa5-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="cbfa5-122">-Top</span></span>
<span data-ttu-id="cbfa5-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cbfa5-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="cbfa5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbfa5-125">CommonParameters</span></span>
<span data-ttu-id="cbfa5-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cbfa5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbfa5-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbfa5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbfa5-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cbfa5-128">INPUTS</span></span>

## <span data-ttu-id="cbfa5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cbfa5-129">OUTPUTS</span></span>

### <span data-ttu-id="cbfa5-130">Microsoft. AzureStack. Management. abonelikler. admin. modeller. Planalımı</span><span class="sxs-lookup"><span data-stu-id="cbfa5-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="cbfa5-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cbfa5-131">NOTES</span></span>

## <span data-ttu-id="cbfa5-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cbfa5-132">RELATED LINKS</span></span>
