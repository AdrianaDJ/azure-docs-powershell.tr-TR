---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 869cd48507ba9384026f8e58b9cd7853179b844f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761698"
---
# <span data-ttu-id="224fb-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="224fb-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="224fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="224fb-102">SYNOPSIS</span></span>
<span data-ttu-id="224fb-103">Bir konumdaki tüm ölçek birimlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="224fb-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="224fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="224fb-104">SYNTAX</span></span>

### <span data-ttu-id="224fb-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="224fb-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="224fb-106">Al</span><span class="sxs-lookup"><span data-stu-id="224fb-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="224fb-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="224fb-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="224fb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="224fb-108">DESCRIPTION</span></span>
<span data-ttu-id="224fb-109">Bir konumdaki tüm ölçek birimlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="224fb-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="224fb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="224fb-110">EXAMPLES</span></span>

### <span data-ttu-id="224fb-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="224fb-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="224fb-112">Ölçek birimleri hakkında bilgi listesi döndürme.</span><span class="sxs-lookup"><span data-stu-id="224fb-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="224fb-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="224fb-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="224fb-114">Belirli bir ölçek birimi hakkında bilgi döndürme.</span><span class="sxs-lookup"><span data-stu-id="224fb-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="224fb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="224fb-115">PARAMETERS</span></span>

### <span data-ttu-id="224fb-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="224fb-116">-Filter</span></span>
<span data-ttu-id="224fb-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="224fb-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="224fb-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="224fb-118">-Location</span></span>
<span data-ttu-id="224fb-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="224fb-119">Location of the resource.</span></span>

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

### <span data-ttu-id="224fb-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="224fb-120">-Name</span></span>
<span data-ttu-id="224fb-121">Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="224fb-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="224fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="224fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="224fb-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="224fb-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="224fb-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="224fb-124">-ResourceId</span></span>
<span data-ttu-id="224fb-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="224fb-125">The resource id.</span></span>

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

### <span data-ttu-id="224fb-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="224fb-126">-Skip</span></span>
<span data-ttu-id="224fb-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="224fb-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="224fb-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="224fb-128">-Top</span></span>
<span data-ttu-id="224fb-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="224fb-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="224fb-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="224fb-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="224fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224fb-131">CommonParameters</span></span>
<span data-ttu-id="224fb-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="224fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224fb-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="224fb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224fb-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="224fb-134">INPUTS</span></span>

## <span data-ttu-id="224fb-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="224fb-135">OUTPUTS</span></span>

### <span data-ttu-id="224fb-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="224fb-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="224fb-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="224fb-137">NOTES</span></span>

## <span data-ttu-id="224fb-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="224fb-138">RELATED LINKS</span></span>

