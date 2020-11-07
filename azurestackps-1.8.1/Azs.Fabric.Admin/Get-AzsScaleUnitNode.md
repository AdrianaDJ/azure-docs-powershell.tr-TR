---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 07cb5e675003eccc9fad54e723e80a0ddb73ff9a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935126"
---
# <span data-ttu-id="34ced-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="34ced-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="34ced-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34ced-102">SYNOPSIS</span></span>
<span data-ttu-id="34ced-103">Bir konumdaki tüm ölçek birimi düğümlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="34ced-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="34ced-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34ced-104">SYNTAX</span></span>

### <span data-ttu-id="34ced-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34ced-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="34ced-106">Al</span><span class="sxs-lookup"><span data-stu-id="34ced-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="34ced-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="34ced-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="34ced-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34ced-108">DESCRIPTION</span></span>
<span data-ttu-id="34ced-109">Bir konumdaki tüm ölçek birimi düğümlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="34ced-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="34ced-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34ced-110">EXAMPLES</span></span>

### <span data-ttu-id="34ced-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="34ced-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="34ced-112">Bir konumdaki tüm ölçek birim düğümlerini alın.</span><span class="sxs-lookup"><span data-stu-id="34ced-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="34ced-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="34ced-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="34ced-114">Bir ad verilen konumda belirli bir ölçek birimi düğümünü edinin.</span><span class="sxs-lookup"><span data-stu-id="34ced-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="34ced-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34ced-115">PARAMETERS</span></span>

### <span data-ttu-id="34ced-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="34ced-116">-Name</span></span>
<span data-ttu-id="34ced-117">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="34ced-117">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="34ced-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="34ced-118">-Location</span></span>
<span data-ttu-id="34ced-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="34ced-119">Location of the resource.</span></span>

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

### <span data-ttu-id="34ced-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ced-120">-ResourceGroupName</span></span>
<span data-ttu-id="34ced-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="34ced-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="34ced-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="34ced-122">-ResourceId</span></span>
<span data-ttu-id="34ced-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="34ced-123">The resource id.</span></span>

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

### <span data-ttu-id="34ced-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="34ced-124">-Filter</span></span>
<span data-ttu-id="34ced-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="34ced-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="34ced-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="34ced-126">-Skip</span></span>
<span data-ttu-id="34ced-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="34ced-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="34ced-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="34ced-128">-Top</span></span>
<span data-ttu-id="34ced-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="34ced-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="34ced-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="34ced-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="34ced-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ced-131">CommonParameters</span></span>
<span data-ttu-id="34ced-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34ced-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ced-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ced-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ced-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34ced-134">INPUTS</span></span>

## <span data-ttu-id="34ced-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34ced-135">OUTPUTS</span></span>

### <span data-ttu-id="34ced-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="34ced-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="34ced-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34ced-137">NOTES</span></span>

## <span data-ttu-id="34ced-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34ced-138">RELATED LINKS</span></span>
