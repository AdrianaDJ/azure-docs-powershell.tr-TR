---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 7566c1ef5c8e9cbf2134bc18b3aecf37d9f88bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588987"
---
# <span data-ttu-id="e064b-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e064b-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="e064b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e064b-102">SYNOPSIS</span></span>
<span data-ttu-id="e064b-103">Sanal makineye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="e064b-103">Adds a data disk to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e064b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e064b-104">SYNTAX</span></span>

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [<CommonParameters>]
```

## <span data-ttu-id="e064b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e064b-105">DESCRIPTION</span></span>
<span data-ttu-id="e064b-106">**Add-Azurermvmdatadısk** cmdlet 'i, bir sanal makineye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="e064b-106">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="e064b-107">Bir sanal makine oluşturduğunuzda veri diski ekleyebilirsiniz veya varolan bir sanal makineye veri diski ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e064b-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="e064b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e064b-108">EXAMPLES</span></span>

### <span data-ttu-id="e064b-109">Örnek 1: yeni bir sanal makineye veri diskleri ekleme</span><span class="sxs-lookup"><span data-stu-id="e064b-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="e064b-110">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e064b-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e064b-111">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="e064b-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="e064b-112">Sonraki üç komut, $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03 değişkenlerine üç veri disklerinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="e064b-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="e064b-113">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e064b-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="e064b-114">Her biri $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="e064b-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e064b-115">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="e064b-116">Her diskin URI 'SI $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="e064b-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="e064b-117">Örnek 2: var olan bir sanal makineye veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="e064b-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="e064b-118">İlk komut VirtualMachine07 adındaki sanal makineyi [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="e064b-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="e064b-119">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="e064b-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="e064b-120">İkinci komut $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="e064b-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="e064b-121">Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e064b-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="e064b-122">Örnek 3: genelleştirilmiş bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="e064b-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="e064b-123">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e064b-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e064b-124">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="e064b-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="e064b-125">Sonraki iki komut, veri görüntüsü ve veri disklerinin yollarını sırasıyla $DataImageUri ve $DataDiskUri değişkenlerine atar.</span><span class="sxs-lookup"><span data-stu-id="e064b-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="e064b-126">Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e064b-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="e064b-127">Son komutlar $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="e064b-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e064b-128">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="e064b-129">Örnek 4: özel bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diskleri ekleme</span><span class="sxs-lookup"><span data-stu-id="e064b-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="e064b-130">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e064b-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e064b-131">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="e064b-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="e064b-132">Sonraki komutlar veri diskinin yollarını $DataDiskUri değişkenine atar.</span><span class="sxs-lookup"><span data-stu-id="e064b-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="e064b-133">Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e064b-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="e064b-134">Son komutu $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="e064b-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="e064b-135">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="e064b-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e064b-136">PARAMETERS</span></span>

### <span data-ttu-id="e064b-137">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="e064b-137">-Caching</span></span>
<span data-ttu-id="e064b-138">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="e064b-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e064b-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e064b-140">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="e064b-140">ReadOnly</span></span>
- <span data-ttu-id="e064b-141">Yazma</span><span class="sxs-lookup"><span data-stu-id="e064b-141">ReadWrite</span></span>
- <span data-ttu-id="e064b-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e064b-142">None</span></span>

<span data-ttu-id="e064b-143">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="e064b-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="e064b-144">Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="e064b-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="e064b-145">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="e064b-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-146">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e064b-146">-CreateOption</span></span>
<span data-ttu-id="e064b-147">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="e064b-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="e064b-148">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e064b-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e064b-149">Nota.</span><span class="sxs-lookup"><span data-stu-id="e064b-149">Attach.</span></span>
<span data-ttu-id="e064b-150">Özel bir diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="e064b-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="e064b-151">Bu seçeneği belirttiğinizde *Sourceımageuri* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="e064b-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="e064b-152">Bu *, Azure* platformuna sanal sabit diskin (VHD) sanal sabit diskinin (VHD), sanal makineye veri diski olarak iliştirileceği yeri bildirmek için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e064b-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="e064b-153">Boşaltma.</span><span class="sxs-lookup"><span data-stu-id="e064b-153">Empty.</span></span>
<span data-ttu-id="e064b-154">Boş bir veri disketi oluşturmak için bunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="e064b-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="e064b-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="e064b-155">FromImage.</span></span>
<span data-ttu-id="e064b-156">Genelleştirilmiş bir yansıma veya diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="e064b-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="e064b-157">Bu seçeneği belirttiğinizde, Azure platformuna veri diski olarak eklenecek VHD 'nin konumunu belirtmek için *Sourceımageuri* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e064b-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="e064b-158">*Vhduri* parametresi, sanal makine tarafından kullanıldığında VERI diski VHD 'nin depolanacağı konumu tanımlayan konum olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e064b-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-159">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e064b-159">-DiskSizeInGB</span></span>
<span data-ttu-id="e064b-160">Sanal makineye eklenecek boş bir diskin boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-160">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-161">-LUN</span><span class="sxs-lookup"><span data-stu-id="e064b-161">-Lun</span></span>
<span data-ttu-id="e064b-162">Veri diskinin mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-162">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-163">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="e064b-163">-ManagedDiskId</span></span>
<span data-ttu-id="e064b-164">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-164">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-165">-Ad</span><span class="sxs-lookup"><span data-stu-id="e064b-165">-Name</span></span>
<span data-ttu-id="e064b-166">Eklenecek veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-166">Specifies the name of the data disk to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-167">-Sourceımageuri</span><span class="sxs-lookup"><span data-stu-id="e064b-167">-SourceImageUri</span></span>
<span data-ttu-id="e064b-168">Bu cmdlet 'in ilişolduğu diskin Kaynak URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-168">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-169">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e064b-169">-StorageAccountType</span></span>
<span data-ttu-id="e064b-170">Yönetilen diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-170">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-171">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="e064b-171">-VhdUri</span></span>
<span data-ttu-id="e064b-172">Bir platform görüntüsü veya Kullanıcı görüntüsü kullanıldığında oluşturulacak sanal sabit disk (VHD) dosyasının Tekdüzen Kaynak tanımlayıcısını (VHD) belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-172">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="e064b-173">Bu cmdlet, resim ikili büyük nesnesini (blob) bu konuma kopyalar.</span><span class="sxs-lookup"><span data-stu-id="e064b-173">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="e064b-174">Bu, sanal makinenin başlayacağı konumdur.</span><span class="sxs-lookup"><span data-stu-id="e064b-174">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-175">-VM</span><span class="sxs-lookup"><span data-stu-id="e064b-175">-VM</span></span>
<span data-ttu-id="e064b-176">Veri diskinin ekleneceği yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e064b-176">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="e064b-177">Sanal makine nesnesi edinmek için **Get-AzureRmVM** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e064b-177">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="e064b-178">Sanal makine nesnesi oluşturmak için **New-AzureRmVMConfig** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e064b-178">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e064b-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e064b-179">CommonParameters</span></span>
<span data-ttu-id="e064b-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e064b-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e064b-181">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e064b-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e064b-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e064b-182">INPUTS</span></span>

### <span data-ttu-id="e064b-183">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e064b-183">None</span></span>
<span data-ttu-id="e064b-184">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e064b-184">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e064b-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e064b-185">OUTPUTS</span></span>

## <span data-ttu-id="e064b-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e064b-186">NOTES</span></span>

## <span data-ttu-id="e064b-187">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e064b-187">RELATED LINKS</span></span>

[<span data-ttu-id="e064b-188">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e064b-188">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="e064b-189">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e064b-189">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e064b-190">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="e064b-190">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
