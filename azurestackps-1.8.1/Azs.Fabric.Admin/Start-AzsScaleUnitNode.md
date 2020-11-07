---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935175"
---
# <span data-ttu-id="8f25d-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="8f25d-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="8f25d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f25d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f25d-103">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="8f25d-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="8f25d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f25d-104">SYNTAX</span></span>

### <span data-ttu-id="8f25d-105">PowerOn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f25d-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f25d-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="8f25d-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f25d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f25d-107">DESCRIPTION</span></span>
<span data-ttu-id="8f25d-108">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="8f25d-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="8f25d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f25d-109">EXAMPLES</span></span>

### <span data-ttu-id="8f25d-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="8f25d-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="8f25d-111">ProvisioningState: başarılı</span><span class="sxs-lookup"><span data-stu-id="8f25d-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="8f25d-112">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="8f25d-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="8f25d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f25d-113">PARAMETERS</span></span>

### <span data-ttu-id="8f25d-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f25d-114">-Name</span></span>
<span data-ttu-id="8f25d-115">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="8f25d-115">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f25d-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="8f25d-116">-Location</span></span>
<span data-ttu-id="8f25d-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="8f25d-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f25d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f25d-118">-ResourceGroupName</span></span>
<span data-ttu-id="8f25d-119">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8f25d-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f25d-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8f25d-120">-ResourceId</span></span>
<span data-ttu-id="8f25d-121">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8f25d-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="8f25d-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="8f25d-122">-AsJob</span></span>
<span data-ttu-id="8f25d-123">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="8f25d-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8f25d-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8f25d-124">-Force</span></span>
<span data-ttu-id="8f25d-125">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="8f25d-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8f25d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f25d-126">-WhatIf</span></span>
<span data-ttu-id="8f25d-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f25d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f25d-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f25d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f25d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f25d-129">-Confirm</span></span>
<span data-ttu-id="8f25d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f25d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f25d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f25d-131">CommonParameters</span></span>
<span data-ttu-id="8f25d-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f25d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f25d-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f25d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f25d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f25d-134">INPUTS</span></span>

## <span data-ttu-id="8f25d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f25d-135">OUTPUTS</span></span>

## <span data-ttu-id="8f25d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f25d-136">NOTES</span></span>

## <span data-ttu-id="8f25d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f25d-137">RELATED LINKS</span></span>
