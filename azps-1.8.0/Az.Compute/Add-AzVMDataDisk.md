---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 56f78fe75ab01db70fb7af1fe2eba98003387342
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917516"
---
# <span data-ttu-id="aa677-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aa677-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="aa677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa677-102">SYNOPSIS</span></span>
<span data-ttu-id="aa677-103">Sanal makineye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="aa677-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="aa677-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa677-104">SYNTAX</span></span>

### <span data-ttu-id="aa677-105">VmNormalDiskParameterSetName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aa677-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa677-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="aa677-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa677-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa677-107">DESCRIPTION</span></span>
<span data-ttu-id="aa677-108">**Add-AzVMDataDisk** cmdlet 'i bir veri diskini bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="aa677-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="aa677-109">Bir sanal makine oluşturduğunuzda veri diski ekleyebilirsiniz veya varolan bir sanal makineye veri diski ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa677-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="aa677-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa677-110">EXAMPLES</span></span>

### <span data-ttu-id="aa677-111">Örnek 1: yeni bir sanal makineye veri diskleri ekleme</span><span class="sxs-lookup"><span data-stu-id="aa677-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="aa677-112">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aa677-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aa677-113">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="aa677-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="aa677-114">Sonraki üç komut, $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03 değişkenlerine üç veri disklerinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="aa677-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="aa677-115">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aa677-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="aa677-116">Her biri $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="aa677-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="aa677-117">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="aa677-118">Her diskin URI 'SI $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="aa677-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="aa677-119">Örnek 2: var olan bir sanal makineye veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="aa677-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="aa677-120">İlk komut VirtualMachine07 adındaki sanal makineyi [Get-AzVM](./Get-AzVM.md) cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="aa677-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="aa677-121">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="aa677-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aa677-122">İkinci komut $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="aa677-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="aa677-123">Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aa677-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="aa677-124">Örnek 3: genelleştirilmiş bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="aa677-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="aa677-125">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aa677-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aa677-126">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="aa677-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="aa677-127">Sonraki iki komut, veri görüntüsü ve veri disklerinin yollarını sırasıyla $DataImageUri ve $DataDiskUri değişkenlerine atar.</span><span class="sxs-lookup"><span data-stu-id="aa677-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="aa677-128">Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aa677-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="aa677-129">Son komutlar $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="aa677-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="aa677-130">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="aa677-131">Örnek 4: özel bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diskleri ekleme</span><span class="sxs-lookup"><span data-stu-id="aa677-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="aa677-132">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aa677-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aa677-133">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="aa677-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="aa677-134">Sonraki komutlar veri diskinin yollarını $DataDiskUri değişkenine atar.</span><span class="sxs-lookup"><span data-stu-id="aa677-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="aa677-135">Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aa677-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="aa677-136">Son komutu $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="aa677-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="aa677-137">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="aa677-138">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa677-138">PARAMETERS</span></span>

