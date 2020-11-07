---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dac95eced72f70d3471019136d302fcdfe95f86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934481"
---
# <span data-ttu-id="8db4a-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="8db4a-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="8db4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8db4a-102">SYNOPSIS</span></span>
<span data-ttu-id="8db4a-103">Bir konumdaki tüm altyapı rollerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8db4a-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="8db4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8db4a-104">SYNTAX</span></span>

### <span data-ttu-id="8db4a-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8db4a-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8db4a-106">Al</span><span class="sxs-lookup"><span data-stu-id="8db4a-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8db4a-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="8db4a-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8db4a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8db4a-108">DESCRIPTION</span></span>
<span data-ttu-id="8db4a-109">Bir konumdaki tüm altyapı rollerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8db4a-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="8db4a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8db4a-110">EXAMPLES</span></span>

### <span data-ttu-id="8db4a-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8db4a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="8db4a-112">Tüm altyapı rollerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="8db4a-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="8db4a-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8db4a-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="8db4a-114">Ada göre bir altyapı rolü edinin.</span><span class="sxs-lookup"><span data-stu-id="8db4a-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="8db4a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8db4a-115">PARAMETERS</span></span>

### <span data-ttu-id="8db4a-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="8db4a-116">-Filter</span></span>
<span data-ttu-id="8db4a-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="8db4a-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="8db4a-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="8db4a-118">-Location</span></span>
<span data-ttu-id="8db4a-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="8db4a-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8db4a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="8db4a-120">-Name</span></span>
<span data-ttu-id="8db4a-121">Altyapı rolü adı.</span><span class="sxs-lookup"><span data-stu-id="8db4a-121">Infrastructure role name.</span></span>

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

### <span data-ttu-id="8db4a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8db4a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8db4a-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8db4a-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8db4a-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8db4a-124">-ResourceId</span></span>
<span data-ttu-id="8db4a-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8db4a-125">The resource id.</span></span>

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

### <span data-ttu-id="8db4a-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="8db4a-126">-Skip</span></span>
<span data-ttu-id="8db4a-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="8db4a-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8db4a-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="8db4a-128">-Top</span></span>
<span data-ttu-id="8db4a-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="8db4a-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8db4a-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="8db4a-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8db4a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db4a-131">CommonParameters</span></span>
<span data-ttu-id="8db4a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8db4a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db4a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8db4a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db4a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8db4a-134">INPUTS</span></span>

## <span data-ttu-id="8db4a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8db4a-135">OUTPUTS</span></span>

### <span data-ttu-id="8db4a-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. InfraRole</span><span class="sxs-lookup"><span data-stu-id="8db4a-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="8db4a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8db4a-137">NOTES</span></span>

## <span data-ttu-id="8db4a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8db4a-138">RELATED LINKS</span></span>

