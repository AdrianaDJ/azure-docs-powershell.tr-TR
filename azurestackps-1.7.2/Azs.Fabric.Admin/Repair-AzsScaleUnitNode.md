---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ad784757210273cd2e456069c8d3a759e973a0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934103"
---
# <span data-ttu-id="bb2aa-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="bb2aa-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="bb2aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2aa-103">Kümenin bir düğümünü onarır.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="bb2aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb2aa-104">SYNTAX</span></span>

### <span data-ttu-id="bb2aa-105">Onar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bb2aa-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb2aa-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="bb2aa-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb2aa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb2aa-107">DESCRIPTION</span></span>
<span data-ttu-id="bb2aa-108">Kümenin bir düğümünü onarır.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="bb2aa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb2aa-109">EXAMPLES</span></span>

### <span data-ttu-id="bb2aa-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bb2aa-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="bb2aa-111">Ölçek birimi düğümünü onarın.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="bb2aa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb2aa-112">PARAMETERS</span></span>

### <span data-ttu-id="bb2aa-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="bb2aa-113">-AsJob</span></span>
<span data-ttu-id="bb2aa-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2aa-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="bb2aa-115">-BMCIPv4Address</span></span>
<span data-ttu-id="bb2aa-116">Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2aa-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bb2aa-117">-Force</span></span>
<span data-ttu-id="bb2aa-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-118">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2aa-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="bb2aa-119">-Location</span></span>
<span data-ttu-id="bb2aa-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2aa-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb2aa-121">-Name</span></span>
<span data-ttu-id="bb2aa-122">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-122">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb2aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb2aa-124">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-124">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2aa-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bb2aa-125">-ResourceId</span></span>
<span data-ttu-id="bb2aa-126">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="bb2aa-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="bb2aa-127">-Confirm</span></span>
<span data-ttu-id="bb2aa-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2aa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb2aa-129">-WhatIf</span></span>
<span data-ttu-id="bb2aa-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb2aa-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2aa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2aa-132">CommonParameters</span></span>
<span data-ttu-id="bb2aa-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2aa-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb2aa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2aa-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb2aa-135">INPUTS</span></span>

## <span data-ttu-id="bb2aa-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb2aa-136">OUTPUTS</span></span>

## <span data-ttu-id="bb2aa-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb2aa-137">NOTES</span></span>

## <span data-ttu-id="bb2aa-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb2aa-138">RELATED LINKS</span></span>
