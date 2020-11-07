---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934986"
---
# <span data-ttu-id="d8f5a-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="d8f5a-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="d8f5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f5a-103">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="d8f5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8f5a-104">SYNTAX</span></span>

### <span data-ttu-id="d8f5a-105">Devre dışı bırak (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8f5a-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8f5a-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d8f5a-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f5a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8f5a-107">DESCRIPTION</span></span>
<span data-ttu-id="d8f5a-108">Ölçeklendirme birimi düğümü için bakım modunu başlatın.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="d8f5a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8f5a-109">EXAMPLES</span></span>

### <span data-ttu-id="d8f5a-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="d8f5a-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="d8f5a-111">Ölçeklendirme birimi düğümü için bakım modunu etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="d8f5a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8f5a-112">PARAMETERS</span></span>

### <span data-ttu-id="d8f5a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8f5a-113">-Name</span></span>
<span data-ttu-id="d8f5a-114">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="d8f5a-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="d8f5a-115">-Location</span></span>
<span data-ttu-id="d8f5a-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-116">Location of the resource.</span></span>

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

### <span data-ttu-id="d8f5a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f5a-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8f5a-118">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d8f5a-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d8f5a-119">-ResourceId</span></span>
<span data-ttu-id="d8f5a-120">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="d8f5a-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="d8f5a-121">-AsJob</span></span>
<span data-ttu-id="d8f5a-122">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d8f5a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d8f5a-123">-Force</span></span>
<span data-ttu-id="d8f5a-124">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d8f5a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f5a-125">-WhatIf</span></span>
<span data-ttu-id="d8f5a-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f5a-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f5a-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8f5a-128">-Confirm</span></span>
<span data-ttu-id="d8f5a-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f5a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f5a-130">CommonParameters</span></span>
<span data-ttu-id="d8f5a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8f5a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f5a-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8f5a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f5a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8f5a-133">INPUTS</span></span>

## <span data-ttu-id="d8f5a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8f5a-134">OUTPUTS</span></span>

## <span data-ttu-id="d8f5a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8f5a-135">NOTES</span></span>

## <span data-ttu-id="d8f5a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8f5a-136">RELATED LINKS</span></span>
