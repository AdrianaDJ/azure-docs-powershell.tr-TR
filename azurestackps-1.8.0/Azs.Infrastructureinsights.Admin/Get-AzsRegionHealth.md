---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934696"
---
# <span data-ttu-id="c9c17-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="c9c17-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="c9c17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c17-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c17-103">Bölgenin uygunluk durumu listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c9c17-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="c9c17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9c17-104">SYNTAX</span></span>

### <span data-ttu-id="c9c17-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9c17-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c17-106">Al</span><span class="sxs-lookup"><span data-stu-id="c9c17-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c9c17-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="c9c17-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c9c17-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9c17-108">DESCRIPTION</span></span>
<span data-ttu-id="c9c17-109">Bölgenin uygunluk durumu listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c9c17-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="c9c17-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9c17-110">EXAMPLES</span></span>

### <span data-ttu-id="c9c17-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="c9c17-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="c9c17-112">Bölgenin uygunluk durumu listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c9c17-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="c9c17-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9c17-113">PARAMETERS</span></span>

### <span data-ttu-id="c9c17-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="c9c17-114">-Location</span></span>
<span data-ttu-id="c9c17-115">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="c9c17-115">Name of the region</span></span>

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

### <span data-ttu-id="c9c17-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c17-116">-ResourceGroupName</span></span>
<span data-ttu-id="c9c17-117">Kaynak grubu adı, isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="c9c17-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="c9c17-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c9c17-118">-ResourceId</span></span>
<span data-ttu-id="c9c17-119">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c9c17-119">The resource id.</span></span>

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

### <span data-ttu-id="c9c17-120">-Filtre</span><span class="sxs-lookup"><span data-stu-id="c9c17-120">-Filter</span></span>
<span data-ttu-id="c9c17-121">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="c9c17-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="c9c17-122">-Üst</span><span class="sxs-lookup"><span data-stu-id="c9c17-122">-Top</span></span>
<span data-ttu-id="c9c17-123">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="c9c17-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c9c17-124">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c9c17-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c9c17-125">-Atla</span><span class="sxs-lookup"><span data-stu-id="c9c17-125">-Skip</span></span>
<span data-ttu-id="c9c17-126">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="c9c17-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c9c17-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c17-127">CommonParameters</span></span>
<span data-ttu-id="c9c17-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9c17-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c17-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9c17-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c17-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9c17-130">INPUTS</span></span>

## <span data-ttu-id="c9c17-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9c17-131">OUTPUTS</span></span>

### <span data-ttu-id="c9c17-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. modeller. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="c9c17-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="c9c17-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9c17-133">NOTES</span></span>

## <span data-ttu-id="c9c17-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9c17-134">RELATED LINKS</span></span>
