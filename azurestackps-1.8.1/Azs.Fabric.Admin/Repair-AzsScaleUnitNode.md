---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934891"
---
# <span data-ttu-id="15e3a-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="15e3a-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="15e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="15e3a-103">Kümenin bir düğümünü onarır.</span><span class="sxs-lookup"><span data-stu-id="15e3a-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="15e3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15e3a-104">SYNTAX</span></span>

### <span data-ttu-id="15e3a-105">Onar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15e3a-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15e3a-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="15e3a-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15e3a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="15e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="15e3a-108">Kümenin bir düğümünü onarır.</span><span class="sxs-lookup"><span data-stu-id="15e3a-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="15e3a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15e3a-109">EXAMPLES</span></span>

### <span data-ttu-id="15e3a-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="15e3a-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="15e3a-111">Ölçek birimi düğümünü onarın.</span><span class="sxs-lookup"><span data-stu-id="15e3a-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="15e3a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15e3a-112">PARAMETERS</span></span>

### <span data-ttu-id="15e3a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="15e3a-113">-Name</span></span>
<span data-ttu-id="15e3a-114">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="15e3a-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="15e3a-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="15e3a-115">-BMCIPv4Address</span></span>
<span data-ttu-id="15e3a-116">Fiziksel makinenin BMC adresi.</span><span class="sxs-lookup"><span data-stu-id="15e3a-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="15e3a-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="15e3a-117">-Location</span></span>
<span data-ttu-id="15e3a-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="15e3a-118">Location of the resource.</span></span>

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

### <span data-ttu-id="15e3a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15e3a-119">-ResourceGroupName</span></span>
<span data-ttu-id="15e3a-120">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="15e3a-120">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="15e3a-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="15e3a-121">-ResourceId</span></span>
<span data-ttu-id="15e3a-122">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="15e3a-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="15e3a-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="15e3a-123">-AsJob</span></span>
<span data-ttu-id="15e3a-124">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="15e3a-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="15e3a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="15e3a-125">-Force</span></span>
<span data-ttu-id="15e3a-126">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="15e3a-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="15e3a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15e3a-127">-WhatIf</span></span>
<span data-ttu-id="15e3a-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15e3a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15e3a-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15e3a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15e3a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="15e3a-130">-Confirm</span></span>
<span data-ttu-id="15e3a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15e3a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15e3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e3a-132">CommonParameters</span></span>
<span data-ttu-id="15e3a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15e3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e3a-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15e3a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e3a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15e3a-135">INPUTS</span></span>

## <span data-ttu-id="15e3a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15e3a-136">OUTPUTS</span></span>

## <span data-ttu-id="15e3a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15e3a-137">NOTES</span></span>

## <span data-ttu-id="15e3a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15e3a-138">RELATED LINKS</span></span>
