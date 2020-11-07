---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88d9fc8456c86f0806313bb0234e145b7f4d727a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934628"
---
# <span data-ttu-id="38f20-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="38f20-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="38f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38f20-102">SYNOPSIS</span></span>
<span data-ttu-id="38f20-103">Bir konumdaki tüm mantıksal ağların bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="38f20-103">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="38f20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38f20-104">SYNTAX</span></span>

### <span data-ttu-id="38f20-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38f20-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="38f20-106">Al</span><span class="sxs-lookup"><span data-stu-id="38f20-106">Get</span></span>
```
Get-AzsLogicalNetwork [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="38f20-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="38f20-107">ResourceId</span></span>
```
Get-AzsLogicalNetwork -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="38f20-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="38f20-108">DESCRIPTION</span></span>
<span data-ttu-id="38f20-109">Bir konumdaki tüm mantıksal ağların bir listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="38f20-109">Returns a list of all logical networks at a location.</span></span>

## <span data-ttu-id="38f20-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38f20-110">EXAMPLES</span></span>

### <span data-ttu-id="38f20-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="38f20-111">EXAMPLE 1</span></span>
```
Get-AzsLogicalNetwork
```

<span data-ttu-id="38f20-112">Tüm mantıksal ağları bir yerde alın.</span><span class="sxs-lookup"><span data-stu-id="38f20-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="38f20-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="38f20-113">EXAMPLE 2</span></span>
```
Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"
```

<span data-ttu-id="38f20-114">Bir ad temelinde belirli bir yerde belirli bir mantıksal ağ edinin.</span><span class="sxs-lookup"><span data-stu-id="38f20-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="38f20-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38f20-115">PARAMETERS</span></span>

### <span data-ttu-id="38f20-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="38f20-116">-Name</span></span>
<span data-ttu-id="38f20-117">Mantıksal ağın adı.</span><span class="sxs-lookup"><span data-stu-id="38f20-117">Name of the logical network.</span></span>

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

### <span data-ttu-id="38f20-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="38f20-118">-Location</span></span>
<span data-ttu-id="38f20-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="38f20-119">Location of the resource.</span></span>

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

### <span data-ttu-id="38f20-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f20-120">-ResourceGroupName</span></span>
<span data-ttu-id="38f20-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="38f20-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="38f20-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="38f20-122">-ResourceId</span></span>
<span data-ttu-id="38f20-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="38f20-123">The resource id.</span></span>

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

### <span data-ttu-id="38f20-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="38f20-124">-Filter</span></span>
<span data-ttu-id="38f20-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="38f20-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="38f20-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="38f20-126">-Skip</span></span>
<span data-ttu-id="38f20-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="38f20-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="38f20-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="38f20-128">-Top</span></span>
<span data-ttu-id="38f20-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="38f20-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="38f20-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="38f20-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="38f20-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f20-131">CommonParameters</span></span>
<span data-ttu-id="38f20-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38f20-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f20-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f20-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f20-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38f20-134">INPUTS</span></span>

## <span data-ttu-id="38f20-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38f20-135">OUTPUTS</span></span>

### <span data-ttu-id="38f20-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="38f20-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalNetwork</span></span>

## <span data-ttu-id="38f20-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38f20-137">NOTES</span></span>

## <span data-ttu-id="38f20-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38f20-138">RELATED LINKS</span></span>
