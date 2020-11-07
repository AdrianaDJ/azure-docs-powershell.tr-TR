---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 4c7e59b847ec1ae1d95c5a884c8979d12d193084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935965"
---
# <span data-ttu-id="7b5ce-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7b5ce-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="7b5ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="7b5ce-103">Sanal makineye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="7b5ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b5ce-104">SYNTAX</span></span>

```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b5ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b5ce-105">DESCRIPTION</span></span>
<span data-ttu-id="7b5ce-106">**Add-AzVMDataDisk** cmdlet 'i bir veri diskini bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-106">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="7b5ce-107">Bir sanal makine oluşturduğunuzda veri diski ekleyebilirsiniz veya varolan bir sanal makineye veri diski ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="7b5ce-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b5ce-108">EXAMPLES</span></span>

### <span data-ttu-id="7b5ce-109">Örnek 1: yeni bir sanal makineye veri diskleri ekleme</span><span class="sxs-lookup"><span data-stu-id="7b5ce-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="7b5ce-110">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7b5ce-111">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="7b5ce-112">Sonraki üç komut, $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03 değişkenlerine üç veri disklerinin yollarını atar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="7b5ce-113">Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="7b5ce-114">Her biri $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7b5ce-115">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="7b5ce-116">Her diskin URI 'SI $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="7b5ce-117">Örnek 2: var olan bir sanal makineye veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="7b5ce-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="7b5ce-118">İlk komut VirtualMachine07 adındaki sanal makineyi [Get-AzVM](./Get-AzVM.md) cmdlet 'ini kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="7b5ce-119">Komut, $VirtualMachine değişkeninde sanal makineyi depolar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="7b5ce-120">İkinci komut $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="7b5ce-121">Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="7b5ce-122">Örnek 3: genelleştirilmiş bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diski ekleme</span><span class="sxs-lookup"><span data-stu-id="7b5ce-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="7b5ce-123">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7b5ce-124">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="7b5ce-125">Sonraki iki komut, veri görüntüsü ve veri disklerinin yollarını sırasıyla $DataImageUri ve $DataDiskUri değişkenlerine atar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="7b5ce-126">Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="7b5ce-127">Son komutlar $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7b5ce-128">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="7b5ce-129">Örnek 4: özel bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diskleri ekleme</span><span class="sxs-lookup"><span data-stu-id="7b5ce-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="7b5ce-130">İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7b5ce-131">Bu komut sanal makineye bir ad ve boyut atar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="7b5ce-132">Sonraki komutlar veri diskinin yollarını $DataDiskUri değişkenine atar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="7b5ce-133">Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="7b5ce-134">Son komutu $VirtualMachine depolanan sanal makineye bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="7b5ce-135">Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="7b5ce-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b5ce-136">PARAMETERS</span></span>

### <span data-ttu-id="7b5ce-137">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="7b5ce-137">-Caching</span></span>
<span data-ttu-id="7b5ce-138">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="7b5ce-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7b5ce-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b5ce-140">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="7b5ce-140">ReadOnly</span></span>
- <span data-ttu-id="7b5ce-141">Yazma</span><span class="sxs-lookup"><span data-stu-id="7b5ce-141">ReadWrite</span></span>
- <span data-ttu-id="7b5ce-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7b5ce-142">None</span></span>

<span data-ttu-id="7b5ce-143">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="7b5ce-144">Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="7b5ce-145">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="7b5ce-146">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="7b5ce-146">-CreateOption</span></span>
<span data-ttu-id="7b5ce-147">Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="7b5ce-148">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7b5ce-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b5ce-149">Nota.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-149">Attach.</span></span>
<span data-ttu-id="7b5ce-150">Özel bir diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="7b5ce-151">Bu seçeneği belirttiğinizde *Sourceımageuri* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="7b5ce-152">Bu *, Azure* platformuna sanal sabit diskin (VHD) sanal sabit diskinin (VHD), sanal makineye veri diski olarak iliştirileceği yeri bildirmek için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="7b5ce-153">Boşaltma.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-153">Empty.</span></span>
<span data-ttu-id="7b5ce-154">Boş bir veri disketi oluşturmak için bunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="7b5ce-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-155">FromImage.</span></span>
<span data-ttu-id="7b5ce-156">Genelleştirilmiş bir yansıma veya diskten sanal makine oluşturmak için bu seçeneği belirtin.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="7b5ce-157">Bu seçeneği belirttiğinizde, Azure platformuna veri diski olarak eklenecek VHD 'nin konumunu belirtmek için *Sourceımageuri* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="7b5ce-158">*Vhduri* parametresi, sanal makine tarafından kullanıldığında VERI diski VHD 'nin depolanacağı konumu tanımlayan konum olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="7b5ce-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b5ce-159">-DefaultProfile</span></span>
<span data-ttu-id="7b5ce-160">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-160">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5ce-161">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7b5ce-161">-DiskSizeInGB</span></span>
<span data-ttu-id="7b5ce-162">Sanal makineye eklenecek boş bir diskin boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-162">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="7b5ce-163">-LUN</span><span class="sxs-lookup"><span data-stu-id="7b5ce-163">-Lun</span></span>
<span data-ttu-id="7b5ce-164">Veri diskinin mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-164">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="7b5ce-165">-Manageddiskıd</span><span class="sxs-lookup"><span data-stu-id="7b5ce-165">-ManagedDiskId</span></span>
<span data-ttu-id="7b5ce-166">Yönetilen bir diskin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-166">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="7b5ce-167">-Ad</span><span class="sxs-lookup"><span data-stu-id="7b5ce-167">-Name</span></span>
<span data-ttu-id="7b5ce-168">Eklenecek veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-168">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="7b5ce-169">-Sourceımageuri</span><span class="sxs-lookup"><span data-stu-id="7b5ce-169">-SourceImageUri</span></span>
<span data-ttu-id="7b5ce-170">Bu cmdlet 'in ilişolduğu diskin Kaynak URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-170">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="7b5ce-171">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7b5ce-171">-StorageAccountType</span></span>
<span data-ttu-id="7b5ce-172">Yönetilen diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-172">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="7b5ce-173">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="7b5ce-173">-VhdUri</span></span>
<span data-ttu-id="7b5ce-174">Bir platform görüntüsü veya Kullanıcı görüntüsü kullanıldığında oluşturulacak sanal sabit disk (VHD) dosyasının Tekdüzen Kaynak tanımlayıcısını (VHD) belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-174">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="7b5ce-175">Bu cmdlet, resim ikili büyük nesnesini (blob) bu konuma kopyalar.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-175">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="7b5ce-176">Bu, sanal makinenin başlayacağı konumdur.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-176">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="7b5ce-177">-VM</span><span class="sxs-lookup"><span data-stu-id="7b5ce-177">-VM</span></span>
<span data-ttu-id="7b5ce-178">Veri diskinin ekleneceği yerel sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-178">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="7b5ce-179">Bir sanal makine nesnesi edinmek için **Get-AzVM** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-179">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="7b5ce-180">Sanal makine nesnesi oluşturmak için **New-AzVMConfig** cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-180">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="7b5ce-181">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7b5ce-181">-WriteAccelerator</span></span>
<span data-ttu-id="7b5ce-182">Veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-182">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b5ce-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b5ce-183">CommonParameters</span></span>
<span data-ttu-id="7b5ce-184">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b5ce-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b5ce-185">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b5ce-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b5ce-186">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b5ce-186">INPUTS</span></span>

### <span data-ttu-id="7b5ce-187">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7b5ce-187">PSVirtualMachine</span></span>
<span data-ttu-id="7b5ce-188">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7b5ce-188">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="7b5ce-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b5ce-189">OUTPUTS</span></span>

### <span data-ttu-id="7b5ce-190">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7b5ce-190">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7b5ce-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b5ce-191">NOTES</span></span>

## <span data-ttu-id="7b5ce-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b5ce-192">RELATED LINKS</span></span>

[<span data-ttu-id="7b5ce-193">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7b5ce-193">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="7b5ce-194">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7b5ce-194">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7b5ce-195">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="7b5ce-195">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