### <span data-ttu-id="aa677-139">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="aa677-139">-Caching</span></span>
<span data-ttu-id="aa677-140">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="aa677-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aa677-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa677-142">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="aa677-142">ReadOnly</span></span>
- <span data-ttu-id="aa677-143">Yazma</span><span class="sxs-lookup"><span data-stu-id="aa677-143">ReadWrite</span></span>
- <span data-ttu-id="aa677-144">Yok varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="aa677-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="aa677-145">Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="aa677-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="aa677-146">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="aa677-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="aa677-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="aa677-147">-CreateOption</span></span>
<span data-ttu-id="aa677-148">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="aa677-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="aa677-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aa677-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa677-150">Nota.</span><span class="sxs-lookup"><span data-stu-id="aa677-150">Attach.</span></span>
<span data-ttu-id="aa677-151">Özel bir diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="aa677-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="aa677-152">Bu seçeneği belirttiğinizde *Sourceımageuri* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="aa677-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="aa677-153">Bu *, Azure* platformuna sanal sabit diskin (VHD) sanal sabit diskinin (VHD), sanal makineye veri diski olarak iliştirileceği yeri bildirmek için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="aa677-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="aa677-154">Boşaltma.</span><span class="sxs-lookup"><span data-stu-id="aa677-154">Empty.</span></span>
<span data-ttu-id="aa677-155">Boş bir veri disketi oluşturmak için bunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="aa677-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="aa677-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="aa677-156">FromImage.</span></span>
<span data-ttu-id="aa677-157">Genelleştirilmiş bir yansıma veya diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="aa677-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="aa677-158">Bu seçeneği belirttiğinizde, Azure platformuna veri diski olarak eklenecek VHD 'nin konumunu belirtmek için *Sourceımageuri* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="aa677-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="aa677-159">*Vhduri* parametresi, sanal makine tarafından kullanıldığında VERI diski VHD 'nin depolanacağı konumu tanımlayan konum olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aa677-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="aa677-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa677-160">-DefaultProfile</span></span>
<span data-ttu-id="aa677-161">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa677-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa677-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="aa677-162">-DiskSizeInGB</span></span>
<span data-ttu-id="aa677-163">Sanal makineye eklenecek boş bir diskin boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-163">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="aa677-164">-LUN</span><span class="sxs-lookup"><span data-stu-id="aa677-164">-Lun</span></span>
<span data-ttu-id="aa677-165">Veri diskinin mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-165">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="aa677-166">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="aa677-166">-ManagedDiskId</span></span>
<span data-ttu-id="aa677-167">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-167">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="aa677-168">-Ad</span><span class="sxs-lookup"><span data-stu-id="aa677-168">-Name</span></span>
<span data-ttu-id="aa677-169">Eklenecek veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-169">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa677-170">-Sourceımageuri</span><span class="sxs-lookup"><span data-stu-id="aa677-170">-SourceImageUri</span></span>
<span data-ttu-id="aa677-171">Bu cmdlet 'in ilişolduğu diskin Kaynak URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-171">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="aa677-172">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="aa677-172">-StorageAccountType</span></span>
<span data-ttu-id="aa677-173">Yönetilen diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-173">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa677-174">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="aa677-174">-VhdUri</span></span>
<span data-ttu-id="aa677-175">Bir platform görüntüsü veya Kullanıcı görüntüsü kullanıldığında oluşturulacak sanal sabit disk (VHD) dosyasının Tekdüzen Kaynak tanımlayıcısını (VHD) belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-175">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="aa677-176">Bu cmdlet, resim ikili büyük nesnesini (blob) bu konuma kopyalar.</span><span class="sxs-lookup"><span data-stu-id="aa677-176">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="aa677-177">Bu, sanal makinenin başlayacağı konumdur.</span><span class="sxs-lookup"><span data-stu-id="aa677-177">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="aa677-178">-VM</span><span class="sxs-lookup"><span data-stu-id="aa677-178">-VM</span></span>
<span data-ttu-id="aa677-179">Veri diskinin ekleneceği yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-179">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="aa677-180">Bir sanal makine nesnesi edinmek için **Get-AzVM** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa677-180">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="aa677-181">Sanal makine nesnesi oluşturmak için **New-AzVMConfig** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa677-181">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa677-182">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="aa677-182">-WriteAccelerator</span></span>
<span data-ttu-id="aa677-183">Yönetilen veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa677-183">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa677-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa677-184">CommonParameters</span></span>
<span data-ttu-id="aa677-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa677-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa677-186">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa677-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa677-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa677-187">INPUTS</span></span>

### <span data-ttu-id="aa677-188">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="aa677-188">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="aa677-189">System. String</span><span class="sxs-lookup"><span data-stu-id="aa677-189">System.String</span></span>

### <span data-ttu-id="aa677-190">Microsoft. Azure. Management. COMPUTE. model. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="aa677-190">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="aa677-191">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="aa677-191">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="aa677-192">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa677-192">OUTPUTS</span></span>

### <span data-ttu-id="aa677-193">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="aa677-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="aa677-194">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="aa677-194">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="aa677-195">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa677-195">NOTES</span></span>

## <span data-ttu-id="aa677-196">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa677-196">RELATED LINKS</span></span>

[<span data-ttu-id="aa677-197">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aa677-197">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="aa677-198">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="aa677-198">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="aa677-199">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="aa677-199">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
