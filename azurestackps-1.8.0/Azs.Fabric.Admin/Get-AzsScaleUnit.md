---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934624"
---
# <span data-ttu-id="bb976-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="bb976-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="bb976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb976-102">SYNOPSIS</span></span>
<span data-ttu-id="bb976-103">Bir konumdaki tüm ölçek birimlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb976-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="bb976-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb976-104">SYNTAX</span></span>

### <span data-ttu-id="bb976-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb976-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bb976-106">Al</span><span class="sxs-lookup"><span data-stu-id="bb976-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="bb976-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="bb976-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bb976-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb976-108">DESCRIPTION</span></span>
<span data-ttu-id="bb976-109">Bir konumdaki tüm ölçek birimlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="bb976-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="bb976-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb976-110">EXAMPLES</span></span>

### <span data-ttu-id="bb976-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="bb976-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="bb976-112">Ölçek birimleri hakkında bilgi listesi döndürme.</span><span class="sxs-lookup"><span data-stu-id="bb976-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="bb976-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="bb976-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="bb976-114">Belirli bir ölçek birimi hakkında bilgi döndürme.</span><span class="sxs-lookup"><span data-stu-id="bb976-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="bb976-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb976-115">PARAMETERS</span></span>

### <span data-ttu-id="bb976-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb976-116">-Name</span></span>
<span data-ttu-id="bb976-117">Ölçek birimlerinin adı.</span><span class="sxs-lookup"><span data-stu-id="bb976-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="bb976-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="bb976-118">-Location</span></span>
<span data-ttu-id="bb976-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="bb976-119">Location of the resource.</span></span>

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

### <span data-ttu-id="bb976-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb976-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb976-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bb976-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="bb976-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bb976-122">-ResourceId</span></span>
<span data-ttu-id="bb976-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="bb976-123">The resource id.</span></span>

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

### <span data-ttu-id="bb976-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="bb976-124">-Filter</span></span>
<span data-ttu-id="bb976-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="bb976-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="bb976-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="bb976-126">-Skip</span></span>
<span data-ttu-id="bb976-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="bb976-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="bb976-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="bb976-128">-Top</span></span>
<span data-ttu-id="bb976-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="bb976-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bb976-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="bb976-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="bb976-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb976-131">CommonParameters</span></span>
<span data-ttu-id="bb976-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb976-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb976-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb976-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb976-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb976-134">INPUTS</span></span>

## <span data-ttu-id="bb976-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb976-135">OUTPUTS</span></span>

### <span data-ttu-id="bb976-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="bb976-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="bb976-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb976-137">NOTES</span></span>

## <span data-ttu-id="bb976-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb976-138">RELATED LINKS</span></span>
