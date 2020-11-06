---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571978"
---
# <span data-ttu-id="e102e-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e102e-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="e102e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e102e-102">SYNOPSIS</span></span>
<span data-ttu-id="e102e-103">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="e102e-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="e102e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e102e-104">SYNTAX</span></span>

### <span data-ttu-id="e102e-105">PowerOn (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e102e-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e102e-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="e102e-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e102e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e102e-107">DESCRIPTION</span></span>
<span data-ttu-id="e102e-108">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="e102e-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="e102e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e102e-109">EXAMPLES</span></span>

### <span data-ttu-id="e102e-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e102e-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="e102e-111">ProvisioningState: başarılı</span><span class="sxs-lookup"><span data-stu-id="e102e-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="e102e-112">Ölçek birimi düğümündeki güç.</span><span class="sxs-lookup"><span data-stu-id="e102e-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="e102e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e102e-113">PARAMETERS</span></span>

### <span data-ttu-id="e102e-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="e102e-114">-AsJob</span></span>
<span data-ttu-id="e102e-115">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="e102e-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e102e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e102e-116">-Force</span></span>
<span data-ttu-id="e102e-117">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="e102e-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e102e-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="e102e-118">-Location</span></span>
<span data-ttu-id="e102e-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="e102e-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e102e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e102e-120">-Name</span></span>
<span data-ttu-id="e102e-121">Ölçek birimi düğümünün adı.</span><span class="sxs-lookup"><span data-stu-id="e102e-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="e102e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e102e-122">-ResourceGroupName</span></span>
<span data-ttu-id="e102e-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e102e-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e102e-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e102e-124">-ResourceId</span></span>
<span data-ttu-id="e102e-125">Birim düğümü kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e102e-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="e102e-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="e102e-126">-Confirm</span></span>
<span data-ttu-id="e102e-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e102e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e102e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e102e-128">-WhatIf</span></span>
<span data-ttu-id="e102e-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e102e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e102e-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e102e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e102e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e102e-131">CommonParameters</span></span>
<span data-ttu-id="e102e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e102e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e102e-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e102e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e102e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e102e-134">INPUTS</span></span>

## <span data-ttu-id="e102e-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e102e-135">OUTPUTS</span></span>

## <span data-ttu-id="e102e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e102e-136">NOTES</span></span>

## <span data-ttu-id="e102e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e102e-137">RELATED LINKS</span></span>

