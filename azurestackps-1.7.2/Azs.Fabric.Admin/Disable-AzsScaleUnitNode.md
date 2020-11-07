---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70ee408b65839e46e408256780a6d705c9881bde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934542"
---
# <span data-ttu-id="eb36f-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="eb36f-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="eb36f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb36f-102">SYNOPSIS</span></span>
<span data-ttu-id="eb36f-103">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="eb36f-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="eb36f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eb36f-104">SYNTAX</span></span>

### <span data-ttu-id="eb36f-105">Devre dışı bırak (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eb36f-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb36f-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="eb36f-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb36f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eb36f-107">DESCRIPTION</span></span>
<span data-ttu-id="eb36f-108">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="eb36f-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="eb36f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eb36f-109">EXAMPLES</span></span>

### <span data-ttu-id="eb36f-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="eb36f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="eb36f-111">Ölçeklendirme birimi düğümü için bakım modunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="eb36f-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="eb36f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eb36f-112">PARAMETERS</span></span>

### <span data-ttu-id="eb36f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="eb36f-113">-AsJob</span></span>
<span data-ttu-id="eb36f-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="eb36f-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="eb36f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="eb36f-115">-Force</span></span>
<span data-ttu-id="eb36f-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="eb36f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="eb36f-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="eb36f-117">-Location</span></span>
<span data-ttu-id="eb36f-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="eb36f-118">Location of the resource.</span></span>

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

### <span data-ttu-id="eb36f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="eb36f-119">-Name</span></span>
<span data-ttu-id="eb36f-120">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="eb36f-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="eb36f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb36f-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb36f-122">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="eb36f-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="eb36f-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="eb36f-123">-ResourceId</span></span>
<span data-ttu-id="eb36f-124">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="eb36f-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="eb36f-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="eb36f-125">-Confirm</span></span>
<span data-ttu-id="eb36f-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eb36f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb36f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb36f-127">-WhatIf</span></span>
<span data-ttu-id="eb36f-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eb36f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb36f-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eb36f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb36f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb36f-130">CommonParameters</span></span>
<span data-ttu-id="eb36f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eb36f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb36f-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb36f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb36f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eb36f-133">INPUTS</span></span>

## <span data-ttu-id="eb36f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eb36f-134">OUTPUTS</span></span>

## <span data-ttu-id="eb36f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eb36f-135">NOTES</span></span>

## <span data-ttu-id="eb36f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eb36f-136">RELATED LINKS</span></span>

