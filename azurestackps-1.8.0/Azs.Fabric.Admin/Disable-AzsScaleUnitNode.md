---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934650"
---
# <span data-ttu-id="072fa-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="072fa-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="072fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="072fa-102">SYNOPSIS</span></span>
<span data-ttu-id="072fa-103">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="072fa-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="072fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="072fa-104">SYNTAX</span></span>

### <span data-ttu-id="072fa-105">Devre dışı bırak (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="072fa-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="072fa-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="072fa-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="072fa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="072fa-107">DESCRIPTION</span></span>
<span data-ttu-id="072fa-108">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="072fa-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="072fa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="072fa-109">EXAMPLES</span></span>

### <span data-ttu-id="072fa-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="072fa-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="072fa-111">Ölçeklendirme birimi düğümü için bakım modunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="072fa-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="072fa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="072fa-112">PARAMETERS</span></span>

### <span data-ttu-id="072fa-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="072fa-113">-Name</span></span>
<span data-ttu-id="072fa-114">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="072fa-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="072fa-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="072fa-115">-Location</span></span>
<span data-ttu-id="072fa-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="072fa-116">Location of the resource.</span></span>

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

### <span data-ttu-id="072fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="072fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="072fa-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="072fa-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="072fa-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="072fa-119">-ResourceId</span></span>
<span data-ttu-id="072fa-120">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="072fa-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="072fa-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="072fa-121">-AsJob</span></span>
<span data-ttu-id="072fa-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="072fa-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="072fa-123">-Force</span><span class="sxs-lookup"><span data-stu-id="072fa-123">-Force</span></span>
<span data-ttu-id="072fa-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="072fa-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="072fa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="072fa-125">-WhatIf</span></span>
<span data-ttu-id="072fa-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="072fa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="072fa-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="072fa-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="072fa-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="072fa-128">-Confirm</span></span>
<span data-ttu-id="072fa-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="072fa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="072fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072fa-130">CommonParameters</span></span>
<span data-ttu-id="072fa-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="072fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072fa-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="072fa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072fa-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="072fa-133">INPUTS</span></span>

## <span data-ttu-id="072fa-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="072fa-134">OUTPUTS</span></span>

## <span data-ttu-id="072fa-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="072fa-135">NOTES</span></span>

## <span data-ttu-id="072fa-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="072fa-136">RELATED LINKS</span></span>
