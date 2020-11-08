---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb535146787c4c33a57ad406f05544f18ba74eb0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106858"
---
# <span data-ttu-id="c3968-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="c3968-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="c3968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3968-102">SYNOPSIS</span></span>
<span data-ttu-id="c3968-103">Tüm mantıksal alt ağların bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c3968-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="c3968-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3968-104">SYNTAX</span></span>

### <span data-ttu-id="c3968-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3968-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c3968-106">Al</span><span class="sxs-lookup"><span data-stu-id="c3968-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3968-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="c3968-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c3968-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3968-108">DESCRIPTION</span></span>
<span data-ttu-id="c3968-109">Tüm mantıksal alt ağların bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c3968-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="c3968-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3968-110">EXAMPLES</span></span>

### <span data-ttu-id="c3968-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="c3968-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="c3968-112">Belirli bir mantıksal ağ ve konum için tüm mantıksal alt ağların bir listesini alın.</span><span class="sxs-lookup"><span data-stu-id="c3968-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="c3968-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="c3968-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="c3968-114">Belirli bir mantıksal ağ için belirli bir mantıksal ağ ve ada göre bir konum edinin.</span><span class="sxs-lookup"><span data-stu-id="c3968-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="c3968-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3968-115">PARAMETERS</span></span>

### <span data-ttu-id="c3968-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3968-116">-Name</span></span>
<span data-ttu-id="c3968-117">Mantıksal alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="c3968-117">Name of the logical subnet.</span></span>

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

### <span data-ttu-id="c3968-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="c3968-118">-LogicalNetwork</span></span>
<span data-ttu-id="c3968-119">Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="c3968-119">Name of the logical network.</span></span>

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

### <span data-ttu-id="c3968-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="c3968-120">-Location</span></span>
<span data-ttu-id="c3968-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="c3968-121">Location of the resource.</span></span>

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

### <span data-ttu-id="c3968-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3968-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3968-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="c3968-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c3968-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c3968-124">-ResourceId</span></span>
<span data-ttu-id="c3968-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c3968-125">The resource id.</span></span>

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

### <span data-ttu-id="c3968-126">-Filtre</span><span class="sxs-lookup"><span data-stu-id="c3968-126">-Filter</span></span>
<span data-ttu-id="c3968-127">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="c3968-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="c3968-128">-Atla</span><span class="sxs-lookup"><span data-stu-id="c3968-128">-Skip</span></span>
<span data-ttu-id="c3968-129">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="c3968-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c3968-130">-Üst</span><span class="sxs-lookup"><span data-stu-id="c3968-130">-Top</span></span>
<span data-ttu-id="c3968-131">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="c3968-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c3968-132">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c3968-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c3968-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3968-133">CommonParameters</span></span>
<span data-ttu-id="c3968-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3968-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3968-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3968-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3968-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3968-136">INPUTS</span></span>

## <span data-ttu-id="c3968-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3968-137">OUTPUTS</span></span>

### <span data-ttu-id="c3968-138">Microsoft. AzureStack. Management. Fabric. admin. modeller. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="c3968-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="c3968-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3968-139">NOTES</span></span>

## <span data-ttu-id="c3968-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3968-140">RELATED LINKS</span></span>
