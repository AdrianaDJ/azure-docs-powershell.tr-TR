---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8da912ed9751231a44c34b27df36abc62d55c4ab
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934655"
---
# <span data-ttu-id="3be9d-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="3be9d-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="3be9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3be9d-102">SYNOPSIS</span></span>
<span data-ttu-id="3be9d-103">Sağlanan parametreleri kullanarak var olan bir işlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="3be9d-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="3be9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3be9d-104">SYNTAX</span></span>

### <span data-ttu-id="3be9d-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3be9d-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3be9d-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="3be9d-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3be9d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3be9d-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3be9d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3be9d-108">DESCRIPTION</span></span>
<span data-ttu-id="3be9d-109">Var olan bir işlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="3be9d-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="3be9d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3be9d-110">EXAMPLES</span></span>

### <span data-ttu-id="3be9d-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3be9d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="3be9d-112">İşlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="3be9d-112">Update a compute quota.</span></span>

## <span data-ttu-id="3be9d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3be9d-113">PARAMETERS</span></span>

### <span data-ttu-id="3be9d-114">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="3be9d-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="3be9d-115">İzin verilen kullanılabilirlik kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="3be9d-115">Number of availability sets allowed.</span></span>

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

### <span data-ttu-id="3be9d-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="3be9d-116">-CoresCount</span></span>
<span data-ttu-id="3be9d-117">İzin verilen çekirdek sayısı.</span><span class="sxs-lookup"><span data-stu-id="3be9d-117">Number of cores allowed.</span></span>

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

### <span data-ttu-id="3be9d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3be9d-118">-InputObject</span></span>
<span data-ttu-id="3be9d-119">Büyük olasılıkla değiştirilmiş COMPUTE Quota, Get-AzsComputeQuota formunu döndürdü.</span><span class="sxs-lookup"><span data-stu-id="3be9d-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

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

### <span data-ttu-id="3be9d-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="3be9d-120">-Location</span></span>
<span data-ttu-id="3be9d-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="3be9d-121">Location of the resource.</span></span>

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

### <span data-ttu-id="3be9d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="3be9d-122">-Name</span></span>
<span data-ttu-id="3be9d-123">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="3be9d-123">The name of the quota.</span></span>

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

### <span data-ttu-id="3be9d-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="3be9d-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="3be9d-125">Standart yönetilen disklerin ve anlık görüntülerin boyutu</span><span class="sxs-lookup"><span data-stu-id="3be9d-125">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="3be9d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3be9d-126">-ResourceId</span></span>
<span data-ttu-id="3be9d-127">ARM COMPUTE kota kimliği.</span><span class="sxs-lookup"><span data-stu-id="3be9d-127">The ARM compute quota id.</span></span>

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

### <span data-ttu-id="3be9d-128">-Standardmanageddiskandsnapshotsıze</span><span class="sxs-lookup"><span data-stu-id="3be9d-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="3be9d-129">Standart yönetilen disklerin ve anlık görüntülerin boyutu</span><span class="sxs-lookup"><span data-stu-id="3be9d-129">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="3be9d-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="3be9d-130">-VirtualMachineCount</span></span>
<span data-ttu-id="3be9d-131">İzin verilen sanal makine sayısı.</span><span class="sxs-lookup"><span data-stu-id="3be9d-131">Number of virtual machines allowed.</span></span>

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

### <span data-ttu-id="3be9d-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="3be9d-132">-VmScaleSetCount</span></span>
<span data-ttu-id="3be9d-133">İzin verilen ölçek kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="3be9d-133">Number of scale sets allowed.</span></span>

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

### <span data-ttu-id="3be9d-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="3be9d-134">-Confirm</span></span>
<span data-ttu-id="3be9d-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3be9d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3be9d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3be9d-136">-WhatIf</span></span>
<span data-ttu-id="3be9d-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3be9d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3be9d-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3be9d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3be9d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be9d-139">CommonParameters</span></span>
<span data-ttu-id="3be9d-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3be9d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be9d-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be9d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be9d-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3be9d-142">INPUTS</span></span>

## <span data-ttu-id="3be9d-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3be9d-143">OUTPUTS</span></span>

### <span data-ttu-id="3be9d-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="3be9d-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="3be9d-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3be9d-145">NOTES</span></span>

## <span data-ttu-id="3be9d-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3be9d-146">RELATED LINKS</span></span>

