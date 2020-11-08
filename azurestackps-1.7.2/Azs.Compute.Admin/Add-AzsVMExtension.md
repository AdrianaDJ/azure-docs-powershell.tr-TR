---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42181271e9295212f256cfc519e8ecc32eeae048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933928"
---
# <span data-ttu-id="92eff-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="92eff-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="92eff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92eff-102">SYNOPSIS</span></span>
<span data-ttu-id="92eff-103">Yeni bir sanal makine uzantısı görüntüsü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="92eff-103">Create a new virtual machine extension image.</span></span>

## <span data-ttu-id="92eff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92eff-104">SYNTAX</span></span>

```
Add-AzsVMExtension [-Publisher] <String> [-Type] <String> [-Version] <String> [-SourceBlob] <Object>
 [-VmOsType] <Object> [-ComputeRole] <String> [-VmScaleSetEnabled] [-SupportMultipleExtensions]
 [-IsSystemExtension] [[-Location] <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92eff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92eff-105">DESCRIPTION</span></span>
<span data-ttu-id="92eff-106">Sanal makine uzantısı görüntüsü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="92eff-106">Create a virtual machine extension image.</span></span>

## <span data-ttu-id="92eff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92eff-107">EXAMPLES</span></span>

### <span data-ttu-id="92eff-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="92eff-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"
```

<span data-ttu-id="92eff-109">Yeni bir platform görüntüsü uzantısı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="92eff-109">Add a new platform image extension.</span></span>

## <span data-ttu-id="92eff-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92eff-110">PARAMETERS</span></span>

### <span data-ttu-id="92eff-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="92eff-111">-AsJob</span></span>
<span data-ttu-id="92eff-112">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="92eff-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="92eff-113">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="92eff-113">-ComputeRole</span></span>
<span data-ttu-id="92eff-114">Bu uzantının desteklediği rol, IaaS veya PaaS türü.</span><span class="sxs-lookup"><span data-stu-id="92eff-114">The type of role, IaaS or PaaS, this extension supports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eff-115">-Force</span><span class="sxs-lookup"><span data-stu-id="92eff-115">-Force</span></span>
<span data-ttu-id="92eff-116">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="92eff-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="92eff-117">-Ispsystegeri</span><span class="sxs-lookup"><span data-stu-id="92eff-117">-IsSystemExtension</span></span>
<span data-ttu-id="92eff-118">Uzantının sistem için olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92eff-118">Indicates if the extension is for the system.</span></span>

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

### <span data-ttu-id="92eff-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="92eff-119">-Location</span></span>
<span data-ttu-id="92eff-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="92eff-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eff-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="92eff-121">-Publisher</span></span>
<span data-ttu-id="92eff-122">Yayımcının adı.</span><span class="sxs-lookup"><span data-stu-id="92eff-122">Name of the publisher.</span></span>

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

### <span data-ttu-id="92eff-123">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="92eff-123">-SourceBlob</span></span>
<span data-ttu-id="92eff-124">Sanal makine uzantısı paketinin URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="92eff-124">URI to virtual machine extension package.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eff-125">-Supportçoğuluzantıları</span><span class="sxs-lookup"><span data-stu-id="92eff-125">-SupportMultipleExtensions</span></span>
<span data-ttu-id="92eff-126">Birden çok uzantı destekliyorsa doğru.</span><span class="sxs-lookup"><span data-stu-id="92eff-126">True if supports multiple extensions.</span></span>

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

### <span data-ttu-id="92eff-127">-Tür</span><span class="sxs-lookup"><span data-stu-id="92eff-127">-Type</span></span>
<span data-ttu-id="92eff-128">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="92eff-128">Type of extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eff-129">-Version</span><span class="sxs-lookup"><span data-stu-id="92eff-129">-Version</span></span>
<span data-ttu-id="92eff-130">Sanal makine görüntü uzantısının sürümü.</span><span class="sxs-lookup"><span data-stu-id="92eff-130">The version of the vritual machine image extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eff-131">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="92eff-131">-VmOsType</span></span>
<span data-ttu-id="92eff-132">Uzantı işleyicisini dağıtmak için gereken hedef sanal makine işletim sistemi türü.</span><span class="sxs-lookup"><span data-stu-id="92eff-132">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92eff-133">-VmScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="92eff-133">-VmScaleSetEnabled</span></span>
<span data-ttu-id="92eff-134">Uzantının sanal makine ölçek kümesi desteği için etkinleştirilip etkinleştirilmediğini gösteren değer.</span><span class="sxs-lookup"><span data-stu-id="92eff-134">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

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

### <span data-ttu-id="92eff-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="92eff-135">-Confirm</span></span>
<span data-ttu-id="92eff-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92eff-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92eff-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92eff-137">-WhatIf</span></span>
<span data-ttu-id="92eff-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92eff-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92eff-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92eff-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92eff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92eff-140">CommonParameters</span></span>
<span data-ttu-id="92eff-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92eff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92eff-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92eff-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92eff-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92eff-143">INPUTS</span></span>

## <span data-ttu-id="92eff-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92eff-144">OUTPUTS</span></span>

### <span data-ttu-id="92eff-145">VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="92eff-145">VmExtensionObject</span></span>

## <span data-ttu-id="92eff-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92eff-146">NOTES</span></span>

## <span data-ttu-id="92eff-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92eff-147">RELATED LINKS</span></span>
