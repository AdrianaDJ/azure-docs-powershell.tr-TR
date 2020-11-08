---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106825"
---
# <span data-ttu-id="65005-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="65005-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="65005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65005-102">SYNOPSIS</span></span>
<span data-ttu-id="65005-103">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="65005-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="65005-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65005-104">SYNTAX</span></span>

### <span data-ttu-id="65005-105">Durdur (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65005-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65005-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="65005-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65005-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="65005-107">DESCRIPTION</span></span>
<span data-ttu-id="65005-108">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="65005-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="65005-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65005-109">EXAMPLES</span></span>

### <span data-ttu-id="65005-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="65005-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="65005-111">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="65005-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="65005-112">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="65005-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="65005-113">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="65005-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="65005-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65005-114">PARAMETERS</span></span>

### <span data-ttu-id="65005-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="65005-115">-Name</span></span>
<span data-ttu-id="65005-116">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="65005-116">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65005-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="65005-117">-Location</span></span>
<span data-ttu-id="65005-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="65005-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65005-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65005-119">-ResourceGroupName</span></span>
<span data-ttu-id="65005-120">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="65005-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65005-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="65005-121">-ResourceId</span></span>
<span data-ttu-id="65005-122">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="65005-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="65005-123">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="65005-123">-Shutdown</span></span>
<span data-ttu-id="65005-124">Ayarla işlevi, ölçek birimi düğümünü dikkatlice kapatır; Aksi takdirde, ölçek birimi düğümünü kapatın.</span><span class="sxs-lookup"><span data-stu-id="65005-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="65005-125">-Iş</span><span class="sxs-lookup"><span data-stu-id="65005-125">-AsJob</span></span>
<span data-ttu-id="65005-126">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="65005-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="65005-127">-Force</span><span class="sxs-lookup"><span data-stu-id="65005-127">-Force</span></span>
<span data-ttu-id="65005-128">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="65005-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="65005-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65005-129">-WhatIf</span></span>
<span data-ttu-id="65005-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65005-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65005-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65005-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65005-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="65005-132">-Confirm</span></span>
<span data-ttu-id="65005-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65005-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65005-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65005-134">CommonParameters</span></span>
<span data-ttu-id="65005-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65005-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65005-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65005-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65005-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65005-137">INPUTS</span></span>

## <span data-ttu-id="65005-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65005-138">OUTPUTS</span></span>

## <span data-ttu-id="65005-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65005-139">NOTES</span></span>

## <span data-ttu-id="65005-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65005-140">RELATED LINKS</span></span>
