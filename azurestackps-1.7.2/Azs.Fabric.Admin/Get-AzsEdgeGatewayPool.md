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
ms.locfileid: "93751104"
---
# <span data-ttu-id="befa8-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="befa8-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="befa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="befa8-102">SYNOPSIS</span></span>
<span data-ttu-id="befa8-103">Bir konumdaki ağ geçidi havuzu nesnelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="befa8-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="befa8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="befa8-104">SYNTAX</span></span>

### <span data-ttu-id="befa8-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="befa8-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="befa8-106">Al</span><span class="sxs-lookup"><span data-stu-id="befa8-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="befa8-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="befa8-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="befa8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="befa8-108">DESCRIPTION</span></span>
<span data-ttu-id="befa8-109">Bir konumda Edge ağ geçidi havuzu nesnelerini getirir.</span><span class="sxs-lookup"><span data-stu-id="befa8-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="befa8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="befa8-110">EXAMPLES</span></span>

### <span data-ttu-id="befa8-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="befa8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="befa8-112">Tüm Edge ağ geçidi havuzlarının bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="befa8-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="befa8-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="befa8-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="befa8-114">Belirli bir Edge ağ geçidi havuzu edinin.</span><span class="sxs-lookup"><span data-stu-id="befa8-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="befa8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="befa8-115">PARAMETERS</span></span>

### <span data-ttu-id="befa8-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="befa8-116">-Filter</span></span>
<span data-ttu-id="befa8-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="befa8-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="befa8-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="befa8-118">-Location</span></span>
<span data-ttu-id="befa8-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="befa8-119">Location of the resource.</span></span>

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

### <span data-ttu-id="befa8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="befa8-120">-Name</span></span>
<span data-ttu-id="befa8-121">Edge ağ geçidi havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="befa8-121">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="befa8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="befa8-122">-ResourceGroupName</span></span>
<span data-ttu-id="befa8-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="befa8-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="befa8-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="befa8-124">-ResourceId</span></span>
<span data-ttu-id="befa8-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="befa8-125">The resource id.</span></span>

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

### <span data-ttu-id="befa8-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="befa8-126">-Skip</span></span>
<span data-ttu-id="befa8-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="befa8-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="befa8-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="befa8-128">-Top</span></span>
<span data-ttu-id="befa8-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="befa8-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="befa8-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="befa8-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="befa8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="befa8-131">CommonParameters</span></span>
<span data-ttu-id="befa8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="befa8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="befa8-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="befa8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="befa8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="befa8-134">INPUTS</span></span>

## <span data-ttu-id="befa8-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="befa8-135">OUTPUTS</span></span>

### <span data-ttu-id="befa8-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="befa8-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="befa8-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="befa8-137">NOTES</span></span>

## <span data-ttu-id="befa8-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="befa8-138">RELATED LINKS</span></span>

