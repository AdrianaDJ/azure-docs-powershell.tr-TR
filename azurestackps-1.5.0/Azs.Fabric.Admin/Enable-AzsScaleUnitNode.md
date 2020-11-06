---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 932d0b77fc6df9a88a2ee13ad92856727db82f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571654"
---
# <span data-ttu-id="89590-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="89590-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="89590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89590-102">SYNOPSIS</span></span>
<span data-ttu-id="89590-103">Ölçeklendirme birimi düğümü için bakım modunu durdurun.</span><span class="sxs-lookup"><span data-stu-id="89590-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="89590-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89590-104">SYNTAX</span></span>

### <span data-ttu-id="89590-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89590-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89590-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="89590-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89590-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="89590-107">DESCRIPTION</span></span>
<span data-ttu-id="89590-108">Ölçeklendirme birimi düğümü için bakım modunu durdurun.</span><span class="sxs-lookup"><span data-stu-id="89590-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="89590-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89590-109">EXAMPLES</span></span>

### <span data-ttu-id="89590-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="89590-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="89590-111">Ölçeklendirme birimi düğümündeki bakım modunu durdurma.</span><span class="sxs-lookup"><span data-stu-id="89590-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="89590-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89590-112">PARAMETERS</span></span>

### <span data-ttu-id="89590-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="89590-113">-AsJob</span></span>
<span data-ttu-id="89590-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="89590-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="89590-115">-Force</span><span class="sxs-lookup"><span data-stu-id="89590-115">-Force</span></span>
<span data-ttu-id="89590-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="89590-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="89590-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="89590-117">-Location</span></span>
<span data-ttu-id="89590-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="89590-118">Location of the resource.</span></span>

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

### <span data-ttu-id="89590-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="89590-119">-Name</span></span>
<span data-ttu-id="89590-120">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="89590-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="89590-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89590-121">-ResourceGroupName</span></span>
<span data-ttu-id="89590-122">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="89590-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="89590-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="89590-123">-ResourceId</span></span>
<span data-ttu-id="89590-124">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="89590-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="89590-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="89590-125">-Confirm</span></span>
<span data-ttu-id="89590-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89590-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89590-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89590-127">-WhatIf</span></span>
<span data-ttu-id="89590-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89590-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89590-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89590-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89590-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89590-130">CommonParameters</span></span>
<span data-ttu-id="89590-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89590-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89590-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89590-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89590-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89590-133">INPUTS</span></span>

## <span data-ttu-id="89590-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89590-134">OUTPUTS</span></span>

## <span data-ttu-id="89590-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89590-135">NOTES</span></span>

## <span data-ttu-id="89590-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89590-136">RELATED LINKS</span></span>

