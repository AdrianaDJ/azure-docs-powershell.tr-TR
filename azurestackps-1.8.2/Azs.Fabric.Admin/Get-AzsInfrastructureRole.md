---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a20f0fbc5b059e878f0062569ffba2c16794204
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106642"
---
# <span data-ttu-id="fc232-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="fc232-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="fc232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc232-102">SYNOPSIS</span></span>
<span data-ttu-id="fc232-103">Bir konumdaki tüm altyapı rollerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc232-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="fc232-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc232-104">SYNTAX</span></span>

### <span data-ttu-id="fc232-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc232-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="fc232-106">Al</span><span class="sxs-lookup"><span data-stu-id="fc232-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc232-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="fc232-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="fc232-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc232-108">DESCRIPTION</span></span>
<span data-ttu-id="fc232-109">Bir konumdaki tüm altyapı rollerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc232-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="fc232-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc232-110">EXAMPLES</span></span>

### <span data-ttu-id="fc232-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="fc232-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="fc232-112">Tüm altyapı rollerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="fc232-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="fc232-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="fc232-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="fc232-114">Ada göre bir altyapı rolü edinin.</span><span class="sxs-lookup"><span data-stu-id="fc232-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="fc232-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc232-115">PARAMETERS</span></span>

### <span data-ttu-id="fc232-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc232-116">-Name</span></span>
<span data-ttu-id="fc232-117">Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="fc232-117">Infrastructure role name.</span></span>

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

### <span data-ttu-id="fc232-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="fc232-118">-Location</span></span>
<span data-ttu-id="fc232-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="fc232-119">Location of the resource.</span></span>

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

### <span data-ttu-id="fc232-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc232-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc232-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fc232-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="fc232-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fc232-122">-ResourceId</span></span>
<span data-ttu-id="fc232-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="fc232-123">The resource id.</span></span>

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

### <span data-ttu-id="fc232-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="fc232-124">-Filter</span></span>
<span data-ttu-id="fc232-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="fc232-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="fc232-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="fc232-126">-Skip</span></span>
<span data-ttu-id="fc232-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="fc232-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="fc232-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="fc232-128">-Top</span></span>
<span data-ttu-id="fc232-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="fc232-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="fc232-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="fc232-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="fc232-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc232-131">CommonParameters</span></span>
<span data-ttu-id="fc232-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc232-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc232-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc232-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc232-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc232-134">INPUTS</span></span>

## <span data-ttu-id="fc232-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc232-135">OUTPUTS</span></span>

### <span data-ttu-id="fc232-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. InfraRole</span><span class="sxs-lookup"><span data-stu-id="fc232-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="fc232-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc232-137">NOTES</span></span>

## <span data-ttu-id="fc232-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc232-138">RELATED LINKS</span></span>
