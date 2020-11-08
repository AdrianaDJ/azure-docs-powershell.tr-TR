---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106650"
---
# <span data-ttu-id="396af-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="396af-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="396af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="396af-102">SYNOPSIS</span></span>
<span data-ttu-id="396af-103">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="396af-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="396af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="396af-104">SYNTAX</span></span>

### <span data-ttu-id="396af-105">Devre dışı bırak (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="396af-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396af-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="396af-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="396af-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="396af-107">DESCRIPTION</span></span>
<span data-ttu-id="396af-108">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="396af-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="396af-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="396af-109">EXAMPLES</span></span>

### <span data-ttu-id="396af-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="396af-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="396af-111">Ölçeklendirme birimi düğümü için bakım modunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="396af-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="396af-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="396af-112">PARAMETERS</span></span>

### <span data-ttu-id="396af-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="396af-113">-Name</span></span>
<span data-ttu-id="396af-114">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="396af-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396af-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="396af-115">-Location</span></span>
<span data-ttu-id="396af-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="396af-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="396af-117">-ResourceGroupName</span></span>
<span data-ttu-id="396af-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="396af-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396af-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="396af-119">-ResourceId</span></span>
<span data-ttu-id="396af-120">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="396af-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="396af-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="396af-121">-AsJob</span></span>
<span data-ttu-id="396af-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="396af-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="396af-123">-Force</span><span class="sxs-lookup"><span data-stu-id="396af-123">-Force</span></span>
<span data-ttu-id="396af-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="396af-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="396af-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="396af-125">-WhatIf</span></span>
<span data-ttu-id="396af-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="396af-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="396af-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="396af-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="396af-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="396af-128">-Confirm</span></span>
<span data-ttu-id="396af-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="396af-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="396af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396af-130">CommonParameters</span></span>
<span data-ttu-id="396af-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="396af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396af-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="396af-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396af-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="396af-133">INPUTS</span></span>

## <span data-ttu-id="396af-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="396af-134">OUTPUTS</span></span>

## <span data-ttu-id="396af-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="396af-135">NOTES</span></span>

## <span data-ttu-id="396af-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="396af-136">RELATED LINKS</span></span>
