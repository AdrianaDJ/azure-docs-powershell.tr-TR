---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcd5d112fea0ec68e372a5ad282b3d661f9481ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761684"
---
# <span data-ttu-id="398a8-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="398a8-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="398a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="398a8-102">SYNOPSIS</span></span>
<span data-ttu-id="398a8-103">Tüm doku konumlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="398a8-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="398a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="398a8-104">SYNTAX</span></span>

### <span data-ttu-id="398a8-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="398a8-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="398a8-106">Al</span><span class="sxs-lookup"><span data-stu-id="398a8-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="398a8-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="398a8-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="398a8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="398a8-108">DESCRIPTION</span></span>
<span data-ttu-id="398a8-109">Tüm doku konumlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="398a8-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="398a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="398a8-110">EXAMPLES</span></span>

### <span data-ttu-id="398a8-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="398a8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="398a8-112">Tüm doku konumlarının listesini döndürme.</span><span class="sxs-lookup"><span data-stu-id="398a8-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="398a8-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="398a8-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="398a8-114">Ada göre bir konum döndürün.</span><span class="sxs-lookup"><span data-stu-id="398a8-114">Return a location based on the name.</span></span>

## <span data-ttu-id="398a8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="398a8-115">PARAMETERS</span></span>

### <span data-ttu-id="398a8-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="398a8-116">-Filter</span></span>
<span data-ttu-id="398a8-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="398a8-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="398a8-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="398a8-118">-Location</span></span>
<span data-ttu-id="398a8-119">Doku konumu.</span><span class="sxs-lookup"><span data-stu-id="398a8-119">Fabric location.</span></span>

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

### <span data-ttu-id="398a8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="398a8-120">-ResourceGroupName</span></span>
<span data-ttu-id="398a8-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="398a8-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="398a8-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="398a8-122">-ResourceId</span></span>
<span data-ttu-id="398a8-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="398a8-123">The resource id.</span></span>

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

### <span data-ttu-id="398a8-124">-Atla</span><span class="sxs-lookup"><span data-stu-id="398a8-124">-Skip</span></span>
<span data-ttu-id="398a8-125">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="398a8-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="398a8-126">-Üst</span><span class="sxs-lookup"><span data-stu-id="398a8-126">-Top</span></span>
<span data-ttu-id="398a8-127">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="398a8-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="398a8-128">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="398a8-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="398a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="398a8-129">CommonParameters</span></span>
<span data-ttu-id="398a8-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="398a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="398a8-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="398a8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="398a8-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="398a8-132">INPUTS</span></span>

## <span data-ttu-id="398a8-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="398a8-133">OUTPUTS</span></span>

### <span data-ttu-id="398a8-134">Microsoft. AzureStack. Management. Fabric. admin. modeller. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="398a8-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="398a8-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="398a8-135">NOTES</span></span>

## <span data-ttu-id="398a8-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="398a8-136">RELATED LINKS</span></span>

