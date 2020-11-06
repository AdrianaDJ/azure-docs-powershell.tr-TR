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
ms.locfileid: "93571305"
---
# <span data-ttu-id="02a41-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="02a41-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="02a41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a41-102">SYNOPSIS</span></span>
<span data-ttu-id="02a41-103">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="02a41-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="02a41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02a41-104">SYNTAX</span></span>

### <span data-ttu-id="02a41-105">Devre dışı bırak (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02a41-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a41-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="02a41-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a41-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="02a41-107">DESCRIPTION</span></span>
<span data-ttu-id="02a41-108">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="02a41-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="02a41-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02a41-109">EXAMPLES</span></span>

### <span data-ttu-id="02a41-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="02a41-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="02a41-111">Ölçeklendirme birimi düğümü için bakım modunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="02a41-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="02a41-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02a41-112">PARAMETERS</span></span>

### <span data-ttu-id="02a41-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="02a41-113">-AsJob</span></span>
<span data-ttu-id="02a41-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="02a41-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="02a41-115">-Force</span><span class="sxs-lookup"><span data-stu-id="02a41-115">-Force</span></span>
<span data-ttu-id="02a41-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="02a41-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="02a41-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="02a41-117">-Location</span></span>
<span data-ttu-id="02a41-118">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="02a41-118">Location of the resource.</span></span>

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

### <span data-ttu-id="02a41-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="02a41-119">-Name</span></span>
<span data-ttu-id="02a41-120">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="02a41-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="02a41-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a41-121">-ResourceGroupName</span></span>
<span data-ttu-id="02a41-122">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="02a41-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="02a41-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02a41-123">-ResourceId</span></span>
<span data-ttu-id="02a41-124">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="02a41-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="02a41-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="02a41-125">-Confirm</span></span>
<span data-ttu-id="02a41-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02a41-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a41-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a41-127">-WhatIf</span></span>
<span data-ttu-id="02a41-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02a41-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a41-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02a41-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a41-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a41-130">CommonParameters</span></span>
<span data-ttu-id="02a41-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02a41-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a41-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a41-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a41-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02a41-133">INPUTS</span></span>

## <span data-ttu-id="02a41-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02a41-134">OUTPUTS</span></span>

## <span data-ttu-id="02a41-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02a41-135">NOTES</span></span>

## <span data-ttu-id="02a41-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02a41-136">RELATED LINKS</span></span>

