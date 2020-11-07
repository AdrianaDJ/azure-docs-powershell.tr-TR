---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934647"
---
# <span data-ttu-id="4c294-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="4c294-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="4c294-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c294-102">SYNOPSIS</span></span>
<span data-ttu-id="4c294-103">Ölçeklendirme birimi düğümü için bakım modunu durdurun.</span><span class="sxs-lookup"><span data-stu-id="4c294-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="4c294-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c294-104">SYNTAX</span></span>

### <span data-ttu-id="4c294-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c294-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c294-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="4c294-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c294-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c294-107">DESCRIPTION</span></span>
<span data-ttu-id="4c294-108">Ölçeklendirme birimi düğümü için bakım modunu durdurun.</span><span class="sxs-lookup"><span data-stu-id="4c294-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="4c294-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c294-109">EXAMPLES</span></span>

### <span data-ttu-id="4c294-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="4c294-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="4c294-111">Ölçeklendirme birimi düğümündeki bakım modunu durdurma.</span><span class="sxs-lookup"><span data-stu-id="4c294-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="4c294-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c294-112">PARAMETERS</span></span>

### <span data-ttu-id="4c294-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c294-113">-Name</span></span>
<span data-ttu-id="4c294-114">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="4c294-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c294-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="4c294-115">-Location</span></span>
<span data-ttu-id="4c294-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="4c294-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c294-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c294-117">-ResourceGroupName</span></span>
<span data-ttu-id="4c294-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="4c294-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c294-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4c294-119">-ResourceId</span></span>
<span data-ttu-id="4c294-120">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4c294-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="4c294-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="4c294-121">-AsJob</span></span>
<span data-ttu-id="4c294-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="4c294-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4c294-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4c294-123">-Force</span></span>
<span data-ttu-id="4c294-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="4c294-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4c294-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c294-125">-WhatIf</span></span>
<span data-ttu-id="4c294-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c294-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c294-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c294-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c294-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c294-128">-Confirm</span></span>
<span data-ttu-id="4c294-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c294-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c294-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c294-130">CommonParameters</span></span>
<span data-ttu-id="4c294-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c294-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c294-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c294-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c294-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c294-133">INPUTS</span></span>

## <span data-ttu-id="4c294-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c294-134">OUTPUTS</span></span>

## <span data-ttu-id="4c294-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c294-135">NOTES</span></span>

## <span data-ttu-id="4c294-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c294-136">RELATED LINKS</span></span>
