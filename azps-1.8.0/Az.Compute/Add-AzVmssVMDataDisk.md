---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 81f9e57bd2d815616cfc856246ff6950230f7112
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761368"
---
# <span data-ttu-id="46c54-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="46c54-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="46c54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46c54-102">SYNOPSIS</span></span>
<span data-ttu-id="46c54-103">Bir VMSS VM 'ye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="46c54-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="46c54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46c54-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46c54-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46c54-105">DESCRIPTION</span></span>
<span data-ttu-id="46c54-106">**Add-Azvmssvmdatadısk** cmdlet 'ı bir VMSS VM 'ye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="46c54-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="46c54-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46c54-107">EXAMPLES</span></span>

### <span data-ttu-id="46c54-108">Örnek 1: bir VMSS VM 'ye yönetilen veri diski ekleyin.</span><span class="sxs-lookup"><span data-stu-id="46c54-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="46c54-109">İlk komut, varolan bir yönetilen diski alır.</span><span class="sxs-lookup"><span data-stu-id="46c54-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="46c54-110">Next komutu, kaynak grup adı, VMSS adı ve örnek KIMLIĞI tarafından verilen mevcut bir VMSS VM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="46c54-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="46c54-111">Sonraki komut, $VmssVM yerel olarak depolanan VMSS VM 'ye yönetilen diski ekler.</span><span class="sxs-lookup"><span data-stu-id="46c54-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="46c54-112">Son komutu, VMSS VM 'yi ekli veri disketiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="46c54-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="46c54-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46c54-113">PARAMETERS</span></span>

### <span data-ttu-id="46c54-114">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="46c54-114">-Caching</span></span>
<span data-ttu-id="46c54-115">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="46c54-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="46c54-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46c54-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46c54-117">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="46c54-117">ReadOnly</span></span>
- <span data-ttu-id="46c54-118">Yazma</span><span class="sxs-lookup"><span data-stu-id="46c54-118">ReadWrite</span></span>
- <span data-ttu-id="46c54-119">Yok varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="46c54-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="46c54-120">Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="46c54-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="46c54-121">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="46c54-121">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c54-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="46c54-122">-CreateOption</span></span>
<span data-ttu-id="46c54-123">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="46c54-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="46c54-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46c54-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="46c54-125">Nota.</span><span class="sxs-lookup"><span data-stu-id="46c54-125">Attach.</span></span>
<span data-ttu-id="46c54-126">Özel bir diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="46c54-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="46c54-127">Bu seçeneği belirttiğinizde *Sourceımageuri* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="46c54-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="46c54-128">Bu *, Azure* platformuna sanal sabit diskin (VHD) sanal sabit diskinin (VHD), sanal makineye veri diski olarak iliştirileceği yeri bildirmek için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="46c54-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="46c54-129">Boşaltma.</span><span class="sxs-lookup"><span data-stu-id="46c54-129">Empty.</span></span>
<span data-ttu-id="46c54-130">Boş bir veri disketi oluşturmak için bunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="46c54-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="46c54-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="46c54-131">FromImage.</span></span>
<span data-ttu-id="46c54-132">Genelleştirilmiş bir yansıma veya diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="46c54-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="46c54-133">Bu seçeneği belirttiğinizde, Azure platformuna veri diski olarak eklenecek VHD 'nin konumunu belirtmek için *Sourceımageuri* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="46c54-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="46c54-134">*Vhduri* parametresi, sanal makine tarafından kullanıldığında VERI diski VHD 'nin depolanacağı konumu tanımlayan konum olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="46c54-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c54-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c54-135">-DefaultProfile</span></span>
<span data-ttu-id="46c54-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46c54-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46c54-137">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="46c54-137">-DiskSizeInGB</span></span>
<span data-ttu-id="46c54-138">Sanal makineye eklenecek boş bir diskin boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="46c54-138">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c54-139">-LUN</span><span class="sxs-lookup"><span data-stu-id="46c54-139">-Lun</span></span>
<span data-ttu-id="46c54-140">Veri diskinin mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="46c54-140">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c54-141">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="46c54-141">-ManagedDiskId</span></span>
<span data-ttu-id="46c54-142">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="46c54-142">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c54-143">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="46c54-143">-StorageAccountType</span></span>
<span data-ttu-id="46c54-144">Yönetilen diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="46c54-144">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46c54-145">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="46c54-145">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="46c54-146">Veri diskinin ekleneceği yerel sanal makine ölçek kümesi VM nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46c54-146">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="46c54-147">Bir sanal makine ölçeği kümesi VM nesnesini edinmek için **Get-AzVmssVM** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46c54-147">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46c54-148">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="46c54-148">-WriteAccelerator</span></span>
<span data-ttu-id="46c54-149">Yönetilen veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46c54-149">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="46c54-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c54-150">CommonParameters</span></span>
<span data-ttu-id="46c54-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46c54-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c54-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46c54-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c54-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46c54-153">INPUTS</span></span>

### <span data-ttu-id="46c54-154">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="46c54-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="46c54-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="46c54-155">System.Int32</span></span>

### <span data-ttu-id="46c54-156">System. String</span><span class="sxs-lookup"><span data-stu-id="46c54-156">System.String</span></span>

### <span data-ttu-id="46c54-157">Microsoft. Azure. Management. COMPUTE. model. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="46c54-157">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="46c54-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46c54-158">OUTPUTS</span></span>

### <span data-ttu-id="46c54-159">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="46c54-159">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="46c54-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46c54-160">NOTES</span></span>

## <span data-ttu-id="46c54-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46c54-161">RELATED LINKS</span></span>