---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276756"
---
# <span data-ttu-id="214bb-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="214bb-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="214bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="214bb-102">SYNOPSIS</span></span>
<span data-ttu-id="214bb-103">Bir Vmsubnet 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="214bb-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="214bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="214bb-104">SYNTAX</span></span>

### <span data-ttu-id="214bb-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="214bb-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="214bb-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="214bb-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="214bb-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="214bb-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214bb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="214bb-108">DESCRIPTION</span></span>
<span data-ttu-id="214bb-109">Bir Vmsubnet 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="214bb-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="214bb-110">Şimdilik, izin verilen tek güncelleştirme yönetilen veri diski ekliyor.</span><span class="sxs-lookup"><span data-stu-id="214bb-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="214bb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="214bb-111">EXAMPLES</span></span>

### <span data-ttu-id="214bb-112">Örnek 1: New-AzVMDataDisk kullanarak bir VMSS VM 'ye yönetilen veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="214bb-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="214bb-113">İlk komut, varolan bir yönetilen diski alır.</span><span class="sxs-lookup"><span data-stu-id="214bb-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="214bb-114">Next komutu, yönetilen diskle bir veri diski nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="214bb-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="214bb-115">Next komutu, kaynak grup adı, VMSS adı ve örnek KIMLIĞI tarafından verilen mevcut bir VMSS VM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="214bb-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="214bb-116">Son komutu, yeni veri diski ekleyerek VMSS VM 'yi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="214bb-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="214bb-117">Örnek 2: Add-AzVMDataDisk kullanarak bir VMSS VM 'ye yönetilen veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="214bb-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="214bb-118">İlk komut, varolan bir yönetilen diski alır.</span><span class="sxs-lookup"><span data-stu-id="214bb-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="214bb-119">Next komutu, kaynak grup adı, VMSS adı ve örnek KIMLIĞI tarafından verilen mevcut bir VMSS VM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="214bb-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="214bb-120">Sonraki komut, $VmssVM yerel olarak depolanan VMSS VM 'ye yönetilen diski ekler.</span><span class="sxs-lookup"><span data-stu-id="214bb-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="214bb-121">Son komutu, VMSS VM 'yi ekli veri disketiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="214bb-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="214bb-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="214bb-122">Example 3</span></span>

<span data-ttu-id="214bb-123">Bir Vmsubnet 'in durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="214bb-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="214bb-124">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="214bb-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="214bb-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="214bb-125">PARAMETERS</span></span>

### <span data-ttu-id="214bb-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="214bb-126">-AsJob</span></span>
<span data-ttu-id="214bb-127">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="214bb-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="214bb-128">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="214bb-128">-DataDisk</span></span>

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

### <span data-ttu-id="214bb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214bb-129">-DefaultProfile</span></span>
<span data-ttu-id="214bb-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="214bb-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214bb-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="214bb-131">-InstanceId</span></span>
<span data-ttu-id="214bb-132">Bir VMSS VM 'nin örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="214bb-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="214bb-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="214bb-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="214bb-134">Sanal makine ölçek kümesi VM 'sinin ölçeklendirme işlemi sırasında silinmek üzere değerlendirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="214bb-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="214bb-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="214bb-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="214bb-136">VMSS 'de başlatılan model güncelleştirmeleri veya eylemlerinin (ölçeklendirme dahil) VMSS VM 'ye uygulanmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="214bb-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="214bb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214bb-137">-ResourceGroupName</span></span>
<span data-ttu-id="214bb-138">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="214bb-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="214bb-139">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="214bb-139">-ResourceId</span></span>
<span data-ttu-id="214bb-140">Sanal makine ölçek kümesi VM 'sinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="214bb-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="214bb-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="214bb-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="214bb-142">Yerel sanal makine ölçek kümesi VM nesnesi</span><span class="sxs-lookup"><span data-stu-id="214bb-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="214bb-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="214bb-143">-VMScaleSetName</span></span>
<span data-ttu-id="214bb-144">Sanal makine ölçek kümesi adı</span><span class="sxs-lookup"><span data-stu-id="214bb-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="214bb-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="214bb-145">-Confirm</span></span>
<span data-ttu-id="214bb-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="214bb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214bb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214bb-147">-WhatIf</span></span>
<span data-ttu-id="214bb-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="214bb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214bb-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="214bb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214bb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214bb-150">CommonParameters</span></span>
<span data-ttu-id="214bb-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="214bb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214bb-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="214bb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214bb-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="214bb-153">INPUTS</span></span>

### <span data-ttu-id="214bb-154">System. String</span><span class="sxs-lookup"><span data-stu-id="214bb-154">System.String</span></span>

### <span data-ttu-id="214bb-155">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="214bb-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="214bb-156">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="214bb-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="214bb-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="214bb-157">OUTPUTS</span></span>

### <span data-ttu-id="214bb-158">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="214bb-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="214bb-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="214bb-159">NOTES</span></span>

## <span data-ttu-id="214bb-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="214bb-160">RELATED LINKS</span></span>
