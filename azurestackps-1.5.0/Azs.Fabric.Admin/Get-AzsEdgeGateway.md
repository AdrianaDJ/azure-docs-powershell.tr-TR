---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a81fcf688e1c269aabd64250e9b0694730edc8f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572197"
---
# <span data-ttu-id="49d75-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="49d75-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="49d75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49d75-102">SYNOPSIS</span></span>
<span data-ttu-id="49d75-103">Belirli bir konumdaki tüm kenar ağ geçitlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="49d75-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="49d75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49d75-104">SYNTAX</span></span>

### <span data-ttu-id="49d75-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="49d75-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="49d75-106">Al</span><span class="sxs-lookup"><span data-stu-id="49d75-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="49d75-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="49d75-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="49d75-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="49d75-108">DESCRIPTION</span></span>
<span data-ttu-id="49d75-109">Belirli bir konumdaki tüm kenar ağ geçitlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="49d75-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="49d75-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49d75-110">EXAMPLES</span></span>

### <span data-ttu-id="49d75-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="49d75-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="49d75-112">Tüm Edge ağ geçitlerinin bir listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="49d75-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="49d75-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="49d75-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="49d75-114">Belirli bir Edge ağ geçidi edinin.</span><span class="sxs-lookup"><span data-stu-id="49d75-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="49d75-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49d75-115">PARAMETERS</span></span>

### <span data-ttu-id="49d75-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="49d75-116">-Filter</span></span>
<span data-ttu-id="49d75-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="49d75-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="49d75-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="49d75-118">-Location</span></span>
<span data-ttu-id="49d75-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="49d75-119">Location of the resource.</span></span>

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

### <span data-ttu-id="49d75-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="49d75-120">-Name</span></span>
<span data-ttu-id="49d75-121">Uç ağ geçidinin adı.</span><span class="sxs-lookup"><span data-stu-id="49d75-121">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="49d75-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49d75-122">-ResourceGroupName</span></span>
<span data-ttu-id="49d75-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="49d75-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="49d75-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="49d75-124">-ResourceId</span></span>
<span data-ttu-id="49d75-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="49d75-125">The resource id.</span></span>

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

### <span data-ttu-id="49d75-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="49d75-126">-Skip</span></span>
<span data-ttu-id="49d75-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="49d75-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="49d75-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="49d75-128">-Top</span></span>
<span data-ttu-id="49d75-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="49d75-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="49d75-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="49d75-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="49d75-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d75-131">CommonParameters</span></span>
<span data-ttu-id="49d75-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49d75-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d75-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49d75-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d75-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49d75-134">INPUTS</span></span>

## <span data-ttu-id="49d75-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49d75-135">OUTPUTS</span></span>

### <span data-ttu-id="49d75-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="49d75-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="49d75-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49d75-137">NOTES</span></span>

## <span data-ttu-id="49d75-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49d75-138">RELATED LINKS</span></span>

