---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 793bf4a4b5b9dfb448c5b2a1baf9d74af592a23e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106647"
---
# <span data-ttu-id="5d6fe-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="5d6fe-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="5d6fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d6fe-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6fe-103">Belirli bir konumdaki tüm kenar ağ geçitlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="5d6fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d6fe-104">SYNTAX</span></span>

### <span data-ttu-id="5d6fe-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d6fe-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5d6fe-106">Al</span><span class="sxs-lookup"><span data-stu-id="5d6fe-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="5d6fe-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="5d6fe-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5d6fe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d6fe-108">DESCRIPTION</span></span>
<span data-ttu-id="5d6fe-109">Belirli bir konumdaki tüm kenar ağ geçitlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="5d6fe-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d6fe-110">EXAMPLES</span></span>

### <span data-ttu-id="5d6fe-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="5d6fe-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="5d6fe-112">Tüm Edge ağ geçitlerinin bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="5d6fe-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="5d6fe-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="5d6fe-114">Belirli bir Edge ağ geçidi edinin.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="5d6fe-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d6fe-115">PARAMETERS</span></span>

### <span data-ttu-id="5d6fe-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="5d6fe-116">-Name</span></span>
<span data-ttu-id="5d6fe-117">Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-117">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="5d6fe-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="5d6fe-118">-Location</span></span>
<span data-ttu-id="5d6fe-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-119">Location of the resource.</span></span>

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

### <span data-ttu-id="5d6fe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d6fe-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d6fe-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="5d6fe-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5d6fe-122">-ResourceId</span></span>
<span data-ttu-id="5d6fe-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-123">The resource id.</span></span>

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

### <span data-ttu-id="5d6fe-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="5d6fe-124">-Filter</span></span>
<span data-ttu-id="5d6fe-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="5d6fe-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="5d6fe-126">-Skip</span></span>
<span data-ttu-id="5d6fe-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="5d6fe-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="5d6fe-128">-Top</span></span>
<span data-ttu-id="5d6fe-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5d6fe-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="5d6fe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6fe-131">CommonParameters</span></span>
<span data-ttu-id="5d6fe-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d6fe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6fe-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d6fe-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6fe-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d6fe-134">INPUTS</span></span>

## <span data-ttu-id="5d6fe-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d6fe-135">OUTPUTS</span></span>

### <span data-ttu-id="5d6fe-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="5d6fe-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="5d6fe-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d6fe-137">NOTES</span></span>

## <span data-ttu-id="5d6fe-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d6fe-138">RELATED LINKS</span></span>
