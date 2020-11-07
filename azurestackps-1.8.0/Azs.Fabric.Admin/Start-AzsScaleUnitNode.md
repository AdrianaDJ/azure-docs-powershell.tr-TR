---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934599"
---
# <span data-ttu-id="66bfa-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="66bfa-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="66bfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="66bfa-103">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="66bfa-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="66bfa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66bfa-104">SYNTAX</span></span>

### <span data-ttu-id="66bfa-105">PowerOn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66bfa-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66bfa-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="66bfa-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66bfa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="66bfa-107">DESCRIPTION</span></span>
<span data-ttu-id="66bfa-108">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="66bfa-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="66bfa-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66bfa-109">EXAMPLES</span></span>

### <span data-ttu-id="66bfa-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="66bfa-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="66bfa-111">ProvisioningState: başarılı</span><span class="sxs-lookup"><span data-stu-id="66bfa-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="66bfa-112">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="66bfa-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="66bfa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66bfa-113">PARAMETERS</span></span>

### <span data-ttu-id="66bfa-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="66bfa-114">-Name</span></span>
<span data-ttu-id="66bfa-115">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="66bfa-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="66bfa-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="66bfa-116">-Location</span></span>
<span data-ttu-id="66bfa-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="66bfa-117">Location of the resource.</span></span>

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

### <span data-ttu-id="66bfa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66bfa-118">-ResourceGroupName</span></span>
<span data-ttu-id="66bfa-119">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="66bfa-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="66bfa-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="66bfa-120">-ResourceId</span></span>
<span data-ttu-id="66bfa-121">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="66bfa-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="66bfa-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="66bfa-122">-AsJob</span></span>
<span data-ttu-id="66bfa-123">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="66bfa-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="66bfa-124">-Force</span><span class="sxs-lookup"><span data-stu-id="66bfa-124">-Force</span></span>
<span data-ttu-id="66bfa-125">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="66bfa-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="66bfa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66bfa-126">-WhatIf</span></span>
<span data-ttu-id="66bfa-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66bfa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66bfa-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66bfa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66bfa-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="66bfa-129">-Confirm</span></span>
<span data-ttu-id="66bfa-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66bfa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66bfa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bfa-131">CommonParameters</span></span>
<span data-ttu-id="66bfa-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66bfa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bfa-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66bfa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bfa-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66bfa-134">INPUTS</span></span>

## <span data-ttu-id="66bfa-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66bfa-135">OUTPUTS</span></span>

## <span data-ttu-id="66bfa-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66bfa-136">NOTES</span></span>

## <span data-ttu-id="66bfa-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66bfa-137">RELATED LINKS</span></span>
