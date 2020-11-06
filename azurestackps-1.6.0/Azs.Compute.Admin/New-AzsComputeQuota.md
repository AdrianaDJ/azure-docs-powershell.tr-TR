---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc92bcc617c771c15330d1a24e8ed24466f7ffc7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571333"
---
# <span data-ttu-id="c20ce-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="c20ce-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="c20ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c20ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c20ce-103">Hesaplama kaynaklarını sınırlandırmak için kullanılan yeni bir işlem kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c20ce-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="c20ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c20ce-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c20ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c20ce-105">DESCRIPTION</span></span>
<span data-ttu-id="c20ce-106">Yeni bir işlem kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c20ce-106">Create a new compute quota.</span></span>

## <span data-ttu-id="c20ce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c20ce-107">EXAMPLES</span></span>

### <span data-ttu-id="c20ce-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c20ce-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="c20ce-109">Yeni bir işlem kotası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c20ce-109">Create a new compute quota.</span></span>

## <span data-ttu-id="c20ce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c20ce-110">PARAMETERS</span></span>

### <span data-ttu-id="c20ce-111">-Kullanılabilirlik kümesi</span><span class="sxs-lookup"><span data-stu-id="c20ce-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="c20ce-112">İzin verilen kullanılabilirlik kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="c20ce-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20ce-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="c20ce-113">-CoresCount</span></span>
<span data-ttu-id="c20ce-114">İzin verilen çekirdek sayısı.</span><span class="sxs-lookup"><span data-stu-id="c20ce-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20ce-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="c20ce-115">-Location</span></span>
<span data-ttu-id="c20ce-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="c20ce-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20ce-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c20ce-117">-Name</span></span>
<span data-ttu-id="c20ce-118">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="c20ce-118">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20ce-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="c20ce-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="c20ce-120">Standart yönetilen disklerin ve anlık görüntülerin boyutu</span><span class="sxs-lookup"><span data-stu-id="c20ce-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20ce-121">-Standardmanageddiskandsnapshotsıze</span><span class="sxs-lookup"><span data-stu-id="c20ce-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="c20ce-122">Standart yönetilen disklerin ve anlık görüntülerin boyutu</span><span class="sxs-lookup"><span data-stu-id="c20ce-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20ce-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="c20ce-123">-VirtualMachineCount</span></span>
<span data-ttu-id="c20ce-124">İzin verilen sanal makine sayısı.</span><span class="sxs-lookup"><span data-stu-id="c20ce-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20ce-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="c20ce-125">-VmScaleSetCount</span></span>
<span data-ttu-id="c20ce-126">İzin verilen ölçek kümesi sayısı.</span><span class="sxs-lookup"><span data-stu-id="c20ce-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20ce-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="c20ce-127">-Confirm</span></span>
<span data-ttu-id="c20ce-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c20ce-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c20ce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c20ce-129">-WhatIf</span></span>
<span data-ttu-id="c20ce-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c20ce-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c20ce-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c20ce-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c20ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c20ce-132">CommonParameters</span></span>
<span data-ttu-id="c20ce-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c20ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c20ce-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c20ce-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c20ce-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c20ce-135">INPUTS</span></span>

## <span data-ttu-id="c20ce-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c20ce-136">OUTPUTS</span></span>

### <span data-ttu-id="c20ce-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="c20ce-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="c20ce-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c20ce-138">NOTES</span></span>

## <span data-ttu-id="c20ce-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c20ce-139">RELATED LINKS</span></span>

