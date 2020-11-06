---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67a49abc82ba1ec8d9411141d456b8f71f75600f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571294"
---
# <span data-ttu-id="e9c3d-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="e9c3d-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="e9c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c3d-103">Bir konumdaki ağ geçidi havuzu nesnelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="e9c3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9c3d-104">SYNTAX</span></span>

### <span data-ttu-id="e9c3d-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e9c3d-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e9c3d-106">Al</span><span class="sxs-lookup"><span data-stu-id="e9c3d-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="e9c3d-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="e9c3d-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e9c3d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9c3d-108">DESCRIPTION</span></span>
<span data-ttu-id="e9c3d-109">Bir konumda Edge ağ geçidi havuzu nesnelerini getirir.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="e9c3d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9c3d-110">EXAMPLES</span></span>

### <span data-ttu-id="e9c3d-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e9c3d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="e9c3d-112">Tüm Edge ağ geçidi havuzlarının bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="e9c3d-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e9c3d-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="e9c3d-114">Belirli bir Edge ağ geçidi havuzu edinin.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="e9c3d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9c3d-115">PARAMETERS</span></span>

### <span data-ttu-id="e9c3d-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="e9c3d-116">-Filter</span></span>
<span data-ttu-id="e9c3d-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e9c3d-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="e9c3d-118">-Location</span></span>
<span data-ttu-id="e9c3d-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e9c3d-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9c3d-120">-Name</span></span>
<span data-ttu-id="e9c3d-121">Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-121">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="e9c3d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c3d-122">-ResourceGroupName</span></span>
<span data-ttu-id="e9c3d-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e9c3d-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e9c3d-124">-ResourceId</span></span>
<span data-ttu-id="e9c3d-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-125">The resource id.</span></span>

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

### <span data-ttu-id="e9c3d-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="e9c3d-126">-Skip</span></span>
<span data-ttu-id="e9c3d-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e9c3d-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="e9c3d-128">-Top</span></span>
<span data-ttu-id="e9c3d-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e9c3d-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e9c3d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c3d-131">CommonParameters</span></span>
<span data-ttu-id="e9c3d-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9c3d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c3d-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c3d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c3d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9c3d-134">INPUTS</span></span>

## <span data-ttu-id="e9c3d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9c3d-135">OUTPUTS</span></span>

### <span data-ttu-id="e9c3d-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="e9c3d-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="e9c3d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9c3d-137">NOTES</span></span>

## <span data-ttu-id="e9c3d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9c3d-138">RELATED LINKS</span></span>

