---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: de0f5fd2583f1622e750e71299a5753444feed1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592325"
---
# <span data-ttu-id="06e37-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="06e37-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="06e37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06e37-102">SYNOPSIS</span></span>
<span data-ttu-id="06e37-103">Bir sanal makineye veya bir VMSS VM 'ye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="06e37-103">Adds a data disk to a virtual machine or a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06e37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06e37-104">SYNTAX</span></span>

### <span data-ttu-id="06e37-105">VmNormalDiskParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06e37-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String>
 [[-SourceImageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06e37-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="06e37-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06e37-107">VmScaleSetVMParameterSetName</span><span class="sxs-lookup"><span data-stu-id="06e37-107">VmScaleSetVMParameterSetName</span></span>
```
Add-AzureRmVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [-ManagedDiskId] <String>
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06e37-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="06e37-108">DESCRIPTION</span></span>
<span data-ttu-id="06e37-109">**Add-Azurermvmdatadısk** cmdlet 'i, bir sanal makineye veya bir VMSS VM 'ye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="06e37-109">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine or a Vmss VM.</span></span>
<span data-ttu-id="06e37-110">Bir sanal makine oluşturduğunuzda veri diski ekleyebilirsiniz veya varolan bir sanal makineye veri diski ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06e37-110">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="06e37-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06e37-111">EXAMPLES</span></span>

### <span data-ttu-id="06e37-112">Örnek 1: yeni bir sanal makineye veri diskleri ekleme</span><span class="sxs-lookup"><span data-stu-id="06e37-112">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="06e37-113">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="06e37-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="06e37-114">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="06e37-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="06e37-115">Sonraki üç komut, $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03 değişkenlerine üç veri disklerinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="06e37-115">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="06e37-116">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="06e37-116">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="06e37-117">Her biri $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="06e37-117">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="06e37-118">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-118">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="06e37-119">Her diskin URI 'SI $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="06e37-119">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="06e37-120">Örnek 2: var olan bir sanal makineye veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="06e37-120">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="06e37-121">İlk komut VirtualMachine07 adındaki sanal makineyi [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="06e37-121">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="06e37-122">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="06e37-122">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="06e37-123">İkinci komut $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="06e37-123">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="06e37-124">Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="06e37-124">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="06e37-125">Örnek 3: genelleştirilmiş bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="06e37-125">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="06e37-126">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="06e37-126">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="06e37-127">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="06e37-127">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="06e37-128">Sonraki iki komut, veri görüntüsü ve veri disklerinin yollarını sırasıyla $DataImageUri ve $DataDiskUri değişkenlerine atar.</span><span class="sxs-lookup"><span data-stu-id="06e37-128">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="06e37-129">Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="06e37-129">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="06e37-130">Son komutlar $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="06e37-130">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="06e37-131">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-131">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="06e37-132">Örnek 4: özel bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diskleri ekleme</span><span class="sxs-lookup"><span data-stu-id="06e37-132">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="06e37-133">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="06e37-133">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="06e37-134">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="06e37-134">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="06e37-135">Sonraki komutlar veri diskinin yollarını $DataDiskUri değişkenine atar.</span><span class="sxs-lookup"><span data-stu-id="06e37-135">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="06e37-136">Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="06e37-136">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="06e37-137">Son komutu $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="06e37-137">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="06e37-138">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-138">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

### <span data-ttu-id="06e37-139">Örnek 5: bir VMSS VM 'ye yönetilen veri diski ekleyin.</span><span class="sxs-lookup"><span data-stu-id="06e37-139">Example 5: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="06e37-140">İlk komut, varolan bir yönetilen diski alır.</span><span class="sxs-lookup"><span data-stu-id="06e37-140">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="06e37-141">Next komutu, kaynak grup adı, VMSS adı ve örnek KIMLIĞI tarafından verilen mevcut bir VMSS VM 'yi alır.</span><span class="sxs-lookup"><span data-stu-id="06e37-141">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="06e37-142">Sonraki komut, $VmssVM yerel olarak depolanan VMSS VM 'ye yönetilen diski ekler.</span><span class="sxs-lookup"><span data-stu-id="06e37-142">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="06e37-143">Son komutu, VMSS VM 'yi ekli veri disketiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="06e37-143">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="06e37-144">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06e37-144">PARAMETERS</span></span>

### <span data-ttu-id="06e37-145">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="06e37-145">-Caching</span></span>
<span data-ttu-id="06e37-146">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-146">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="06e37-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="06e37-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06e37-148">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="06e37-148">ReadOnly</span></span>
- <span data-ttu-id="06e37-149">Yazma</span><span class="sxs-lookup"><span data-stu-id="06e37-149">ReadWrite</span></span>
- <span data-ttu-id="06e37-150">Yok varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="06e37-150">None The default value is ReadWrite.</span></span>
<span data-ttu-id="06e37-151">Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="06e37-151">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="06e37-152">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="06e37-152">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-153">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="06e37-153">-CreateOption</span></span>
<span data-ttu-id="06e37-154">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="06e37-154">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="06e37-155">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="06e37-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="06e37-156">Nota.</span><span class="sxs-lookup"><span data-stu-id="06e37-156">Attach.</span></span>
<span data-ttu-id="06e37-157">Özel bir diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="06e37-157">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="06e37-158">Bu seçeneği belirttiğinizde *Sourceımageuri* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="06e37-158">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="06e37-159">Bu *, Azure* platformuna sanal sabit diskin (VHD) sanal sabit diskinin (VHD), sanal makineye veri diski olarak iliştirileceği yeri bildirmek için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="06e37-159">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="06e37-160">Boşaltma.</span><span class="sxs-lookup"><span data-stu-id="06e37-160">Empty.</span></span>
<span data-ttu-id="06e37-161">Boş bir veri disketi oluşturmak için bunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="06e37-161">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="06e37-162">FromImage.</span><span class="sxs-lookup"><span data-stu-id="06e37-162">FromImage.</span></span>
<span data-ttu-id="06e37-163">Genelleştirilmiş bir yansıma veya diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="06e37-163">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="06e37-164">Bu seçeneği belirttiğinizde, Azure platformuna veri diski olarak eklenecek VHD 'nin konumunu belirtmek için *Sourceımageuri* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="06e37-164">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="06e37-165">*Vhduri* parametresi, sanal makine tarafından kullanıldığında VERI diski VHD 'nin depolanacağı konumu tanımlayan konum olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="06e37-165">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e37-166">-DefaultProfile</span></span>
<span data-ttu-id="06e37-167">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06e37-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-168">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="06e37-168">-DiskSizeInGB</span></span>
<span data-ttu-id="06e37-169">Sanal makineye eklenecek boş bir diskin boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-169">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-170">-LUN</span><span class="sxs-lookup"><span data-stu-id="06e37-170">-Lun</span></span>
<span data-ttu-id="06e37-171">Veri diskinin mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-171">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-172">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="06e37-172">-ManagedDiskId</span></span>
<span data-ttu-id="06e37-173">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-173">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-174">-Ad</span><span class="sxs-lookup"><span data-stu-id="06e37-174">-Name</span></span>
<span data-ttu-id="06e37-175">Eklenecek veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-175">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-176">-Sourceımageuri</span><span class="sxs-lookup"><span data-stu-id="06e37-176">-SourceImageUri</span></span>
<span data-ttu-id="06e37-177">Bu cmdlet 'in ilişolduğu diskin Kaynak URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-177">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="06e37-178">-StorageAccountType</span></span>
<span data-ttu-id="06e37-179">Yönetilen diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-179">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="06e37-180">-VhdUri</span></span>
<span data-ttu-id="06e37-181">Bir platform görüntüsü veya Kullanıcı görüntüsü kullanıldığında oluşturulacak sanal sabit disk (VHD) dosyasının Tekdüzen Kaynak tanımlayıcısını (VHD) belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-181">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="06e37-182">Bu cmdlet, resim ikili büyük nesnesini (blob) bu konuma kopyalar.</span><span class="sxs-lookup"><span data-stu-id="06e37-182">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="06e37-183">Bu, sanal makinenin başlayacağı konumdur.</span><span class="sxs-lookup"><span data-stu-id="06e37-183">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-184">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="06e37-184">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="06e37-185">Veri diskinin ekleneceği yerel sanal makine ölçek kümesi VM nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-185">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="06e37-186">Sanal makine ölçeği kümesi VM nesnesini edinmek için **Get-AzureRmVmssVM** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06e37-186">You can use the **Get-AzureRmVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: VmScaleSetVMParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-187">-VM</span><span class="sxs-lookup"><span data-stu-id="06e37-187">-VM</span></span>
<span data-ttu-id="06e37-188">Veri diskinin ekleneceği yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-188">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="06e37-189">Sanal makine nesnesi edinmek için **Get-AzureRmVM** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06e37-189">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="06e37-190">Sanal makine nesnesi oluşturmak için **New-AzureRmVMConfig** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06e37-190">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VmNormalDiskParameterSetName, VmManagedDiskParameterSetName
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-191">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="06e37-191">-WriteAccelerator</span></span>
<span data-ttu-id="06e37-192">Yönetilen veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06e37-192">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName, VmScaleSetVMParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e37-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e37-193">CommonParameters</span></span>
<span data-ttu-id="06e37-194">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06e37-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e37-195">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e37-195">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e37-196">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06e37-196">INPUTS</span></span>

### <span data-ttu-id="06e37-197">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="06e37-197">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="06e37-198">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="06e37-198">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="06e37-199">System. String</span><span class="sxs-lookup"><span data-stu-id="06e37-199">System.String</span></span>

### <span data-ttu-id="06e37-200">Microsoft. Azure. Management. COMPUTE. model. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="06e37-200">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="06e37-201">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="06e37-201">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="06e37-202">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06e37-202">OUTPUTS</span></span>

### <span data-ttu-id="06e37-203">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="06e37-203">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="06e37-204">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="06e37-204">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="06e37-205">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06e37-205">NOTES</span></span>

## <span data-ttu-id="06e37-206">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06e37-206">RELATED LINKS</span></span>

[<span data-ttu-id="06e37-207">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="06e37-207">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="06e37-208">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06e37-208">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="06e37-209">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="06e37-209">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
