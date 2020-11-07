---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: bc24cab117a3ada64c4e64118b4b9b86ebffef55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752624"
---
# <span data-ttu-id="4ab95-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="4ab95-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="4ab95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ab95-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab95-103">Bir Vmsubnet 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4ab95-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="4ab95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ab95-104">SYNTAX</span></span>

### <span data-ttu-id="4ab95-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ab95-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab95-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="4ab95-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ab95-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4ab95-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ab95-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ab95-108">DESCRIPTION</span></span>
<span data-ttu-id="4ab95-109">Bir Vmsubnet 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4ab95-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="4ab95-110">Şimdilik, izin verilen tek güncelleştirme yönetilen veri diski ekliyor.</span><span class="sxs-lookup"><span data-stu-id="4ab95-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="4ab95-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ab95-111">EXAMPLES</span></span>

### <span data-ttu-id="4ab95-112">Örnek 1: New-AzVMDataDisk kullanarak bir VMSS VM 'ye yönetilen veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="4ab95-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="4ab95-113">İlk komut, varolan bir yönetilen diski alır.</span><span class="sxs-lookup"><span data-stu-id="4ab95-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="4ab95-114">Next komutu, yönetilen diskle bir veri diski nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ab95-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="4ab95-115">Next komutu, kaynak grup adı, VMSS adı ve örnek KIMLIĞI tarafından verilen mevcut bir VMSS VM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="4ab95-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="4ab95-116">Son komutu, yeni veri diski ekleyerek VMSS VM 'yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4ab95-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="4ab95-117">Örnek 2: Add-AzVMDataDisk kullanarak bir VMSS VM 'ye yönetilen veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="4ab95-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="4ab95-118">İlk komut, varolan bir yönetilen diski alır.</span><span class="sxs-lookup"><span data-stu-id="4ab95-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="4ab95-119">Next komutu, kaynak grup adı, VMSS adı ve örnek KIMLIĞI tarafından verilen mevcut bir VMSS VM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="4ab95-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="4ab95-120">Sonraki komut, $VmssVM yerel olarak depolanan VMSS VM 'ye yönetilen diski ekler.</span><span class="sxs-lookup"><span data-stu-id="4ab95-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="4ab95-121">Son komutu, VMSS VM 'yi ekli veri disketiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4ab95-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="4ab95-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ab95-122">PARAMETERS</span></span>

### <span data-ttu-id="4ab95-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="4ab95-123">-AsJob</span></span>
<span data-ttu-id="4ab95-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4ab95-124">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-125">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="4ab95-125">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ab95-126">-DefaultProfile</span></span>
<span data-ttu-id="4ab95-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ab95-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4ab95-128">-InstanceId</span></span>
<span data-ttu-id="4ab95-129">Bir VMSS VM 'nin örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ab95-129">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-130">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="4ab95-130">-ProtectFromScaleIn</span></span>
<span data-ttu-id="4ab95-131">Sanal makine ölçek kümesi VM 'sinin ölçeklendirme işlemi sırasında silinmek üzere değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ab95-131">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-132">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="4ab95-132">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="4ab95-133">VMSS 'de başlatılan model güncelleştirmeleri veya eylemlerinin (ölçeklendirme dahil) VMSS VM 'ye uygulanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4ab95-133">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab95-134">-ResourceGroupName</span></span>
<span data-ttu-id="4ab95-135">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ab95-135">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4ab95-136">-ResourceId</span></span>
<span data-ttu-id="4ab95-137">Sanal makine ölçek kümesi VM 'sinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4ab95-137">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-138">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4ab95-138">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="4ab95-139">Yerel sanal makine ölçek kümesi VM nesnesi</span><span class="sxs-lookup"><span data-stu-id="4ab95-139">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-140">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4ab95-140">-VMScaleSetName</span></span>
<span data-ttu-id="4ab95-141">Sanal makine ölçek kümesi adı</span><span class="sxs-lookup"><span data-stu-id="4ab95-141">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ab95-142">-Confirm</span></span>
<span data-ttu-id="4ab95-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ab95-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ab95-144">-WhatIf</span></span>
<span data-ttu-id="4ab95-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ab95-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ab95-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ab95-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ab95-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab95-147">CommonParameters</span></span>
<span data-ttu-id="4ab95-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ab95-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab95-149">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4ab95-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab95-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ab95-150">INPUTS</span></span>

### <span data-ttu-id="4ab95-151">System. String</span><span class="sxs-lookup"><span data-stu-id="4ab95-151">System.String</span></span>

### <span data-ttu-id="4ab95-152">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="4ab95-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="4ab95-153">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4ab95-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4ab95-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ab95-154">OUTPUTS</span></span>

### <span data-ttu-id="4ab95-155">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="4ab95-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="4ab95-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ab95-156">NOTES</span></span>

## <span data-ttu-id="4ab95-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ab95-157">RELATED LINKS</span></span>
