---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107173"
---
# <span data-ttu-id="a7e8a-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="a7e8a-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="a7e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e8a-103">Bir konumdaki tüm ölçek birimi düğümlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="a7e8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7e8a-104">SYNTAX</span></span>

### <span data-ttu-id="a7e8a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7e8a-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a7e8a-106">Al</span><span class="sxs-lookup"><span data-stu-id="a7e8a-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="a7e8a-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a7e8a-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a7e8a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="a7e8a-109">Bir konumdaki tüm ölçek birimi düğümlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="a7e8a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7e8a-110">EXAMPLES</span></span>

### <span data-ttu-id="a7e8a-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="a7e8a-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="a7e8a-112">Bir konumdaki tüm ölçek birim düğümlerini alın.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="a7e8a-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="a7e8a-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="a7e8a-114">Bir ad verilen konumda belirli bir ölçek birimi düğümünü edinin.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="a7e8a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7e8a-115">PARAMETERS</span></span>

### <span data-ttu-id="a7e8a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7e8a-116">-Name</span></span>
<span data-ttu-id="a7e8a-117">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="a7e8a-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="a7e8a-118">-Location</span></span>
<span data-ttu-id="a7e8a-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="a7e8a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7e8a-120">-ResourceGroupName</span></span>
<span data-ttu-id="a7e8a-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="a7e8a-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a7e8a-122">-ResourceId</span></span>
<span data-ttu-id="a7e8a-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-123">The resource id.</span></span>

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

### <span data-ttu-id="a7e8a-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="a7e8a-124">-Filter</span></span>
<span data-ttu-id="a7e8a-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="a7e8a-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="a7e8a-126">-Skip</span></span>
<span data-ttu-id="a7e8a-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a7e8a-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="a7e8a-128">-Top</span></span>
<span data-ttu-id="a7e8a-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a7e8a-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a7e8a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e8a-131">CommonParameters</span></span>
<span data-ttu-id="a7e8a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7e8a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e8a-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e8a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e8a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7e8a-134">INPUTS</span></span>

## <span data-ttu-id="a7e8a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7e8a-135">OUTPUTS</span></span>

### <span data-ttu-id="a7e8a-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="a7e8a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="a7e8a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7e8a-137">NOTES</span></span>

## <span data-ttu-id="a7e8a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7e8a-138">RELATED LINKS</span></span>
