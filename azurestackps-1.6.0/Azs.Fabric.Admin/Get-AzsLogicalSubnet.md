---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572173"
---
# <span data-ttu-id="14bb2-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="14bb2-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="14bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="14bb2-103">Tüm mantıksal alt ağların bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="14bb2-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="14bb2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14bb2-104">SYNTAX</span></span>

### <span data-ttu-id="14bb2-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="14bb2-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="14bb2-106">Al</span><span class="sxs-lookup"><span data-stu-id="14bb2-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="14bb2-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="14bb2-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="14bb2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="14bb2-108">DESCRIPTION</span></span>
<span data-ttu-id="14bb2-109">Tüm mantıksal alt ağların bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="14bb2-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="14bb2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14bb2-110">EXAMPLES</span></span>

### <span data-ttu-id="14bb2-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="14bb2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="14bb2-112">Belirli bir mantıksal ağ ve konum için tüm mantıksal alt ağların bir listesini alın.</span><span class="sxs-lookup"><span data-stu-id="14bb2-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="14bb2-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="14bb2-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="14bb2-114">Belirli bir mantıksal ağ için belirli bir mantıksal ağ ve ada göre bir konum edinin.</span><span class="sxs-lookup"><span data-stu-id="14bb2-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="14bb2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14bb2-115">PARAMETERS</span></span>

### <span data-ttu-id="14bb2-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="14bb2-116">-Filter</span></span>
<span data-ttu-id="14bb2-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="14bb2-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="14bb2-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="14bb2-118">-Location</span></span>
<span data-ttu-id="14bb2-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="14bb2-119">Location of the resource.</span></span>

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

### <span data-ttu-id="14bb2-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="14bb2-120">-LogicalNetwork</span></span>
<span data-ttu-id="14bb2-121">Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="14bb2-121">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14bb2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="14bb2-122">-Name</span></span>
<span data-ttu-id="14bb2-123">Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="14bb2-123">Name of the logical subnet.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14bb2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14bb2-124">-ResourceGroupName</span></span>
<span data-ttu-id="14bb2-125">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="14bb2-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="14bb2-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="14bb2-126">-ResourceId</span></span>
<span data-ttu-id="14bb2-127">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="14bb2-127">The resource id.</span></span>

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

### <span data-ttu-id="14bb2-128">-Atla</span><span class="sxs-lookup"><span data-stu-id="14bb2-128">-Skip</span></span>
<span data-ttu-id="14bb2-129">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="14bb2-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="14bb2-130">-Üst</span><span class="sxs-lookup"><span data-stu-id="14bb2-130">-Top</span></span>
<span data-ttu-id="14bb2-131">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="14bb2-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="14bb2-132">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="14bb2-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="14bb2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14bb2-133">CommonParameters</span></span>
<span data-ttu-id="14bb2-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14bb2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14bb2-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14bb2-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14bb2-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14bb2-136">INPUTS</span></span>

## <span data-ttu-id="14bb2-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14bb2-137">OUTPUTS</span></span>

### <span data-ttu-id="14bb2-138">Microsoft. AzureStack. Management. Fabric. admin. modeller. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="14bb2-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="14bb2-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14bb2-139">NOTES</span></span>

## <span data-ttu-id="14bb2-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14bb2-140">RELATED LINKS</span></span>

