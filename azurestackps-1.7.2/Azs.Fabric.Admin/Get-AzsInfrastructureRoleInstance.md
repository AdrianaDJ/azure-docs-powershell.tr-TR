---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39955a2b99ffd7e3c604b4fc288f117face8205f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934480"
---
# <span data-ttu-id="95758-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="95758-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="95758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95758-102">SYNOPSIS</span></span>
<span data-ttu-id="95758-103">Bir konumdaki tüm altyapı rolü örneklerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="95758-103">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="95758-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95758-104">SYNTAX</span></span>

### <span data-ttu-id="95758-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="95758-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="95758-106">Al</span><span class="sxs-lookup"><span data-stu-id="95758-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="95758-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="95758-107">ResourceId</span></span>
```
Get-AzsInfrastructureRoleInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="95758-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="95758-108">DESCRIPTION</span></span>
<span data-ttu-id="95758-109">Bir konumdaki tüm altyapı rolü örneklerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="95758-109">Returns a list of all infrastructure role instances at a location.</span></span>

## <span data-ttu-id="95758-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95758-110">EXAMPLES</span></span>

### <span data-ttu-id="95758-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="95758-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance
```

<span data-ttu-id="95758-112">Tüm altyapı rolü örneklerinin listesini döndürme.</span><span class="sxs-lookup"><span data-stu-id="95758-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="95758-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="95758-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="95758-114">Ada dayalı olarak tek bir altyapı rol örneği döndürün.</span><span class="sxs-lookup"><span data-stu-id="95758-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="95758-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95758-115">PARAMETERS</span></span>

### <span data-ttu-id="95758-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="95758-116">-Filter</span></span>
<span data-ttu-id="95758-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="95758-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="95758-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="95758-118">-Location</span></span>
<span data-ttu-id="95758-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="95758-119">Location of the resource.</span></span>

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

### <span data-ttu-id="95758-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="95758-120">-Name</span></span>
<span data-ttu-id="95758-121">Altyapı rolü örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="95758-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="95758-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95758-122">-ResourceGroupName</span></span>
<span data-ttu-id="95758-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="95758-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="95758-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="95758-124">-ResourceId</span></span>
<span data-ttu-id="95758-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="95758-125">The resource id.</span></span>

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

### <span data-ttu-id="95758-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="95758-126">-Skip</span></span>
<span data-ttu-id="95758-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="95758-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="95758-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="95758-128">-Top</span></span>
<span data-ttu-id="95758-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="95758-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="95758-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="95758-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="95758-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95758-131">CommonParameters</span></span>
<span data-ttu-id="95758-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95758-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95758-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95758-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95758-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95758-134">INPUTS</span></span>

## <span data-ttu-id="95758-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95758-135">OUTPUTS</span></span>

### <span data-ttu-id="95758-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. InfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="95758-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRoleInstance</span></span>

## <span data-ttu-id="95758-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95758-137">NOTES</span></span>

## <span data-ttu-id="95758-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95758-138">RELATED LINKS</span></span>

