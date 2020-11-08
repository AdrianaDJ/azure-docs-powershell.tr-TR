---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934982"
---
# <span data-ttu-id="45626-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="45626-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="45626-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45626-102">SYNOPSIS</span></span>
<span data-ttu-id="45626-103">Tüm doku konumlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="45626-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="45626-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45626-104">SYNTAX</span></span>

### <span data-ttu-id="45626-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="45626-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="45626-106">Al</span><span class="sxs-lookup"><span data-stu-id="45626-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="45626-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="45626-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="45626-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="45626-108">DESCRIPTION</span></span>
<span data-ttu-id="45626-109">Tüm doku konumlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="45626-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="45626-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45626-110">EXAMPLES</span></span>

### <span data-ttu-id="45626-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="45626-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="45626-112">Tüm doku konumlarının listesini döndürme.</span><span class="sxs-lookup"><span data-stu-id="45626-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="45626-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="45626-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="45626-114">Ada göre bir konum döndürün.</span><span class="sxs-lookup"><span data-stu-id="45626-114">Return a location based on the name.</span></span>

## <span data-ttu-id="45626-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45626-115">PARAMETERS</span></span>

### <span data-ttu-id="45626-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="45626-116">-Location</span></span>
<span data-ttu-id="45626-117">Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="45626-117">Fabric location.</span></span>

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

### <span data-ttu-id="45626-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45626-118">-ResourceGroupName</span></span>
<span data-ttu-id="45626-119">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="45626-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="45626-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="45626-120">-ResourceId</span></span>
<span data-ttu-id="45626-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="45626-121">The resource id.</span></span>

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

### <span data-ttu-id="45626-122">-Filtre</span><span class="sxs-lookup"><span data-stu-id="45626-122">-Filter</span></span>
<span data-ttu-id="45626-123">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="45626-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="45626-124">-Atla</span><span class="sxs-lookup"><span data-stu-id="45626-124">-Skip</span></span>
<span data-ttu-id="45626-125">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="45626-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="45626-126">-Üst</span><span class="sxs-lookup"><span data-stu-id="45626-126">-Top</span></span>
<span data-ttu-id="45626-127">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="45626-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="45626-128">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="45626-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="45626-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45626-129">CommonParameters</span></span>
<span data-ttu-id="45626-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45626-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45626-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45626-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45626-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45626-132">INPUTS</span></span>

## <span data-ttu-id="45626-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45626-133">OUTPUTS</span></span>

### <span data-ttu-id="45626-134">Microsoft. AzureStack. Management. Fabric. admin. modeller. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="45626-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="45626-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45626-135">NOTES</span></span>

## <span data-ttu-id="45626-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45626-136">RELATED LINKS</span></span>