---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4caf955c25cd29c9cc9c09f1182454ee3a4d56df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934545"
---
# <span data-ttu-id="f69f6-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="f69f6-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="f69f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f69f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f69f6-103">Sağlanan parametreleri kullanarak var olan bir işlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f69f6-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="f69f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f69f6-104">SYNTAX</span></span>

### <span data-ttu-id="f69f6-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f69f6-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f69f6-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f69f6-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f69f6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f69f6-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f69f6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f69f6-108">DESCRIPTION</span></span>
<span data-ttu-id="f69f6-109">Var olan bir işlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f69f6-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="f69f6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f69f6-110">EXAMPLES</span></span>

### <span data-ttu-id="f69f6-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f69f6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="f69f6-112">İşlem kotasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f69f6-112">Update a compute quota.</span></span>

## <span data-ttu-id="f69f6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f69f6-113">PARAMETERS</span></span>

### <span data-ttu-id="f69f6-114">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="f69f6-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="f69f6-115">İzin verilen kullanılabilirlik kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="f69f6-115">Number of availability sets allowed.</span></span>

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

### <span data-ttu-id="f69f6-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="f69f6-116">-CoresCount</span></span>
<span data-ttu-id="f69f6-117">İzin verilen çekirdek sayısı.</span><span class="sxs-lookup"><span data-stu-id="f69f6-117">Number of cores allowed.</span></span>

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

### <span data-ttu-id="f69f6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f69f6-118">-InputObject</span></span>
<span data-ttu-id="f69f6-119">Büyük olasılıkla değiştirilmiş COMPUTE Quota, Get-AzsComputeQuota formunu döndürdü.</span><span class="sxs-lookup"><span data-stu-id="f69f6-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

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

### <span data-ttu-id="f69f6-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="f69f6-120">-Location</span></span>
<span data-ttu-id="f69f6-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="f69f6-121">Location of the resource.</span></span>

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

### <span data-ttu-id="f69f6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f69f6-122">-Name</span></span>
<span data-ttu-id="f69f6-123">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="f69f6-123">The name of the quota.</span></span>

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

### <span data-ttu-id="f69f6-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="f69f6-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="f69f6-125">Standart yönetilen disklerin ve anlık görüntülerin boyutu</span><span class="sxs-lookup"><span data-stu-id="f69f6-125">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="f69f6-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f69f6-126">-ResourceId</span></span>
<span data-ttu-id="f69f6-127">ARM COMPUTE kota kimliği.</span><span class="sxs-lookup"><span data-stu-id="f69f6-127">The ARM compute quota id.</span></span>

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

### <span data-ttu-id="f69f6-128">-Standardmanageddiskandsnapshotsıze</span><span class="sxs-lookup"><span data-stu-id="f69f6-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="f69f6-129">Standart yönetilen disklerin ve anlık görüntülerin boyutu</span><span class="sxs-lookup"><span data-stu-id="f69f6-129">Size for standard managed disks and snapshots allowed.</span></span>

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

### <span data-ttu-id="f69f6-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="f69f6-130">-VirtualMachineCount</span></span>
<span data-ttu-id="f69f6-131">İzin verilen sanal makine sayısı.</span><span class="sxs-lookup"><span data-stu-id="f69f6-131">Number of virtual machines allowed.</span></span>

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

### <span data-ttu-id="f69f6-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="f69f6-132">-VmScaleSetCount</span></span>
<span data-ttu-id="f69f6-133">İzin verilen ölçek kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="f69f6-133">Number of scale sets allowed.</span></span>

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

### <span data-ttu-id="f69f6-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="f69f6-134">-Confirm</span></span>
<span data-ttu-id="f69f6-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f69f6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f69f6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f69f6-136">-WhatIf</span></span>
<span data-ttu-id="f69f6-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f69f6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f69f6-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f69f6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f69f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69f6-139">CommonParameters</span></span>
<span data-ttu-id="f69f6-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f69f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69f6-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69f6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69f6-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f69f6-142">INPUTS</span></span>

## <span data-ttu-id="f69f6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f69f6-143">OUTPUTS</span></span>

### <span data-ttu-id="f69f6-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="f69f6-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="f69f6-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f69f6-145">NOTES</span></span>

## <span data-ttu-id="f69f6-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f69f6-146">RELATED LINKS</span></span>
