---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761759"
---
# <span data-ttu-id="66ec9-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="66ec9-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="66ec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="66ec9-103">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="66ec9-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="66ec9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66ec9-104">SYNTAX</span></span>

### <span data-ttu-id="66ec9-105">Durdur (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66ec9-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ec9-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="66ec9-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66ec9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="66ec9-107">DESCRIPTION</span></span>
<span data-ttu-id="66ec9-108">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="66ec9-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="66ec9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66ec9-109">EXAMPLES</span></span>

### <span data-ttu-id="66ec9-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="66ec9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="66ec9-111">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="66ec9-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="66ec9-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="66ec9-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="66ec9-113">Ölçek birimi düğümünü kapatma.</span><span class="sxs-lookup"><span data-stu-id="66ec9-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="66ec9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66ec9-114">PARAMETERS</span></span>

### <span data-ttu-id="66ec9-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="66ec9-115">-AsJob</span></span>
<span data-ttu-id="66ec9-116">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="66ec9-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="66ec9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="66ec9-117">-Force</span></span>
<span data-ttu-id="66ec9-118">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="66ec9-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="66ec9-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="66ec9-119">-Location</span></span>
<span data-ttu-id="66ec9-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="66ec9-120">Location of the resource.</span></span>

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

### <span data-ttu-id="66ec9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="66ec9-121">-Name</span></span>
<span data-ttu-id="66ec9-122">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="66ec9-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="66ec9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ec9-123">-ResourceGroupName</span></span>
<span data-ttu-id="66ec9-124">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="66ec9-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="66ec9-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="66ec9-125">-ResourceId</span></span>
<span data-ttu-id="66ec9-126">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="66ec9-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="66ec9-127">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="66ec9-127">-Shutdown</span></span>
<span data-ttu-id="66ec9-128">Ayarla işlevi, ölçek birimi düğümünü dikkatlice kapatır; Aksi takdirde, ölçek birimi düğümünü kapatın.</span><span class="sxs-lookup"><span data-stu-id="66ec9-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="66ec9-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="66ec9-129">-Confirm</span></span>
<span data-ttu-id="66ec9-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66ec9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ec9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ec9-131">-WhatIf</span></span>
<span data-ttu-id="66ec9-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66ec9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ec9-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66ec9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ec9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ec9-134">CommonParameters</span></span>
<span data-ttu-id="66ec9-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66ec9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ec9-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ec9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ec9-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66ec9-137">INPUTS</span></span>

## <span data-ttu-id="66ec9-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66ec9-138">OUTPUTS</span></span>

## <span data-ttu-id="66ec9-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66ec9-139">NOTES</span></span>

## <span data-ttu-id="66ec9-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66ec9-140">RELATED LINKS</span></span>

