---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8da912ed9751231a44c34b27df36abc62d55c4ab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106784"
---
# <span data-ttu-id="e502b-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="e502b-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="e502b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e502b-102">SYNOPSIS</span></span>
<span data-ttu-id="e502b-103">Sağlanan parametreleri kullanarak var olan bir işlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e502b-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="e502b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e502b-104">SYNTAX</span></span>

### <span data-ttu-id="e502b-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e502b-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e502b-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="e502b-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e502b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e502b-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e502b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e502b-108">DESCRIPTION</span></span>
<span data-ttu-id="e502b-109">Var olan bir işlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e502b-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="e502b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e502b-110">EXAMPLES</span></span>

### <span data-ttu-id="e502b-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e502b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="e502b-112">İşlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="e502b-112">Update a compute quota.</span></span>

## <span data-ttu-id="e502b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e502b-113">PARAMETERS</span></span>

### <span data-ttu-id="e502b-114">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="e502b-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="e502b-115">İzin verilen kullanılabilirlik kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="e502b-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="e502b-116">-CoresCount</span></span>
<span data-ttu-id="e502b-117">İzin verilen çekirdek sayısı.</span><span class="sxs-lookup"><span data-stu-id="e502b-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e502b-118">-InputObject</span></span>
<span data-ttu-id="e502b-119">Büyük olasılıkla değiştirilmiş COMPUTE Quota, Get-AzsComputeQuota formunu döndürdü.</span><span class="sxs-lookup"><span data-stu-id="e502b-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="e502b-120">-Location</span></span>
<span data-ttu-id="e502b-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="e502b-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="e502b-122">-Name</span></span>
<span data-ttu-id="e502b-123">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="e502b-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="e502b-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="e502b-125">Standart yönetilen disklerin ve anlık görüntülerin boyutu</span><span class="sxs-lookup"><span data-stu-id="e502b-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e502b-126">-ResourceId</span></span>
<span data-ttu-id="e502b-127">ARM COMPUTE kota kimliği.</span><span class="sxs-lookup"><span data-stu-id="e502b-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-128">-Standardmanageddiskandsnapshotsıze</span><span class="sxs-lookup"><span data-stu-id="e502b-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="e502b-129">Standart yönetilen disklerin ve anlık görüntülerin boyutu</span><span class="sxs-lookup"><span data-stu-id="e502b-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="e502b-130">-VirtualMachineCount</span></span>
<span data-ttu-id="e502b-131">İzin verilen sanal makine sayısı.</span><span class="sxs-lookup"><span data-stu-id="e502b-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="e502b-132">-VmScaleSetCount</span></span>
<span data-ttu-id="e502b-133">İzin verilen ölçek kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="e502b-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e502b-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e502b-134">-Confirm</span></span>
<span data-ttu-id="e502b-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e502b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e502b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e502b-136">-WhatIf</span></span>
<span data-ttu-id="e502b-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e502b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e502b-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e502b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e502b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e502b-139">CommonParameters</span></span>
<span data-ttu-id="e502b-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e502b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e502b-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e502b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e502b-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e502b-142">INPUTS</span></span>

## <span data-ttu-id="e502b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e502b-143">OUTPUTS</span></span>

### <span data-ttu-id="e502b-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="e502b-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="e502b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e502b-145">NOTES</span></span>

## <span data-ttu-id="e502b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e502b-146">RELATED LINKS</span></span>

