---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106649"
---
# <span data-ttu-id="32f2f-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="32f2f-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="32f2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="32f2f-103">Ölçeklendirme birimi düğümü için bakım modunu durdurun.</span><span class="sxs-lookup"><span data-stu-id="32f2f-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="32f2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32f2f-104">SYNTAX</span></span>

### <span data-ttu-id="32f2f-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32f2f-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32f2f-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="32f2f-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32f2f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="32f2f-107">DESCRIPTION</span></span>
<span data-ttu-id="32f2f-108">Ölçeklendirme birimi düğümü için bakım modunu durdurun.</span><span class="sxs-lookup"><span data-stu-id="32f2f-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="32f2f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32f2f-109">EXAMPLES</span></span>

### <span data-ttu-id="32f2f-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="32f2f-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="32f2f-111">Ölçeklendirme birimi düğümündeki bakım modunu durdurma.</span><span class="sxs-lookup"><span data-stu-id="32f2f-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="32f2f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32f2f-112">PARAMETERS</span></span>

### <span data-ttu-id="32f2f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="32f2f-113">-Name</span></span>
<span data-ttu-id="32f2f-114">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="32f2f-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="32f2f-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="32f2f-115">-Location</span></span>
<span data-ttu-id="32f2f-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="32f2f-116">Location of the resource.</span></span>

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

### <span data-ttu-id="32f2f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32f2f-117">-ResourceGroupName</span></span>
<span data-ttu-id="32f2f-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="32f2f-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="32f2f-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="32f2f-119">-ResourceId</span></span>
<span data-ttu-id="32f2f-120">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="32f2f-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="32f2f-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="32f2f-121">-AsJob</span></span>
<span data-ttu-id="32f2f-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="32f2f-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="32f2f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="32f2f-123">-Force</span></span>
<span data-ttu-id="32f2f-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="32f2f-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="32f2f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32f2f-125">-WhatIf</span></span>
<span data-ttu-id="32f2f-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32f2f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32f2f-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32f2f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32f2f-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="32f2f-128">-Confirm</span></span>
<span data-ttu-id="32f2f-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32f2f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32f2f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32f2f-130">CommonParameters</span></span>
<span data-ttu-id="32f2f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32f2f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32f2f-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32f2f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32f2f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32f2f-133">INPUTS</span></span>

## <span data-ttu-id="32f2f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32f2f-134">OUTPUTS</span></span>

## <span data-ttu-id="32f2f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32f2f-135">NOTES</span></span>

## <span data-ttu-id="32f2f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32f2f-136">RELATED LINKS</span></span>
