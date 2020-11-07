---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d5870624b6d39b3e821ed6a7fb76d87c8422ab2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761730"
---
# <span data-ttu-id="97683-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="97683-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="97683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97683-102">SYNOPSIS</span></span>
<span data-ttu-id="97683-103">Bir konumdaki tüm ölçek birimi düğümlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="97683-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="97683-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97683-104">SYNTAX</span></span>

### <span data-ttu-id="97683-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97683-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="97683-106">Al</span><span class="sxs-lookup"><span data-stu-id="97683-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="97683-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="97683-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="97683-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="97683-108">DESCRIPTION</span></span>
<span data-ttu-id="97683-109">Bir konumdaki tüm ölçek birimi düğümlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="97683-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="97683-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97683-110">EXAMPLES</span></span>

### <span data-ttu-id="97683-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="97683-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="97683-112">Bir konumdaki tüm ölçek birim düğümlerini alın.</span><span class="sxs-lookup"><span data-stu-id="97683-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="97683-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="97683-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="97683-114">Bir ad verilen konumda belirli bir ölçek birimi düğümünü edinin.</span><span class="sxs-lookup"><span data-stu-id="97683-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="97683-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97683-115">PARAMETERS</span></span>

### <span data-ttu-id="97683-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="97683-116">-Filter</span></span>
<span data-ttu-id="97683-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="97683-117">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97683-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="97683-118">-Location</span></span>
<span data-ttu-id="97683-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="97683-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97683-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="97683-120">-Name</span></span>
<span data-ttu-id="97683-121">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="97683-121">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97683-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97683-122">-ResourceGroupName</span></span>
<span data-ttu-id="97683-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="97683-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97683-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97683-124">-ResourceId</span></span>
<span data-ttu-id="97683-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="97683-125">The resource id.</span></span>

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

### <span data-ttu-id="97683-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="97683-126">-Skip</span></span>
<span data-ttu-id="97683-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="97683-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="97683-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="97683-128">-Top</span></span>
<span data-ttu-id="97683-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="97683-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="97683-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="97683-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="97683-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97683-131">CommonParameters</span></span>
<span data-ttu-id="97683-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97683-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97683-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97683-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97683-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97683-134">INPUTS</span></span>

## <span data-ttu-id="97683-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97683-135">OUTPUTS</span></span>

### <span data-ttu-id="97683-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="97683-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="97683-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97683-137">NOTES</span></span>

## <span data-ttu-id="97683-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97683-138">RELATED LINKS</span></span>
